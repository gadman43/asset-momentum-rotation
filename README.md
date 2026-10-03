# asset-momentum-rotation
7-Asset Momentum Rotation Strategy - Backtesting Results &amp; Analysis

## Momentum Warning Table (TradingView)

`momentum_warning_table.pine` (Pine Script v5, daily chart) adds a table grading SPMO and MTUM from 1 (healthy) to 5 (severe):

| Indicator | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Relative strength (ETF/SPY vs 20/50 SMA) | above both, 20 SMA rising | above 50, 20 SMA not rising | below one average | below both | below both, 20<50, new 60-day low within 5 bars |
| Trend / drawdown (252-day high) | DD<3%, above 50 SMA | DD 3-5% | DD 5-8% or close<50 SMA | DD 8-12% or 50 SMA falling | DD>12%, close<200 SMA, or 50<200 |
| Distribution / divergence (25 sessions, RSI 14) | 0-2 dist. days | 3 | 4 or bearish divergence | 5+ with divergence | 6+ or RSI<40 after divergence |

Composite = average of the six scores, held for 2+ bars: <2 full exposure, 2-3 watch, 3-4 reduce ~25%, >=4 reduce 50%+. Alerts fire on each level. Thresholds are inputs.

Note: thresholds are untuned; backtesting against past tops (2018 Q4, Feb 2020, 2022, 2024-25) has not been done.
