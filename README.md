# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-15)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-16.54** over 903 fills |
| 🔴 P&L / contract | -1.8¢ |
| Win rate | 73% |
| Profit factor | 0.89 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -3.42 |
| 🔴 Today | $-7.05 (66 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 263 runs / ~33h | rewards $7,382.68, fills $-11,062.42 (81653.3 settled, 48712.1 open) → **net $-3,679.74** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 215 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 26 | -0.1¢ | -18.1¢ to +20.2¢ | $-0.03 | collecting (26/100) |
| `fade_move` 24h | 24 | -4.7¢ | -22.6¢ to +13.9¢ | $-1.12 | collecting (24/100) |
| `fade_move` 30h | 20 | -7.6¢ | -24.0¢ to +10.0¢ | $-1.53 | collecting (20/100) |
| `fav_longshot` 18h | 148 | -6.1¢ | -14.9¢ to +2.6¢ | $-8.96 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 135 | +3.7¢ | -4.5¢ to +11.5¢ | $+4.97 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 134 | -5.7¢ | -14.0¢ to +2.9¢ | $-7.59 | no edge yet (CI spans 0) |
| `follow_move` 18h | 27 | -9.2¢ | -31.4¢ to +13.2¢ | $-2.49 | collecting (27/100) |
| `follow_move` 24h | 24 | +13.6¢ | -4.7¢ to +28.8¢ | $+3.26 | collecting (24/100) |
| `follow_move` 30h | 16 | +6.3¢ | -13.8¢ to +26.7¢ | $+1.01 | collecting (16/100) |
| `overround` 18h | 16 | +1.7¢ | -11.8¢ to +14.3¢ | $+0.27 | collecting (16/100) |
| `overround` 24h | 9 | -6.6¢ | — | $-0.59 | collecting (9/100) |
| `overround` 30h | 20 | -6.8¢ | -24.7¢ to +9.0¢ | $-1.37 | collecting (20/100) |
| `rv_updown_3c` 6h | 13 | -18.6¢ | — | $-2.42 | collecting (13/100) |
| `rv_updown_6c` 6h | 9 | -31.7¢ | — | $-2.85 | collecting (9/100) |
| `sell_longshot` 6h | 60 | -0.1¢ | -6.9¢ to +6.4¢ | $-0.09 | collecting (60/100) |
| `sell_longshot` 12h | 6 | +8.2¢ | — | $+0.49 | collecting (6/100) |
| `sell_longshot_div` 6h | 82 | +2.4¢ | -7.0¢ to +7.5¢ | $+1.93 | collecting (82/100) |
| `sell_longshot_div` 24h | 94 | -2.1¢ | -11.4¢ to +5.9¢ | $-1.94 | collecting (94/100) |
| `tails` 18h | 16 | -1.1¢ | -24.1¢ to +17.2¢ | $-0.18 | collecting (16/100) |
| `tails` 24h | 15 | +8.1¢ | -11.2¢ to +18.2¢ | $+1.21 | collecting (15/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

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
- [2026-11-02](paper/reports/2026-11-02.md)
