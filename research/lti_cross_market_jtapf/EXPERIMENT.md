# Cross-market JTAPF experiment

This branch runs a controlled out-of-sample study of stale daily prices in the United States, Taiwan, Japan, and China.

## Design

- Daily adjusted OHLCV from 2012-01-01 through 2026-08-06, downloaded at run time.
- Up to 12 securities per market after a minimum-history screen.
- 60% training / 40% testing split.
- Selection, threshold-censoring, and mixed non-trading mechanisms.
- Target non-trading rates: 10%, 20%, and 40%.
- Two paired replications per stock/mechanism/rate.
- Baselines: LOCF, liquidity-adaptive factor Kalman filter, and ex-post interpolation.
- Proposed model: joint trade-arrival/latent-price particle filter (JTAPF).

## Applications

The evaluation covers latent-price and moving-average reconstruction, one- and five-day truly out-of-sample forecasting, MA(5,20) signal fidelity, and long/cash trading performance at 0, 10, 25, and 50 basis-point one-way costs. Signals are lagged and changes in position are permitted only on observable synthetic trading days.
