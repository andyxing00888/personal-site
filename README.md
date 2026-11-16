# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-16)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-15.08** over 945 fills |
| 🔴 P&L / contract | -1.6¢ |
| Win rate | 73% |
| Profit factor | 0.90 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -3.01 |
| 🟢 Today | $+1.46 (42 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 282 runs / ~33h | rewards $7,965.75, fills $-13,783.68 (94571.3 settled, 50272.9 open) → **net $-5,817.93** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 234 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 26 | -0.1¢ | -18.1¢ to +20.2¢ | $-0.03 | collecting (26/100) |
| `fade_move` 24h | 27 | -7.1¢ | -23.2¢ to +11.0¢ | $-1.92 | collecting (27/100) |
| `fade_move` 30h | 20 | -7.6¢ | -24.0¢ to +10.0¢ | $-1.53 | collecting (20/100) |
| `fav_longshot` 18h | 154 | -5.0¢ | -13.0¢ to +3.4¢ | $-7.67 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 146 | +3.1¢ | -5.0¢ to +10.3¢ | $+4.50 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 139 | -5.2¢ | -13.5¢ to +3.1¢ | $-7.23 | no edge yet (CI spans 0) |
| `follow_move` 18h | 27 | -9.2¢ | -31.4¢ to +13.2¢ | $-2.49 | collecting (27/100) |
| `follow_move` 24h | 27 | +15.0¢ | -1.1¢ to +28.5¢ | $+4.05 | collecting (27/100) |
| `follow_move` 30h | 17 | +6.5¢ | -12.4¢ to +28.5¢ | $+1.10 | collecting (17/100) |
| `overround` 18h | 16 | +1.7¢ | -11.8¢ to +14.3¢ | $+0.27 | collecting (16/100) |
| `overround` 24h | 10 | -4.8¢ | — | $-0.48 | collecting (10/100) |
| `overround` 30h | 20 | -6.8¢ | -24.7¢ to +9.0¢ | $-1.37 | collecting (20/100) |
| `rv_updown_3c` 6h | 13 | -18.6¢ | — | $-2.42 | collecting (13/100) |
| `rv_updown_6c` 6h | 9 | -31.7¢ | — | $-2.85 | collecting (9/100) |
| `sell_longshot` 6h | 60 | -0.1¢ | -6.9¢ to +6.4¢ | $-0.09 | collecting (60/100) |
| `sell_longshot` 12h | 7 | +9.0¢ | — | $+0.63 | collecting (7/100) |
| `sell_longshot_div` 6h | 89 | +1.7¢ | -6.5¢ to +6.9¢ | $+1.47 | collecting (89/100) |
| `sell_longshot_div` 24h | 95 | -1.9¢ | -11.7¢ to +6.5¢ | $-1.78 | collecting (95/100) |
| `tails` 18h | 17 | -0.7¢ | -20.6¢ to +15.3¢ | $-0.12 | collecting (17/100) |
| `tails` 24h | 16 | +8.2¢ | -7.9¢ to +17.9¢ | $+1.31 | collecting (16/100) |
| `tails` 30h | 8 | +12.6¢ | — | $+1.01 | collecting (8/100) |

## Daily reports

- [2026-11-16](paper/reports/2026-11-16.md)
- [2026-11-15](paper/reports/2026-11-15.md)
- [2026-11-14](paper/reports/2026-11-14.md)
- [2026-11-13](paper/reports/2026-11-13.md)
- [2026-11-12](paper/reports/2026-11-12.md)
- [2026-11-11](paper/reports/2026-11-11.md)
- [2026-11-10](paper/reports/2026-11-10.md)
- [2026-11-09](paper/reports/2026-11-09.md)
- [2026-11-08](paper/reports/2026-11-08.md)
- [2026-11-07](paper/reports/2026-11-07.md)
- [2026-11-06](paper/reports/2026-11-06.md)
- [2026-11-05](paper/reports/2026-11-05.md)
- [2026-11-04](paper/reports/2026-11-04.md)
- [2026-11-03](paper/reports/2026-11-03.md)
