# 🔄 Trends

🌐 [Русская версия](../topics/06-trends.md)

**Trend** — the general direction of a metric's movement over a long period (growth, decline, stabilization), stripped of short-term fluctuations and seasonality.

**Types of trends:**
- **Growth** — values increase over time.
- **Decline** — values decrease.
- **Flat (stabilization)** — values stay at roughly the same level.

**How to identify a trend:**
1. **Visually** — the line on the chart is smoothed (e.g., with a moving average, see [Moving averages](27-moving-averages.md)).
2. **Statistically** — linear regression on time: a significant, non-zero slope coefficient indicates a trend (see [Simple linear regression](15-simple-linear-regression.md)).

**How a trend differs from random fluctuations:**
- A metric fell in one month and grew in the next — that's not yet a trend.
- A trend is a sustained direction observed over a long horizon (several periods in a row).

**Example:**
Revenue has been growing for 12 months in a row — we note an upward trend. If revenue fluctuates around the mean without a direction — there is no trend (flat).

**Key takeaway:** before concluding "the metric is falling", make sure this is a trend and not one-off fluctuations. To do so, look at a long period and use smoothing methods that exclude seasonality.

---
← [Back to overview: Mathematical analysis and algebra](06-math-analysis-and-algebra.md) · Related topics: [Reading charts](06-reading-charts.md), [Moving averages](27-moving-averages.md), [Simple linear regression](15-simple-linear-regression.md)