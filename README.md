# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-26)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-23.67** over 1749 fills |
| 🔴 P&L / contract | -1.4¢ |
| Win rate | 73% |
| Profit factor | 0.91 |
| Max drawdown | -$40.56 |
| Sharpe (ann.) | -3.16 |
| 🔴 Today | $-11.31 (71 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 445 runs / ~32h | rewards $15,301.86, fills $-36,829.46 (230044 settled, 60089.3 open) → **net $-21,527.59** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 356 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 47 | -1.2¢ | -16.2¢ to +16.7¢ | $-0.56 | collecting (47/100) |
| `fade_move` 24h | 53 | +7.9¢ | -6.8¢ to +22.0¢ | $+4.18 | collecting (53/100) |
| `fade_move` 30h | 41 | -2.5¢ | -14.9¢ to +10.9¢ | $-1.02 | collecting (41/100) |
| `fav_longshot` 18h | 266 | -3.2¢ | -9.3¢ to +2.8¢ | $-8.58 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 256 | +2.2¢ | -3.7¢ to +7.4¢ | $+5.57 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 261 | -1.3¢ | -7.2¢ to +4.2¢ | $-3.52 | no edge yet (CI spans 0) |
| `follow_move` 18h | 49 | -5.3¢ | -23.2¢ to +12.5¢ | $-2.58 | collecting (49/100) |
| `follow_move` 24h | 56 | -5.0¢ | -19.0¢ to +8.7¢ | $-2.80 | collecting (56/100) |
| `follow_move` 30h | 37 | -1.0¢ | -14.2¢ to +11.9¢ | $-0.36 | collecting (37/100) |
| `overround` 18h | 35 | +4.6¢ | -4.6¢ to +13.4¢ | $+1.60 | collecting (35/100) |
| `overround` 24h | 19 | -7.6¢ | -30.3¢ to +10.4¢ | $-1.44 | collecting (19/100) |
| `overround` 30h | 37 | -3.3¢ | -16.1¢ to +8.2¢ | $-1.22 | collecting (37/100) |
| `rv_updown_3c` 6h | 23 | -22.7¢ | -38.8¢ to -6.7¢ | $-5.21 | collecting (23/100) |
| `rv_updown_6c` 6h | 19 | -27.5¢ | -45.3¢ to -9.9¢ | $-5.22 | collecting (19/100) |
| `sell_longshot` 6h | 129 | -2.3¢ | -6.3¢ to +1.4¢ | $-2.99 | no edge yet (CI spans 0) |
| `sell_longshot` 12h | 15 | +2.0¢ | -7.3¢ to +10.3¢ | $+0.30 | collecting (15/100) |
| `sell_longshot_div` 6h | 153 | +0.4¢ | -5.3¢ to +5.1¢ | $+0.66 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 177 | -0.5¢ | -7.1¢ to +5.6¢ | $-0.95 | no edge yet (CI spans 0) |
| `tails` 18h | 27 | -3.1¢ | -18.8¢ to +10.3¢ | $-0.83 | collecting (27/100) |
| `tails` 24h | 25 | +1.7¢ | -13.2¢ to +13.7¢ | $+0.43 | collecting (25/100) |
| `tails` 30h | 21 | +0.7¢ | -14.3¢ to +13.0¢ | $+0.14 | collecting (21/100) |

## Daily reports

- [2026-11-26](paper/reports/2026-11-26.md)
- [2026-11-25](paper/reports/2026-11-25.md)
- [2026-11-24](paper/reports/2026-11-24.md)
- [2026-11-23](paper/reports/2026-11-23.md)
- [2026-11-22](paper/reports/2026-11-22.md)
- [2026-11-21](paper/reports/2026-11-21.md)
- [2026-11-20](paper/reports/2026-11-20.md)
- [2026-11-19](paper/reports/2026-11-19.md)
- [2026-11-18](paper/reports/2026-11-18.md)
- [2026-11-17](paper/reports/2026-11-17.md)
- [2026-11-16](paper/reports/2026-11-16.md)
- [2026-11-15](paper/reports/2026-11-15.md)
- [2026-11-14](paper/reports/2026-11-14.md)
- [2026-11-13](paper/reports/2026-11-13.md)
