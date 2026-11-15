# 📈 Time series: moving averages, decomposition, ARIMA

🌐 [Русская версия](../topics/27-time-series.md)

**A time series** is a sequence of observations ordered in time (revenue by day, sales by week, traffic by hour). Time series analysis is the foundation of forecasting and anomaly monitoring.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Moving averages | Smoothing a series to find the trend | [27-moving-averages.md](27-moving-averages.md) |
| Series decomposition | Decomposition into trend, seasonality, and residual | [27-decomposition.md](27-decomposition.md) |
| ARIMA | Classical forecasting model | [27-arima.md](27-arima.md) |

---

## 📊 Comparison table

| Method | Type | Purpose | Complexity |
|--------|------|---------|------------|
| **Moving average** | Smoothing | Identify the trend, remove noise | Low |
| **Decomposition** | Decomposition | Split into trend + seasonality + residual | Medium |
| **ARIMA** | Forecasting model | Forecast future values | High |

**Key components of any series:**
- **Trend** — long-term direction.
- **Seasonality** — repeating patterns (weeks, months, holidays) (see [Trends](06-trends.md)).
- **Residual (noise)** — the irregular part.

---

## ✅ Summary

- Moving averages are the first tool for "cleaning" a series of noise.
- Decomposition helps you understand the structure of a series before modeling.
- ARIMA is a classical forecasting method, but it requires data preparation and stationarity checks.

Related topics: [Calculus and algebra](06-math-analysis-and-algebra.md) · [Percentage changes](06-percentage-change.md) · [Product metrics](08-product-metrics.md)

Happy forecasting! 📊