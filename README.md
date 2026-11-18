# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-18)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-9.27** over 1085 fills |
| 🔴 P&L / contract | -0.9¢ |
| Win rate | 74% |
| Profit factor | 0.94 |
| Max drawdown | -$33.43 |
| Sharpe (ann.) | -1.67 |
| 🟢 Today | $+6.64 (75 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 313 runs / ~32h | rewards $8,899.56, fills $-13,978.95 (99599.6 settled, 75769.9 open) → **net $-5,079.39** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 256 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 26 | -0.1¢ | -18.1¢ to +20.2¢ | $-0.03 | collecting (26/100) |
| `fade_move` 24h | 31 | -5.7¢ | -21.2¢ to +11.1¢ | $-1.76 | collecting (31/100) |
| `fade_move` 30h | 27 | -7.0¢ | -20.7¢ to +7.6¢ | $-1.90 | collecting (27/100) |
| `fav_longshot` 18h | 162 | -3.7¢ | -12.3¢ to +4.5¢ | $-6.02 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 177 | +2.9¢ | -3.8¢ to +9.5¢ | $+5.17 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 165 | -3.3¢ | -10.5¢ to +4.6¢ | $-5.52 | no edge yet (CI spans 0) |
| `follow_move` 18h | 27 | -9.2¢ | -31.4¢ to +13.2¢ | $-2.49 | collecting (27/100) |
| `follow_move` 24h | 31 | +12.5¢ | -1.4¢ to +25.1¢ | $+3.86 | collecting (31/100) |
| `follow_move` 30h | 22 | +6.7¢ | -8.2¢ to +22.7¢ | $+1.48 | collecting (22/100) |
| `overround` 18h | 16 | +1.7¢ | -11.8¢ to +14.3¢ | $+0.27 | collecting (16/100) |
| `overround` 24h | 12 | -2.8¢ | — | $-0.34 | collecting (12/100) |
| `overround` 30h | 23 | -8.7¢ | -24.9¢ to +7.0¢ | $-2.01 | collecting (23/100) |
| `rv_updown_3c` 6h | 15 | -16.0¢ | -35.7¢ to +0.5¢ | $-2.40 | collecting (15/100) |
| `rv_updown_6c` 6h | 11 | -24.1¢ | — | $-2.65 | collecting (11/100) |
| `sell_longshot` 6h | 72 | -1.2¢ | -6.5¢ to +4.3¢ | $-0.87 | collecting (72/100) |
| `sell_longshot` 12h | 8 | +8.8¢ | — | $+0.70 | collecting (8/100) |
| `sell_longshot_div` 6h | 97 | +2.2¢ | -4.9¢ to +7.2¢ | $+2.17 | collecting (97/100) |
| `sell_longshot_div` 24h | 114 | -0.1¢ | -8.4¢ to +6.3¢ | $-0.17 | no edge yet (CI spans 0) |
| `tails` 18h | 18 | -0.3¢ | -19.7¢ to +14.6¢ | $-0.06 | collecting (18/100) |
| `tails` 24h | 19 | +7.9¢ | -5.4¢ to +15.9¢ | $+1.51 | collecting (19/100) |
| `tails` 30h | 10 | +12.3¢ | — | $+1.23 | collecting (10/100) |

## Daily reports

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
- [2026-11-05](paper/reports/2026-11-05.md)
