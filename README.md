# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-21)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-7.17** over 1379 fills |
| 🔴 P&L / contract | -0.5¢ |
| Win rate | 75% |
| Profit factor | 0.96 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.18 |
| 🟢 Today | $+2.94 (111 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 369 runs / ~31h | rewards $11,467.52, fills $-26,430.66 (169701 settled, 46281 open) → **net $-14,963.14** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 298 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 34 | +1.1¢ | -16.7¢ to +21.1¢ | $+0.38 | collecting (34/100) |
| `fade_move` 24h | 41 | +1.7¢ | -13.6¢ to +17.6¢ | $+0.69 | collecting (41/100) |
| `fade_move` 30h | 33 | -7.1¢ | -21.2¢ to +7.1¢ | $-2.35 | collecting (33/100) |
| `fav_longshot` 18h | 210 | -3.0¢ | -9.3¢ to +3.5¢ | $-6.24 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 209 | +3.2¢ | -2.5¢ to +9.1¢ | $+6.63 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 209 | -0.3¢ | -6.8¢ to +5.7¢ | $-0.71 | no edge yet (CI spans 0) |
| `follow_move` 18h | 35 | -8.5¢ | -28.4¢ to +13.2¢ | $-2.96 | collecting (35/100) |
| `follow_move` 24h | 43 | +1.2¢ | -14.5¢ to +17.0¢ | $+0.52 | collecting (43/100) |
| `follow_move` 30h | 26 | +4.2¢ | -10.2¢ to +19.6¢ | $+1.10 | collecting (26/100) |
| `overround` 18h | 25 | +2.8¢ | -7.1¢ to +12.5¢ | $+0.69 | collecting (25/100) |
| `overround` 24h | 14 | -1.4¢ | — | $-0.19 | collecting (14/100) |
| `overround` 30h | 28 | -7.8¢ | -23.8¢ to +6.5¢ | $-2.17 | collecting (28/100) |
| `rv_updown_3c` 6h | 21 | -23.3¢ | -40.8¢ to -6.8¢ | $-4.89 | collecting (21/100) |
| `rv_updown_6c` 6h | 17 | -29.2¢ | -48.5¢ to -10.1¢ | $-4.96 | collecting (17/100) |
| `sell_longshot` 6h | 94 | -1.0¢ | -5.7¢ to +3.4¢ | $-0.96 | collecting (94/100) |
| `sell_longshot` 12h | 8 | +8.8¢ | — | $+0.70 | collecting (8/100) |
| `sell_longshot_div` 6h | 121 | +1.1¢ | -5.6¢ to +6.5¢ | $+1.30 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 151 | +1.9¢ | -4.3¢ to +6.7¢ | $+2.91 | no edge yet (CI spans 0) |
| `tails` 18h | 22 | +0.8¢ | -15.0¢ to +13.6¢ | $+0.18 | collecting (22/100) |
| `tails` 24h | 21 | +8.3¢ | -4.5¢ to +16.1¢ | $+1.74 | collecting (21/100) |
| `tails` 30h | 14 | +4.9¢ | — | $+0.69 | collecting (14/100) |

## Daily reports

- [2026-11-21](paper/reports/2026-11-21.md)
- [2026-11-20](paper/reports/2026-11-20.md)
- [2026-11-19](paper/reports/2026-11-19.md)
- [2026-11-18](paper/reports/2026-11-18.md)
- [2026-11-17](paper/reports/2026-11-17.md)
- [2026-11-16](paper/reports/2026-11-16.md)
- [2026-11-15](paper/reports/2026-11-15.md)
- [2026-11-14](paper/reports/2026-11-14.md)
- [2026-11-13](paper/reports/2026-11-13.md)
- [2026-11-12](paper/reports/2026-11-12.md)
- [2026-11-11](paper/reports/2026-11-11.md)
- [2026-11-10](paper/reports/2026-11-10.md)
- [2026-11-09](paper/reports/2026-11-09.md)
- [2026-11-08](paper/reports/2026-11-08.md)
