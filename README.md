# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-10)

| Metric | Value |
|---|--:|
| 🟢 Total P&L | **$+9.93** over 533 fills |
| 🟢 P&L / contract | +1.9¢ |
| Win rate | 78% |
| Profit factor | 1.14 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | 5.02 |
| 🟢 Today | $+6.14 (65 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 172 runs / ~32h | rewards $5,234.07, fills $-8,907.46 (72649.3 settled, 25498.6 open) → **net $-3,673.39** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 145 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 171 runs | 11196 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 12 | +3.9¢ | — | $+0.47 | collecting (12/100) |
| `fade_move` 24h | 13 | -5.8¢ | — | $-0.75 | collecting (13/100) |
| `fade_move` 30h | 13 | -7.8¢ | — | $-1.02 | collecting (13/100) |
| `fav_longshot` 18h | 78 | +2.4¢ | -9.0¢ to +12.1¢ | $+1.90 | collecting (78/100) |
| `fav_longshot` 24h | 90 | +6.2¢ | -3.6¢ to +14.7¢ | $+5.59 | collecting (90/100) |
| `fav_longshot` 30h | 78 | +1.5¢ | -8.6¢ to +10.9¢ | $+1.19 | collecting (78/100) |
| `follow_move` 18h | 13 | -10.5¢ | — | $-1.36 | collecting (13/100) |
| `follow_move` 24h | 13 | +5.4¢ | — | $+0.70 | collecting (13/100) |
| `follow_move` 30h | 10 | +3.1¢ | — | $+0.31 | collecting (10/100) |
| `overround` 18h | 6 | +11.5¢ | — | $+0.69 | collecting (6/100) |
| `overround` 24h | 7 | -13.6¢ | — | $-0.95 | collecting (7/100) |
| `overround` 30h | 5 | +20.2¢ | — | $+1.01 | collecting (5/100) |
| `rv_updown_3c` 6h | 6 | -17.3¢ | — | $-1.04 | collecting (6/100) |
| `rv_updown_6c` 6h | 4 | -26.5¢ | — | $-1.06 | collecting (4/100) |
| `sell_longshot` 6h | 29 | +2.8¢ | -4.5¢ to +10.6¢ | $+0.82 | collecting (29/100) |
| `sell_longshot` 12h | 4 | +10.5¢ | — | $+0.42 | collecting (4/100) |
| `sell_longshot_div` 6h | 58 | +6.8¢ | +5.5¢ to +7.9¢ | $+3.95 | collecting (58/100) |
| `sell_longshot_div` 24h | 66 | -3.3¢ | -16.7¢ to +7.0¢ | $-2.20 | collecting (66/100) |
| `tails` 18h | 9 | -5.6¢ | — | $-0.50 | collecting (9/100) |
| `tails` 24h | 10 | +2.8¢ | — | $+0.28 | collecting (10/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

- [2026-11-10](paper/reports/2026-11-10.md)
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
