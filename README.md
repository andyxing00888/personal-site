# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-17)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-15.91** over 1010 fills |
| 🔴 P&L / contract | -1.6¢ |
| Win rate | 73% |
| Profit factor | 0.90 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -3.09 |
| 🔴 Today | $-0.83 (65 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 295 runs / ~32h | rewards $8,339.80, fills $-13,729.54 (98611 settled, 57627.6 open) → **net $-5,389.74** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 243 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 26 | -0.1¢ | -18.1¢ to +20.2¢ | $-0.03 | collecting (26/100) |
| `fade_move` 24h | 30 | -7.8¢ | -23.1¢ to +9.4¢ | $-2.34 | collecting (30/100) |
| `fade_move` 30h | 24 | -7.3¢ | -22.8¢ to +8.2¢ | $-1.75 | collecting (24/100) |
| `fav_longshot` 18h | 161 | -4.0¢ | -12.1¢ to +4.3¢ | $-6.44 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 162 | +2.0¢ | -4.8¢ to +8.9¢ | $+3.25 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 153 | -5.4¢ | -13.5¢ to +2.8¢ | $-8.26 | no edge yet (CI spans 0) |
| `follow_move` 18h | 27 | -9.2¢ | -31.4¢ to +13.2¢ | $-2.49 | collecting (27/100) |
| `follow_move` 24h | 30 | +14.8¢ | +1.8¢ to +27.3¢ | $+4.45 | collecting (30/100) |
| `follow_move` 30h | 21 | +6.1¢ | -10.3¢ to +23.0¢ | $+1.28 | collecting (21/100) |
| `overround` 18h | 16 | +1.7¢ | -11.8¢ to +14.3¢ | $+0.27 | collecting (16/100) |
| `overround` 24h | 10 | -4.8¢ | — | $-0.48 | collecting (10/100) |
| `overround` 30h | 21 | -10.7¢ | -28.0¢ to +4.5¢ | $-2.24 | collecting (21/100) |
| `rv_updown_3c` 6h | 13 | -18.6¢ | — | $-2.42 | collecting (13/100) |
| `rv_updown_6c` 6h | 9 | -31.7¢ | — | $-2.85 | collecting (9/100) |
| `sell_longshot` 6h | 60 | -0.1¢ | -6.9¢ to +6.4¢ | $-0.09 | collecting (60/100) |
| `sell_longshot` 12h | 8 | +8.8¢ | — | $+0.70 | collecting (8/100) |
| `sell_longshot_div` 6h | 89 | +1.7¢ | -6.5¢ to +6.9¢ | $+1.47 | collecting (89/100) |
| `sell_longshot_div` 24h | 103 | -0.9¢ | -9.4¢ to +6.2¢ | $-0.94 | no edge yet (CI spans 0) |
| `tails` 18h | 18 | -0.3¢ | -19.7¢ to +14.6¢ | $-0.06 | collecting (18/100) |
| `tails` 24h | 18 | +7.9¢ | -6.4¢ to +16.4¢ | $+1.42 | collecting (18/100) |
| `tails` 30h | 9 | +12.0¢ | — | $+1.08 | collecting (9/100) |

## Daily reports

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
- [2026-11-05](paper/reports/2026-11-05.md)
- [2026-11-04](paper/reports/2026-11-04.md)
