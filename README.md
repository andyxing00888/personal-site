# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-22)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-10.76** over 1454 fills |
| 🔴 P&L / contract | -0.7¢ |
| Win rate | 74% |
| Profit factor | 0.95 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.71 |
| 🔴 Today | $-3.59 (75 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 388 runs / ~31h | rewards $13,156.92, fills $-32,563.31 (201011 settled, 42926.2 open) → **net $-19,406.39** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 317 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 39 | +2.6¢ | -15.2¢ to +21.1¢ | $+1.02 | collecting (39/100) |
| `fade_move` 24h | 41 | +1.7¢ | -13.6¢ to +17.6¢ | $+0.69 | collecting (41/100) |
| `fade_move` 30h | 35 | -3.1¢ | -17.4¢ to +12.4¢ | $-1.09 | collecting (35/100) |
| `fav_longshot` 18h | 226 | -2.6¢ | -8.8¢ to +3.7¢ | $-5.98 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 218 | +3.3¢ | -2.6¢ to +9.0¢ | $+7.27 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 219 | -0.5¢ | -6.7¢ to +5.8¢ | $-1.18 | no edge yet (CI spans 0) |
| `follow_move` 18h | 40 | -9.1¢ | -28.2¢ to +10.1¢ | $-3.65 | collecting (40/100) |
| `follow_move` 24h | 44 | +2.4¢ | -13.1¢ to +16.6¢ | $+1.07 | collecting (44/100) |
| `follow_move` 30h | 29 | -2.2¢ | -17.3¢ to +15.2¢ | $-0.63 | collecting (29/100) |
| `overround` 18h | 29 | +0.8¢ | -8.6¢ to +10.3¢ | $+0.23 | collecting (29/100) |
| `overround` 24h | 15 | -0.9¢ | -20.1¢ to +12.7¢ | $-0.14 | collecting (15/100) |
| `overround` 30h | 29 | -7.2¢ | -23.0¢ to +6.8¢ | $-2.10 | collecting (29/100) |
| `rv_updown_3c` 6h | 21 | -23.3¢ | -40.8¢ to -6.8¢ | $-4.89 | collecting (21/100) |
| `rv_updown_6c` 6h | 17 | -29.2¢ | -48.5¢ to -10.1¢ | $-4.96 | collecting (17/100) |
| `sell_longshot` 6h | 94 | -1.0¢ | -5.7¢ to +3.4¢ | $-0.96 | collecting (94/100) |
| `sell_longshot` 12h | 9 | +8.3¢ | — | $+0.75 | collecting (9/100) |
| `sell_longshot_div` 6h | 125 | +1.2¢ | -5.5¢ to +6.7¢ | $+1.56 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 164 | -0.7¢ | -7.2¢ to +5.3¢ | $-1.11 | no edge yet (CI spans 0) |
| `tails` 18h | 22 | +0.8¢ | -15.0¢ to +13.6¢ | $+0.18 | collecting (22/100) |
| `tails` 24h | 21 | +8.3¢ | -4.5¢ to +16.1¢ | $+1.74 | collecting (21/100) |
| `tails` 30h | 14 | +4.9¢ | — | $+0.69 | collecting (14/100) |

## Daily reports

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
- [2026-11-12](paper/reports/2026-11-12.md)
- [2026-11-11](paper/reports/2026-11-11.md)
- [2026-11-10](paper/reports/2026-11-10.md)
- [2026-11-09](paper/reports/2026-11-09.md)
