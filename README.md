# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-08)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-0.43** over 413 fills |
| 🔴 P&L / contract | -0.1¢ |
| Win rate | 76% |
| Profit factor | 0.99 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | -0.30 |
| 🟢 Today | $+5.83 (71 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 139 runs / ~30h | rewards $4,281.06, fills $-5,331.21 (39206.8 settled, 45137.3 open) → **net $-1,050.15** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 116 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 138 runs | 9650 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 8 | +9.5¢ | — | $+0.76 | collecting (8/100) |
| `fade_move` 24h | 12 | -13.4¢ | — | $-1.61 | collecting (12/100) |
| `fade_move` 30h | 10 | -14.7¢ | — | $-1.47 | collecting (10/100) |
| `fav_longshot` 18h | 57 | -0.5¢ | -12.9¢ to +11.5¢ | $-0.31 | collecting (57/100) |
| `fav_longshot` 24h | 75 | +4.3¢ | -6.4¢ to +15.8¢ | $+3.21 | collecting (75/100) |
| `fav_longshot` 30h | 57 | -5.1¢ | -17.8¢ to +7.2¢ | $-2.88 | collecting (57/100) |
| `follow_move` 18h | 8 | -10.4¢ | — | $-0.83 | collecting (8/100) |
| `follow_move` 24h | 12 | +8.1¢ | — | $+0.97 | collecting (12/100) |
| `follow_move` 30h | 6 | +9.5¢ | — | $+0.57 | collecting (6/100) |
| `overround` 18h | 4 | +8.0¢ | — | $+0.32 | collecting (4/100) |
| `overround` 24h | 7 | -13.6¢ | — | $-0.95 | collecting (7/100) |
| `overround` 30h | 3 | +21.7¢ | — | $+0.65 | collecting (3/100) |
| `rv_updown_3c` 6h | 4 | -28.0¢ | — | $-1.12 | collecting (4/100) |
| `rv_updown_6c` 6h | 3 | -37.7¢ | — | $-1.13 | collecting (3/100) |
| `sell_longshot` 6h | 23 | +1.3¢ | -7.4¢ to +11.5¢ | $+0.31 | collecting (23/100) |
| `sell_longshot` 12h | 2 | +7.5¢ | — | $+0.15 | collecting (2/100) |
| `sell_longshot_div` 6h | 52 | +6.6¢ | +5.2¢ to +7.7¢ | $+3.44 | collecting (52/100) |
| `sell_longshot_div` 24h | 49 | -1.5¢ | -18.5¢ to +9.3¢ | $-0.72 | collecting (49/100) |
| `tails` 18h | 8 | -8.5¢ | — | $-0.68 | collecting (8/100) |
| `tails` 24h | 7 | -2.6¢ | — | $-0.18 | collecting (7/100) |
| `tails` 30h | 4 | +12.8¢ | — | $+0.51 | collecting (4/100) |

## Daily reports

- [2026-11-08](paper/reports/2026-11-08.md)
- [2026-11-07](paper/reports/2026-11-07.md)
- [2026-11-06](paper/reports/2026-11-06.md)
- [2026-11-05](paper/reports/2026-11-05.md)
- [2026-11-04](paper/reports/2026-11-04.md)
- [2026-11-03](paper/reports/2026-11-03.md)
- [2026-11-02](paper/reports/2026-11-02.md)
- [2026-11-01](paper/reports/2026-11-01.md)
- [2026-10-31](paper/reports/2026-10-31.md)
