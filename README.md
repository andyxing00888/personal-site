# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-24)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-11.47** over 1617 fills |
| 🔴 P&L / contract | -0.7¢ |
| Win rate | 74% |
| Profit factor | 0.95 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.72 |
| 🔴 Today | $-3.54 (100 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 416 runs / ~31h | rewards $14,285.02, fills $-34,437.20 (212639 settled, 49968.3 open) → **net $-20,152.18** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 343 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 2 | +22.0¢ | — | $+0.44 | collecting (2/100) |
| `fade_move` 18h | 44 | -0.2¢ | -15.7¢ to +17.1¢ | $-0.09 | collecting (44/100) |
| `fade_move` 24h | 46 | +3.7¢ | -10.5¢ to +18.6¢ | $+1.69 | collecting (46/100) |
| `fade_move` 30h | 37 | -1.3¢ | -15.6¢ to +13.6¢ | $-0.49 | collecting (37/100) |
| `fav_longshot` 18h | 248 | -3.1¢ | -9.7¢ to +2.7¢ | $-7.66 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 236 | +2.5¢ | -3.1¢ to +8.2¢ | $+5.88 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 245 | -1.0¢ | -6.5¢ to +4.7¢ | $-2.52 | no edge yet (CI spans 0) |
| `follow_move` 18h | 46 | -6.6¢ | -26.2¢ to +12.1¢ | $-3.04 | collecting (46/100) |
| `follow_move` 24h | 48 | -0.3¢ | -15.6¢ to +15.2¢ | $-0.14 | collecting (48/100) |
| `follow_move` 30h | 32 | -3.2¢ | -17.7¢ to +11.3¢ | $-1.02 | collecting (32/100) |
| `overround` 18h | 32 | +3.3¢ | -7.1¢ to +13.2¢ | $+1.05 | collecting (32/100) |
| `overround` 24h | 18 | -3.1¢ | -23.2¢ to +12.3¢ | $-0.56 | collecting (18/100) |
| `overround` 30h | 37 | -3.3¢ | -16.1¢ to +8.2¢ | $-1.22 | collecting (37/100) |
| `rv_updown_3c` 6h | 21 | -23.3¢ | -40.8¢ to -6.8¢ | $-4.89 | collecting (21/100) |
| `rv_updown_6c` 6h | 17 | -29.2¢ | -48.5¢ to -10.1¢ | $-4.96 | collecting (17/100) |
| `sell_longshot` 6h | 116 | -0.9¢ | -4.8¢ to +3.0¢ | $-1.09 | no edge yet (CI spans 0) |
| `sell_longshot` 12h | 10 | +7.8¢ | — | $+0.78 | collecting (10/100) |
| `sell_longshot_div` 6h | 142 | +1.3¢ | -4.7¢ to +6.2¢ | $+1.82 | no edge yet (CI spans 0) |
| `sell_longshot_div` 24h | 172 | -0.3¢ | -6.6¢ to +5.8¢ | $-0.45 | no edge yet (CI spans 0) |
| `tails` 18h | 25 | +3.2¢ | -10.7¢ to +14.9¢ | $+0.81 | collecting (25/100) |
| `tails` 24h | 23 | +9.7¢ | -2.5¢ to +16.4¢ | $+2.22 | collecting (23/100) |
| `tails` 30h | 19 | +8.8¢ | -1.9¢ to +15.7¢ | $+1.68 | collecting (19/100) |

## Daily reports

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
- [2026-11-11](paper/reports/2026-11-11.md)
