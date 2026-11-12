# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-12)

| Metric | Value |
|---|--:|
| 🟢 Total P&L | **$+8.19** over 676 fills |
| 🟢 P&L / contract | +1.2¢ |
| Win rate | 77% |
| Profit factor | 1.09 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | 2.70 |
| 🔴 Today | $-8.70 (63 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 209 runs / ~32h | rewards $5,972.69, fills $-10,270.99 (76156.9 settled, 34174.3 open) → **net $-4,298.30** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 168 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 16 | +7.8¢ | -14.8¢ to +34.8¢ | $+1.24 | collecting (16/100) |
| `fade_move` 24h | 19 | -4.8¢ | -26.7¢ to +20.6¢ | $-0.91 | collecting (19/100) |
| `fade_move` 30h | 14 | -5.9¢ | — | $-0.82 | collecting (14/100) |
| `fav_longshot` 18h | 105 | -1.0¢ | -10.9¢ to +7.8¢ | $-1.01 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 106 | +6.8¢ | -1.6¢ to +14.6¢ | $+7.22 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 94 | -1.4¢ | -11.1¢ to +7.4¢ | $-1.31 | collecting (94/100) |
| `follow_move` 18h | 18 | -15.7¢ | -43.0¢ to +12.4¢ | $-2.83 | collecting (18/100) |
| `follow_move` 24h | 19 | +12.9¢ | -8.3¢ to +31.9¢ | $+2.46 | collecting (19/100) |
| `follow_move` 30h | 11 | +0.9¢ | — | $+0.10 | collecting (11/100) |
| `overround` 18h | 10 | +13.7¢ | — | $+1.37 | collecting (10/100) |
| `overround` 24h | 9 | -6.6¢ | — | $-0.59 | collecting (9/100) |
| `overround` 30h | 13 | -3.6¢ | — | $-0.47 | collecting (13/100) |
| `rv_updown_3c` 6h | 10 | -12.9¢ | — | $-1.29 | collecting (10/100) |
| `rv_updown_6c` 6h | 6 | -23.7¢ | — | $-1.42 | collecting (6/100) |
| `sell_longshot` 6h | 47 | +3.6¢ | -1.9¢ to +10.1¢ | $+1.69 | collecting (47/100) |
| `sell_longshot` 12h | 5 | +9.0¢ | — | $+0.45 | collecting (5/100) |
| `sell_longshot_div` 6h | 62 | +7.0¢ | +5.8¢ to +8.2¢ | $+4.37 | collecting (62/100) |
| `sell_longshot_div` 24h | 81 | -2.5¢ | -14.7¢ to +6.8¢ | $-1.99 | collecting (81/100) |
| `tails` 18h | 11 | +0.4¢ | — | $+0.04 | collecting (11/100) |
| `tails` 24h | 11 | +3.7¢ | — | $+0.41 | collecting (11/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

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
