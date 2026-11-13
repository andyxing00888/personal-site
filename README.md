# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-13)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-6.98** over 765 fills |
| 🔴 P&L / contract | -0.9¢ |
| Win rate | 75% |
| Profit factor | 0.94 |
| Max drawdown | -$23.87 |
| Sharpe (ann.) | -1.61 |
| 🔴 Today | $-15.17 (89 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 230 runs / ~32h | rewards $6,537.63, fills $-10,326.15 (78360.4 settled, 40908.2 open) → **net $-3,788.52** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 189 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 17 | +6.3¢ | -14.5¢ to +31.4¢ | $+1.07 | collecting (17/100) |
| `fade_move` 24h | 23 | -6.5¢ | -25.3¢ to +13.7¢ | $-1.49 | collecting (23/100) |
| `fade_move` 30h | 16 | -8.9¢ | -27.5¢ to +10.4¢ | $-1.43 | collecting (16/100) |
| `fav_longshot` 18h | 118 | -4.7¢ | -14.3¢ to +5.2¢ | $-5.56 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 117 | +4.2¢ | -3.8¢ to +12.1¢ | $+4.96 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 109 | -5.0¢ | -15.0¢ to +4.1¢ | $-5.40 | no edge yet (CI spans 0) |
| `follow_move` 18h | 19 | -14.1¢ | -39.0¢ to +11.5¢ | $-2.67 | collecting (19/100) |
| `follow_move` 24h | 23 | +13.3¢ | -5.0¢ to +30.7¢ | $+3.05 | collecting (23/100) |
| `follow_move` 30h | 14 | +1.4¢ | — | $+0.20 | collecting (14/100) |
| `overround` 18h | 12 | +5.5¢ | — | $+0.66 | collecting (12/100) |
| `overround` 24h | 9 | -6.6¢ | — | $-0.59 | collecting (9/100) |
| `overround` 30h | 14 | -3.0¢ | — | $-0.42 | collecting (14/100) |
| `rv_updown_3c` 6h | 11 | -9.7¢ | — | $-1.07 | collecting (11/100) |
| `rv_updown_6c` 6h | 7 | -22.3¢ | — | $-1.56 | collecting (7/100) |
| `sell_longshot` 6h | 54 | +2.6¢ | -2.4¢ to +8.2¢ | $+1.40 | collecting (54/100) |
| `sell_longshot` 12h | 6 | +8.2¢ | — | $+0.49 | collecting (6/100) |
| `sell_longshot_div` 6h | 73 | +3.0¢ | -6.5¢ to +7.8¢ | $+2.16 | collecting (73/100) |
| `sell_longshot_div` 24h | 88 | -2.8¢ | -12.8¢ to +5.8¢ | $-2.42 | collecting (88/100) |
| `tails` 18h | 13 | -4.6¢ | — | $-0.60 | collecting (13/100) |
| `tails` 24h | 13 | +5.8¢ | — | $+0.76 | collecting (13/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

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
- [2026-11-01](paper/reports/2026-11-01.md)
- [2026-10-31](paper/reports/2026-10-31.md)
