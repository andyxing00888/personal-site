# Kalshi paper trading

Forward test of Kalshi strategies: forecast-free rules on weather, econ and a diversified non-sports basket (rules in [strategies.py](paper/strategies.py)), plus the experiments below.

## Summary (as of 2026-11-07)

| Metric | Value |
|---|--:|
| 🔴 Total P&L | **$-6.26** over 342 fills |
| 🔴 P&L / contract | -1.8¢ |
| Win rate | 74% |
| Profit factor | 0.88 |
| Max drawdown | -$9.03 |
| Sharpe (ann.) | -6.34 |
| 🟢 Today | $+0.06 (36 fills) |

Full dashboard: https://functionalleaf.github.io/kalshi-weather/

## Other experiments

| Experiment | Data | Status |
|---|--:|--:|
| Liquidity rewards (`lip.py`), 300/side on watchlist | 118 runs / ~28h | rewards $3,690.55, fills $-3,786.15 (36968.5 settled, 37552.9 open) → **net $-95.61** |
| S&P/Nasdaq cross-series arb (`consistency.py`) | 95 runs | 0 arbs after fees, best edge -1.0¢ |
| Kalshi vs Polymarket sports (`xvenue.py`) | 117 runs | 8090 team quotes, 0 buy-Kalshi arbs after fees |

## Scoreboard

| Strategy | Fills | P&L / contract | 95% CI | Total | Verdict |
|---|--:|--:|--:|--:|--:|
| `fade_move` 18h | 7 | +13.1¢ | — | $+0.92 | collecting (7/100) |
| `fade_move` 24h | 12 | -13.4¢ | — | $-1.61 | collecting (12/100) |
| `fade_move` 30h | 7 | -11.6¢ | — | $-0.81 | collecting (7/100) |
| `fav_longshot` 18h | 42 | -5.6¢ | -20.8¢ to +9.2¢ | $-2.37 | collecting (42/100) |
| `fav_longshot` 24h | 61 | +4.0¢ | -9.3¢ to +17.1¢ | $+2.45 | collecting (61/100) |
| `fav_longshot` 30h | 42 | -10.6¢ | -23.5¢ to +4.0¢ | $-4.47 | collecting (42/100) |
| `follow_move` 18h | 7 | -14.0¢ | — | $-0.98 | collecting (7/100) |
| `follow_move` 24h | 12 | +8.1¢ | — | $+0.97 | collecting (12/100) |
| `follow_move` 30h | 3 | -2.3¢ | — | $-0.07 | collecting (3/100) |
| `overround` 18h | 3 | +8.3¢ | — | $+0.25 | collecting (3/100) |
| `overround` 24h | 3 | -21.3¢ | — | $-0.64 | collecting (3/100) |
| `overround` 30h | 2 | +28.5¢ | — | $+0.57 | collecting (2/100) |
| `rv_updown_3c` 6h | 4 | -28.0¢ | — | $-1.12 | collecting (4/100) |
| `rv_updown_6c` 6h | 3 | -37.7¢ | — | $-1.13 | collecting (3/100) |
| `sell_longshot` 6h | 23 | +1.3¢ | -7.4¢ to +11.5¢ | $+0.31 | collecting (23/100) |
| `sell_longshot` 12h | 2 | +7.5¢ | — | $+0.15 | collecting (2/100) |
| `sell_longshot_div` 6h | 49 | +6.4¢ | +5.0¢ to +7.5¢ | $+3.14 | collecting (49/100) |
| `sell_longshot_div` 24h | 44 | -2.5¢ | -21.0¢ to +9.5¢ | $-1.09 | collecting (44/100) |
| `tails` 18h | 7 | -11.9¢ | — | $-0.83 | collecting (7/100) |
| `tails` 24h | 6 | -5.3¢ | — | $-0.32 | collecting (6/100) |
| `tails` 30h | 3 | +14.0¢ | — | $+0.42 | collecting (3/100) |

## Daily reports

- [2026-11-07](paper/reports/2026-11-07.md)
- [2026-11-06](paper/reports/2026-11-06.md)
- [2026-11-05](paper/reports/2026-11-05.md)
- [2026-11-04](paper/reports/2026-11-04.md)
- [2026-11-03](paper/reports/2026-11-03.md)
- [2026-11-02](paper/reports/2026-11-02.md)
- [2026-11-01](paper/reports/2026-11-01.md)
- [2026-10-31](paper/reports/2026-10-31.md)
