# Kalshi strategy research

Goal: find a **real, repeatable** edge on Kalshi and prove it on forward paper data before any real money.
Nothing here places orders; everything reads public endpoints.

## How to judge a strategy (non-negotiable)
- Fees first. Taker `ceil(0.07·p(1-p))` to the cent (min 1¢ per leg inside (0,1)); maker `ceil(0.0175·p(1-p))`.
  Polymarket taker `rate·p(1-p)` (sports 0.05, no rounding), makers free.
- Backtests are screens, not proof: small samples and many cells have fooled us repeatedly.
  Count the cells you searched; one positive cell out of 50 is noise until forward data agrees.
- Verdict only from **forward paper data**: 100+ fills and an event-clustered bootstrap CI above 0
  (`kalshi.stats.boot`). Maker fills count only on a trade *through* the price (`kalshi.fills.fill_pnl`).
- Ignore quotes from wide books (spread > ~5¢): a 2¢/99¢ book is not a price. Hourly candle bid/ask are
  end-of-hour snapshots with no size; confirm any "arb" with trade prints (`/markets/trades`) or live depth.
- Report results plainly, including dead ends. Record them under "Status" below so nobody re-tests them.

## Where edges can come from (diversify across these, not within one)
| Type | Idea | Status |
|---|---|---|
| Information | forecast/model beats price (weather, gas, TSA, ERCOT, index) | **dead**: pros have finer data (gas mid Brier 0.013) |
| Structural arb | ladder/bucket/updown must agree (`consistency.py`) | rare: 14 trade-confirmed hits / 86 days, ~0.42 total |
| Cross-venue | Kalshi vs Polymarket same event (`xvenue.py`) | none: sports within 1–2¢; Fed Dec, House/Senate control match to ~1¢ |
| Real-time underlying | crypto daily vs Coinbase spot + realized vol (`crypto.py`) | **dead**: Kalshi beats the model's Brier at 1–20h; model-edge trades lose |
| Stale weekend quotes | KXINXU vs ES-futures fair value (`overnight.py`) | inconclusive: model Brier beats Kalshi Sun eve–Mon pre-open (0.108 vs 0.119) but P&L is one weekend (Sep 21, near the ES roll) |
| Momentum/reversal | 24h→6h move predicts outcome? (`drift.py`) | sports slight reversal (n.s.); non-sports "momentum" was 2 days of commodity/crypto moves |
| Relative value | thin series priced off a deep linked one (`consistency.py rv`) | `rv_updown_*` in paper; bucket maker quotes lose (adverse selection) |
| Behavioral | longshot overpricing, favorite underpricing (`calib.py`, `paper/strategies.py`) | sports calibrated; non-sports YES<15¢ ~3.5¢ rich in 20/23 series → `sell_longshot_div` paper basket |
| Liquidity provision | rewards for resting quotes (`lip.py`, `/incentive_programs`) | **most promising**; forward-simulated hourly |
| Carry | interest on cash/positions, high-prob bonds | bonds −4¢ in sports; interest = baseline, not edge |
| Rules/settlement | settlement source quirks (first print, rounding, revisions) | backlog |
| Event-time | scheduled releases (CPI, jobs, Fed), mentions/base rates | backlog |

Backlog worth testing next (each a different edge source):
1. **Mentions with transcripts**: word base rates from Kalshi's own settlements lose (`mentions.py`, −7 to −13¢);
   a real edge would need speech-specific context (transcripts, scheduled topics), not word history.
2. **Settlement-rule mispricing**: TSA first-published number, CPI rounding, data revisions.
3. **Scheduled-release drift**: how prices move in the hour before CPI/NFP/FOMC; fade or follow.
4. **Liquidity rewards, real version**: continuous re-quoting, inventory caps, both sides; needs an account.
5. **Options-implied S&P/Nasdaq ranges** (CBOE delayed chains) vs KXINX buckets.
6. **Sports vs sharp books** (needs the-odds-api.com key from the user).
7. **Weekend staleness, properly**: front-month ES (not the rolling ES=F), more weekends, NDX too; only
   worth a paper rule if several weekends agree.

## Tools
| File | What |
|---|---|
| `python3 -m paper.trader log/score` | forward paper trader for rules in `paper/strategies.py` (hourly / daily on Actions) |
| `python3 -m paper.report` | daily report → `README.md`, `paper/reports/`, `docs/index.html` dashboard |
| `consistency.py pull/(backtest)/rv/live/log` | S&P/Nasdaq cross-series arb, relative value, paper `rv_updown_*` |
| `xvenue.py [log]` | Kalshi vs Polymarket sports moneylines, matched by slug/ticker |
| `lip.py [Q]/watch/track/report` | liquidity-reward estimate, watchlist, hourly forward simulation |
| `calib.py pull/(report)` | calibration by category/series/price bin; `EXCLUDE=Sports ROWS=...` |
| `overnight.py` | KXINXU vs S&P futures (Yahoo ES=F hourly) by overnight / weekend / session |
| `drift.py` | 24h→6h move vs outcome (momentum/fade) on calib caches |
| `crypto.py pull/(report)` | KXBTCD/KXETHD 5pm vs lognormal spot model (Coinbase hourly) |
| `mentions.py pull/(report)` | mention-market calibration (`ROWS=calib_mentions.csv calib.py`) and word base rates |
| `legacy/` (`python3 -m legacy.analyze` etc.) | earlier model backtests and `pull_*` data pullers (all lost) |
| `kalshi/` | shared library: `api` (get, iso_ts), `fees`, `fills`, `stats` (mean, boot, brier, cdf), `store` (csv), `paths`, `universe` |

GitHub Actions `.github/workflows/paper.yml` runs `python3 -m paper.cron`, a ~5.5h loop (GitHub drops many scheduled
runs, so cron only re-arms it every 3h): hourly log + scans at :05, daily score/report/LIP refresh after 15:00 UTC.
Add new hourly/daily jobs to `HOURLY`/`DAILY` in `paper/cron.py`, not to the workflow.
Top-level `data/` is git-ignored (caches); `paper/data/` is tracked.

## API notes (learned the hard way)
- Kalshi base `https://api.elections.kalshi.com/trade-api/v2`, no key for reads. Prices `*_dollars`, sizes `*_fp`.
- `/markets?status=settled` is flooded by parlays: pass `mve_filter=exclude`.
- `/incentive_programs?status=active` lists every liquidity reward; `period_reward` is in 1/10000 $.
  A side pays only with ≥ target size resting; reference price at target/5 depth; discount^ticks below it.
- Orderbook `/markets/{t}/orderbook` → `orderbook_fp.{yes,no}_dollars` = bids, ascending.
  A YES bid at p is a NO offer at 1−p, so yes_bid + no_bid must stay < 1 to rest without crossing.
- Polymarket gamma `/events`: max `limit=100`, `offset` ≤ ~2000; filter with `tag_slug` (nba, nfl, nhl, cfb)
  and `end_date_min/max`. Game slugs `nba-mia-lal-2026-11-02` map to Kalshi `KXNBAGAME-26NOV02MIALAL-MIA`.
- Local Python is 3.9: `datetime.fromisoformat` can't parse Kalshi's 5-digit fractions; use `s[:19] + "+00:00"`.

## Conventions
- Plain stdlib Python, small single-purpose scripts, docstring at top explains method and usage.
- Commits: no `Co-Authored-By` or any AI attribution.
