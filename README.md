# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-20)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-10.11** over 1268 fills |
| 🔴 P&L / contract | -0.8¢ |
| Win rate | 75% |
| Profit factor | 0.95 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.71 |
| 🟢 Today | $+2.03 (89 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 349 runs / ~32h | rewards $10,414.83, fills $-20,067.05 (124764 settled, 60299.3 open) → **net $-9,652.22** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 285 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 29 | +6.2¢ | -12.3¢ to +25.3¢ | $+1.81 | collecting (29/100) |
| `fade_move` 24h | 35 | -1.1¢ | -15.9¢ to +15.8¢ | $-0.40 | collecting (35/100) |
| `fade_move` 30h | 30 | -10.6¢ | -23.8¢ to +3.9¢ | $-3.17 | collecting (30/100) |
| `fav_longshot` 18h | 191 | -3.6¢ | -11.4¢ to +3.8¢ | $-6.88 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 197 | +3.0¢ | -3.5¢ to +9.1¢ | $+5.86 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 192 | -1.3¢ | -8.0¢ to +5.6¢ | $-2.51 | no edge yet (CI spans 0) |
| `follow_move` 18h | 30 | -14.5¢ | -36.1¢ to +8.2¢ | $-4.36 | collecting (30/100) |
| `follow_move` 24h | 36 | +5.4¢ | -11.3¢ to +20.5¢ | $+1.95 | collecting (36/100) |
| `follow_move` 30h | 23 | +8.4¢ | -7.0¢ to +25.0¢ | $+1.94 | collecting (23/100) |
| `overround` 18h | 23 | +1.1¢ | -9.5¢ to +11.3¢ | $+0.26 | collecting (23/100) |
| `overround` 24h | 13 | -2.2¢ | — | $-0.29 | collecting (13/100) |
| `overround` 30h | 23 | -8.7¢ | -24.9¢ to +7.0¢ | $-2.01 | collecting (23/100) |
| `rv_updown_3c` 6h | 19 | -22.7¢ | -41.1¢ to -5.1¢ | $-4.31 | collecting (19/100) |
| `rv_updown_6c` 6h | 15 | -29.6¢ | -50.7¢ to -8.1¢ | $-4.44 | collecting (15/100) |
| `sell_longshot` 6h | 90 | -1.3¢ | -6.0¢ to +3.4¢ | $-1.20 | collecting (90/100) |
| `sell_longshot` 12h | 8 | +8.8¢ | — | $+0.70 | collecting (8/100) |
| `sell_longshot_div` 6h | 115 | +0.7¢ | -6.8¢ to +6.8¢ | $+0.84 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 145 | +1.7¢ | -4.8¢ to +7.2¢ | $+2.44 | no edge yet (CI spans 0) |
| `tails` 18h | 20 | +0.3¢ | -17.0¢ to +14.3¢ | $+0.05 | collecting (20/100) |
| `tails` 24h | 20 | +8.4¢ | -4.3¢ to +16.4¢ | $+1.69 | collecting (20/100) |
| `tails` 30h | 12 | +11.3¢ | — | $+1.36 | collecting (12/100) |

## Daily reports

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
- [2026-11-07](paper/reports/2026-11-07.md)
