# 🤖 ARIMA

🌐 [Русская версия](../topics/27-arima.md)

**ARIMA (AutoRegressive Integrated Moving Average)** is a classical statistical model for time series forecasting. It combines autocorrelation, integration (differencing), and moving average.

**What it stands for:**
- **AR** (autoregression): the future value depends on previous values.
- **I** (integration): the series is made stationary through differencing.
- **MA** (moving average): accounts for past forecast errors.

**Notation ARIMA(p, d, q):**
- **p** — the order of autoregression (the number of y lags used in the forecast).
- **d** — the order of differencing (how many times differences were taken to achieve stationarity).
- **q** — the order of the moving average of errors.

**Model example:** ARIMA(1,1,1) — one autoregression lag, one differencing for stationarity, one error lag.

**How to choose the parameters:**
- The (p, d, q) are selected using ACF/PACF plots and information criteria (AIC/BIC).
- Automatic selection is often used (auto-ARIMA in libraries).

**Prerequisite — stationarity:**
The series must be stationary (mean and variance constant over time). Non-stationarity is removed with differencing (the I part) or transformations (logarithms).

**Limitations:**
- A linear model — reflects nonlinear patterns poorly.
- Doesn't handle complex seasonality without extensions (SARIMA for seasonality).
- Requires a sufficiently long history.

**Key takeaway:** ARIMA is a good "starting" benchmark for forecasting [and machine-learning models (LSTM, XGBoost) are compared precisely against it]. For seasonal business metrics, first look at the decomposition (see [Decomposition](27-decomposition.md)), then apply SARIMA.

---
← [Back to overview: Time series](27-time-series.md) · Related topics: [Decomposition](27-decomposition.md), [Moving averages](27-moving-averages.md), [Trends](06-trends.md)