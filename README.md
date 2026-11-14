# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-14)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-9.49** over 837 fills |
| 🔴 P&L / contract | -1.1¢ |
| Win rate | 74% |
| Profit factor | 0.93 |
| Max drawdown | -$26.38 |
| Sharpe (ann.) | -2.10 |
| 🔴 Today | $-2.51 (72 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 249 runs / ~32h | rewards $6,944.93, fills $-10,940.85 (80139.4 settled, 44090.8 open) → **net $-3,995.92** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 201 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 205 runs | 12928 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 23 | -1.3¢ | -18.7¢ to +20.7¢ | $-0.30 | collecting (23/100) |
| `fade_move` 24h | 24 | -4.7¢ | -22.6¢ to +13.9¢ | $-1.12 | collecting (24/100) |
| `fade_move` 30h | 19 | -10.5¢ | -27.5¢ to +8.1¢ | $-2.00 | collecting (19/100) |
| `fav_longshot` 18h | 133 | -3.5¢ | -12.4¢ to +4.9¢ | $-4.65 | no edge yet (CI spans 0) |
| `fav_longshot` 24h | 124 | +4.3¢ | -3.4¢ to +12.4¢ | $+5.38 | no edge yet (CI spans 0) |
| `fav_longshot` 30h | 118 | -4.3¢ | -13.8¢ to +4.8¢ | $-5.05 | no edge yet (CI spans 0) |
| `follow_move` 18h | 24 | -5.7¢ | -31.8¢ to +17.6¢ | $-1.37 | collecting (24/100) |
| `follow_move` 24h | 23 | +13.3¢ | -5.0¢ to +30.7¢ | $+3.05 | collecting (23/100) |
| `follow_move` 30h | 16 | +6.3¢ | -13.8¢ to +26.7¢ | $+1.01 | collecting (16/100) |
| `overround` 18h | 14 | +5.8¢ | — | $+0.81 | collecting (14/100) |
| `overround` 24h | 9 | -6.6¢ | — | $-0.59 | collecting (9/100) |
| `overround` 30h | 16 | -6.2¢ | -27.3¢ to +12.7¢ | $-0.99 | collecting (16/100) |
| `rv_updown_3c` 6h | 13 | -18.6¢ | — | $-2.42 | collecting (13/100) |
| `rv_updown_6c` 6h | 9 | -31.7¢ | — | $-2.85 | collecting (9/100) |
| `sell_longshot` 6h | 59 | -0.4¢ | -7.0¢ to +5.8¢ | $-0.23 | collecting (59/100) |
| `sell_longshot` 12h | 6 | +8.2¢ | — | $+0.49 | collecting (6/100) |
| `sell_longshot_div` 6h | 80 | +2.2¢ | -6.5¢ to +7.5¢ | $+1.77 | collecting (80/100) |
| `sell_longshot_div` 24h | 90 | -2.4¢ | -12.9¢ to +5.9¢ | $-2.20 | collecting (90/100) |
| `tails` 18h | 15 | -3.1¢ | -26.3¢ to +15.1¢ | $-0.47 | collecting (15/100) |
| `tails` 24h | 13 | +5.8¢ | — | $+0.76 | collecting (13/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

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
- [2026-11-01](paper/reports/2026-11-01.md)
