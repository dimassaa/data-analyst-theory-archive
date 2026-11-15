# 🌊 Moving averages

🌐 [Русская версия](../topics/27-moving-averages.md)

**Moving average** is a method for smoothing a time series: at each point, the mean over a window of the previous k values is taken.

**Formula (simple moving average):**
$$
\text{MA}_t = \frac{x_t + x_{t-1} + \ldots + x_{t-k+1}}{k}
$$
where k is the window size.

**Example:**
Daily revenue: [10, 12, 11, 14, 13].
Moving average with window 3 for t=3: (10+12+11)/3 = 11; for t=4: (12+11+14)/3 ≈ 12.3.

**Types:**
- **Simple (SMA)** — equal weights.
- **Exponential (EMA)** — more weight on recent values (reflecting that the past has less influence).

**Why use it:**
- Remove "noise" and see the trend (see [Trends](06-trends.md)).
- Reduce the impact of individual outliers.
- A basis for trading signals and anomaly monitoring.

**How to choose the window k:**
- Small window → close to the raw data, more noise.
- Large window → a smoother line, but a "lag" in reacting to changes.
- For monthly data a window of 12 (months) is common; for daily data, 7 (weekly cycle).

**Key takeaway:** a moving average "lags" at turning points (smoothing of this kind "chases" the data). Don't rely on it alone to find breakpoints — combine it with other techniques (decomposition).

---
← [Back to overview: Time series](27-time-series.md) · Related topics: [Decomposition](27-decomposition.md), [Trends](06-trends.md)