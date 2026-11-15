# 🧩 Time series decomposition

🌐 [Русская версия](../topics/27-decomposition.md)

**Decomposition** is the splitting of a time series into components: trend, seasonality, and residual (noise).

**Model:**
$$
y_t = \text{trend}_t + \text{seasonality}_t + \text{residual}_t
$$
(additive model); a multiplicative one also exists: $ y_t = \text{trend} \times \text{seasonality} \times \text{residual} $.

**How it is done:**
1. Smooth the series (with a moving average) → trend.
2. Subtract the trend from the raw series → seasonal + noise.
3. Average over periods (months, days of the week) → seasonality.
4. Residual = raw series − trend − seasonality.

**Example:**
Retail revenue by month over 3 years.
Decomposition will reveal:
- an upward trend (the business is growing),
- seasonality (December peaks, January dips),
- a residual — weekly anomalies/events.

**Why decompose:**
- Understand the structure of a series before forecasting.
- Separate the metric's "seasonal" behavior from its "real" growth/decline.
- Detect anomalies: large residuals = points not explained by trend and seasonality — a reason to dig in.

**Key takeaway:** always decompose a metric before drawing conclusions about growth/decline. "January revenue is lower than December's" — that is seasonality, not a business decline.

---
← [Back to overview: Time series](27-time-series.md) · Related topics: [Moving averages](27-moving-averages.md), [Trends](06-trends.md), [ARIMA](27-arima.md)