# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-19)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-12.14** over 1179 fills |
| 🔴 P&L / contract | -1.0¢ |
| Win rate | 75% |
| Profit factor | 0.93 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -2.12 |
| 🔴 Today | $-2.87 (94 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 331 runs / ~31h | rewards $9,708.24, fills $-19,897.99 (118877 settled, 60133.9 open) → **net $-10,189.75** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 267 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 26 | -0.1¢ | -18.1¢ to +20.2¢ | $-0.03 | collecting (26/100) |
| `fade_move` 24h | 32 | -3.8¢ | -18.7¢ to +14.1¢ | $-1.20 | collecting (32/100) |
| `fade_move` 30h | 28 | -8.4¢ | -22.6¢ to +6.0¢ | $-2.36 | collecting (28/100) |
| `fav_longshot` 18h | 177 | -3.8¢ | -11.9¢ to +3.6¢ | $-6.81 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 187 | +2.2¢ | -4.1¢ to +8.7¢ | $+4.10 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 183 | -2.0¢ | -9.1¢ to +5.5¢ | $-3.72 | no edge yet (CI spans 0) |
| `follow_move` 18h | 27 | -9.2¢ | -31.4¢ to +13.2¢ | $-2.49 | collecting (27/100) |
| `follow_move` 24h | 33 | +8.4¢ | -7.6¢ to +23.6¢ | $+2.77 | collecting (33/100) |
| `follow_move` 30h | 23 | +8.4¢ | -7.0¢ to +25.0¢ | $+1.94 | collecting (23/100) |
| `overround` 18h | 20 | -0.9¢ | -12.9¢ to +9.9¢ | $-0.18 | collecting (20/100) |
| `overround` 24h | 13 | -2.2¢ | — | $-0.29 | collecting (13/100) |
| `overround` 30h | 23 | -8.7¢ | -24.9¢ to +7.0¢ | $-2.01 | collecting (23/100) |
| `rv_updown_3c` 6h | 17 | -15.8¢ | -36.2¢ to +1.2¢ | $-2.68 | collecting (17/100) |
| `rv_updown_6c` 6h | 13 | -22.1¢ | — | $-2.87 | collecting (13/100) |
| `sell_longshot` 6h | 81 | -2.4¢ | -7.1¢ to +2.9¢ | $-1.95 | collecting (81/100) |
| `sell_longshot` 12h | 8 | +8.8¢ | — | $+0.70 | collecting (8/100) |
| `sell_longshot_div` 6h | 110 | +0.5¢ | -6.7¢ to +6.6¢ | $+0.52 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 127 | +0.7¢ | -6.8¢ to +6.5¢ | $+0.94 | no edge yet (CI spans 0) |
| `tails` 18h | 18 | -0.3¢ | -19.7¢ to +14.6¢ | $-0.06 | collecting (18/100) |
| `tails` 24h | 20 | +8.4¢ | -4.3¢ to +16.4¢ | $+1.69 | collecting (20/100) |
| `tails` 30h | 11 | +11.7¢ | — | $+1.29 | collecting (11/100) |

## Daily reports

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
- [2026-11-06](paper/reports/2026-11-06.md)
