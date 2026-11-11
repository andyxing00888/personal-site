# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-11)

| Metric | Value |
|---|--:|
| 🟢 Total P&L | **$+16.89** over 613 fills |
| 🟢 P&L / contract | +2.8¢ |
| Win rate | 78% |
| Profit factor | 1.22 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | 7.31 |
| 🟢 Today | $+6.96 (80 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 192 runs / ~33h | rewards $5,681.21, fills $-8,946.24 (72971.9 settled, 35631.1 open) → **net $-3,265.03** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 157 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 191 runs | 12258 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `bump` 24h | 1 | +29.0¢ | — | $+0.29 | collecting (1/100) |
| `bump` 30h | 1 | +27.0¢ | — | $+0.27 | collecting (1/100) |
| `fade_move` 18h | 14 | +6.1¢ | — | $+0.85 | collecting (14/100) |
| `fade_move` 24h | 17 | -11.8¢ | -31.7¢ to +12.2¢ | $-2.01 | collecting (17/100) |
| `fade_move` 30h | 14 | -5.9¢ | — | $-0.82 | collecting (14/100) |
| `fav_longshot` 18h | 91 | +5.2¢ | -4.4¢ to +14.6¢ | $+4.71 | collecting (91/100) |
| `fav_longshot` 24h | 99 | +7.5¢ | -1.8¢ to +15.2¢ | $+7.47 | collecting (99/100) |
| `fav_longshot` 30h | 84 | +2.5¢ | -6.7¢ to +11.3¢ | $+2.08 | collecting (84/100) |
| `follow_move` 18h | 15 | -11.6¢ | -41.6¢ to +16.9¢ | $-1.74 | collecting (15/100) |
| `follow_move` 24h | 16 | +11.5¢ | -9.1¢ to +30.3¢ | $+1.84 | collecting (16/100) |
| `follow_move` 30h | 11 | +0.9¢ | — | $+0.10 | collecting (11/100) |
| `overround` 18h | 10 | +13.7¢ | — | $+1.37 | collecting (10/100) |
| `overround` 24h | 7 | -13.6¢ | — | $-0.95 | collecting (7/100) |
| `overround` 30h | 9 | +19.3¢ | — | $+1.74 | collecting (9/100) |
| `rv_updown_3c` 6h | 8 | -18.3¢ | — | $-1.46 | collecting (8/100) |
| `rv_updown_6c` 6h | 6 | -23.7¢ | — | $-1.42 | collecting (6/100) |
| `sell_longshot` 6h | 41 | +2.6¢ | -2.9¢ to +10.2¢ | $+1.08 | collecting (41/100) |
| `sell_longshot` 12h | 5 | +9.0¢ | — | $+0.45 | collecting (5/100) |
| `sell_longshot_div` 6h | 62 | +7.0¢ | +5.8¢ to +8.2¢ | $+4.37 | collecting (62/100) |
| `sell_longshot_div` 24h | 74 | -3.3¢ | -16.7¢ to +6.4¢ | $-2.44 | collecting (74/100) |
| `tails` 18h | 10 | -2.2¢ | — | $-0.22 | collecting (10/100) |
| `tails` 24h | 11 | +3.7¢ | — | $+0.41 | collecting (11/100) |
| `tails` 30h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |

## Daily reports

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
