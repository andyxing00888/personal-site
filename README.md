# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-09)

| Metric | Value |
|---|--:|
| 🟢 Total P&L | **$+3.79** over 468 fills |
| 🟢 P&L / contract | +0.8¢ |
| Win rate | 76% |
| Profit factor | 1.06 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | 2.28 |
| 🟢 Today | $+4.22 (55 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 154 runs / ~30h | rewards $4,742.68, fills $-5,958.16 (49337.3 settled, 42289.5 open) → **net $-1,215.48** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 131 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 153 runs | 10336 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 12 | +3.9¢ | — | $+0.47 | collecting (12/100) |
| `fade_move` 24h | 12 | -13.4¢ | — | $-1.61 | collecting (12/100) |
| `fade_move` 30h | 12 | -10.2¢ | — | $-1.22 | collecting (12/100) |
| `fav_longshot` 18h | 72 | +0.6¢ | -10.6¢ to +11.4¢ | $+0.41 | collecting (72/100) |
| `fav_longshot` 24h | 80 | +5.2¢ | -4.8¢ to +15.1¢ | $+4.19 | collecting (80/100) |
| `fav_longshot` 30h | 72 | -0.6¢ | -11.1¢ to +9.4¢ | $-0.41 | collecting (72/100) |
| `follow_move` 18h | 13 | -10.5¢ | — | $-1.36 | collecting (13/100) |
| `follow_move` 24h | 12 | +8.1¢ | — | $+0.97 | collecting (12/100) |
| `follow_move` 30h | 9 | +5.8¢ | — | $+0.52 | collecting (9/100) |
| `overround` 18h | 4 | +8.0¢ | — | $+0.32 | collecting (4/100) |
| `overround` 24h | 7 | -13.6¢ | — | $-0.95 | collecting (7/100) |
| `overround` 30h | 3 | +21.7¢ | — | $+0.65 | collecting (3/100) |
| `rv_updown_3c` 6h | 4 | -28.0¢ | — | $-1.12 | collecting (4/100) |
| `rv_updown_6c` 6h | 3 | -37.7¢ | — | $-1.13 | collecting (3/100) |
| `sell_longshot` 6h | 23 | +1.3¢ | -7.4¢ to +11.5¢ | $+0.31 | collecting (23/100) |
| `sell_longshot` 12h | 2 | +7.5¢ | — | $+0.15 | collecting (2/100) |
| `sell_longshot_div` 6h | 53 | +6.7¢ | +5.3¢ to +7.9¢ | $+3.57 | collecting (53/100) |
| `sell_longshot_div` 24h | 51 | -1.0¢ | -15.7¢ to +9.4¢ | $-0.51 | collecting (51/100) |
| `tails` 18h | 8 | -8.5¢ | — | $-0.68 | collecting (8/100) |
| `tails` 24h | 8 | -0.8¢ | — | $-0.06 | collecting (8/100) |
| `tails` 30h | 6 | +12.0¢ | — | $+0.72 | collecting (6/100) |

## Daily reports

- [2026-11-09](paper/reports/2026-11-09.md)
- [2026-11-08](paper/reports/2026-11-08.md)
- [2026-11-07](paper/reports/2026-11-07.md)
- [2026-11-06](paper/reports/2026-11-06.md)
- [2026-11-05](paper/reports/2026-11-05.md)
- [2026-11-04](paper/reports/2026-11-04.md)
- [2026-11-03](paper/reports/2026-11-03.md)
- [2026-11-02](paper/reports/2026-11-02.md)
- [2026-11-01](paper/reports/2026-11-01.md)
- [2026-10-31](paper/reports/2026-10-31.md)
