# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-25)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-12.36** over 1678 fills |
| 🔴 P&L / contract | -0.7¢ |
| Win rate | 74% |
| Profit factor | 0.95 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.82 |
| 🔴 Today | $-0.89 (61 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 433 runs / ~32h | rewards $14,851.39, fills $-36,170.87 (227223 settled, 52639.9 open) → **net $-21,319.48** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 355 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 44 | -0.2¢ | -15.7¢ to +17.1¢ | $-0.09 | collecting (44/100) |
| `fade_move` 24h | 50 | +5.3¢ | -9.9¢ to +18.7¢ | $+2.65 | collecting (50/100) |
| `fade_move` 30h | 37 | -1.3¢ | -15.6¢ to +13.6¢ | $-0.49 | collecting (37/100) |
| `fav_longshot` 18h | 256 | -2.8¢ | -9.1¢ to +3.4¢ | $-7.26 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 248 | +2.7¢ | -3.2¢ to +8.2¢ | $+6.67 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 249 | -1.4¢ | -7.1¢ to +4.4¢ | $-3.49 | no edge yet (CI spans 0) |
| `follow_move` 18h | 46 | -6.6¢ | -26.2¢ to +12.1¢ | $-3.04 | collecting (46/100) |
| `follow_move` 24h | 52 | -2.1¢ | -15.8¢ to +12.8¢ | $-1.11 | collecting (52/100) |
| `follow_move` 30h | 32 | -3.2¢ | -17.7¢ to +11.3¢ | $-1.02 | collecting (32/100) |
| `overround` 18h | 35 | +4.6¢ | -4.6¢ to +13.4¢ | $+1.60 | collecting (35/100) |
| `overround` 24h | 18 | -3.1¢ | -23.2¢ to +12.3¢ | $-0.56 | collecting (18/100) |
| `overround` 30h | 37 | -3.3¢ | -16.1¢ to +8.2¢ | $-1.22 | collecting (37/100) |
| `rv_updown_3c` 6h | 23 | -22.7¢ | -38.8¢ to -6.7¢ | $-5.21 | collecting (23/100) |
| `rv_updown_6c` 6h | 19 | -27.5¢ | -45.3¢ to -9.9¢ | $-5.22 | collecting (19/100) |
| `sell_longshot` 6h | 128 | -1.6¢ | -5.4¢ to +2.0¢ | $-2.11 | no edge yet (CI spans 0) |
| `sell_longshot` 12h | 11 | +8.0¢ | — | $+0.88 | collecting (11/100) |
| `sell_longshot_div` 6h | 149 | +0.9¢ | -4.5¢ to +5.7¢ | $+1.41 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 174 | -0.1¢ | -7.0¢ to +6.1¢ | $-0.19 | no edge yet (CI spans 0) |
| `tails` 18h | 25 | +3.2¢ | -10.7¢ to +14.9¢ | $+0.81 | collecting (25/100) |
| `tails` 24h | 23 | +9.7¢ | -2.5¢ to +16.4¢ | $+2.22 | collecting (23/100) |
| `tails` 30h | 19 | +8.8¢ | -1.9¢ to +15.7¢ | $+1.68 | collecting (19/100) |

## Daily reports

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
- [2026-11-12](paper/reports/2026-11-12.md)
