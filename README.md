# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-23)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-7.93** over 1517 fills |
| 🔴 P&L / contract | -0.5¢ |
| Win rate | 74% |
| Profit factor | 0.96 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.23 |
| 🟢 Today | $+2.83 (63 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 405 runs / ~31h | rewards $13,775.73, fills $-33,979.05 (207002 settled, 45186.7 open) → **net $-20,203.31** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 334 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 41 | +0.3¢ | -16.4¢ to +18.3¢ | $+0.13 | collecting (41/100) |
| `fade_move` 24h | 44 | +4.1¢ | -12.0¢ to +20.2¢ | $+1.82 | collecting (44/100) |
| `fade_move` 30h | 37 | -1.3¢ | -15.6¢ to +13.6¢ | $-0.49 | collecting (37/100) |
| `fav_longshot` 18h | 234 | -2.3¢ | -8.4¢ to +4.1¢ | $-5.33 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 228 | +2.8¢ | -3.0¢ to +8.7¢ | $+6.29 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 229 | -0.4¢ | -6.1¢ to +5.5¢ | $-0.98 | no edge yet (CI spans 0) |
| `follow_move` 18h | 43 | -5.7¢ | -25.3¢ to +13.4¢ | $-2.45 | collecting (43/100) |
| `follow_move` 24h | 46 | -0.5¢ | -16.2¢ to +13.9¢ | $-0.25 | collecting (46/100) |
| `follow_move` 30h | 31 | -4.0¢ | -18.5¢ to +11.5¢ | $-1.25 | collecting (31/100) |
| `overround` 18h | 31 | +2.5¢ | -8.1¢ to +12.3¢ | $+0.76 | collecting (31/100) |
| `overround` 24h | 18 | -3.1¢ | -23.2¢ to +12.3¢ | $-0.56 | collecting (18/100) |
| `overround` 30h | 33 | -3.3¢ | -18.0¢ to +9.2¢ | $-1.08 | collecting (33/100) |
| `rv_updown_3c` 6h | 21 | -23.3¢ | -40.8¢ to -6.8¢ | $-4.89 | collecting (21/100) |
| `rv_updown_6c` 6h | 17 | -29.2¢ | -48.5¢ to -10.1¢ | $-4.96 | collecting (17/100) |
| `sell_longshot` 6h | 94 | -1.0¢ | -5.7¢ to +3.4¢ | $-0.96 | collecting (94/100) |
| `sell_longshot` 12h | 9 | +8.3¢ | — | $+0.75 | collecting (9/100) |
| `sell_longshot_div` 6h | 130 | +1.5¢ | -4.7¢ to +6.8¢ | $+1.95 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 164 | -0.7¢ | -7.2¢ to +5.3¢ | $-1.11 | no edge yet (CI spans 0) |
| `tails` 18h | 24 | +2.2¢ | -13.0¢ to +13.7¢ | $+0.52 | collecting (24/100) |
| `tails` 24h | 22 | +9.0¢ | -3.5¢ to +16.2¢ | $+1.98 | collecting (22/100) |
| `tails` 30h | 18 | +8.1¢ | -3.7¢ to +15.4¢ | $+1.45 | collecting (18/100) |

## Daily reports

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
- [2026-11-11](paper/reports/2026-11-11.md)
- [2026-11-10](paper/reports/2026-11-10.md)
