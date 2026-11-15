# 📐 Median

🌐 [Русская версия](../topics/01-median.md)

**Median** — the value that splits an ordered dataset exactly in half. Half of the observations are below the median, half are above.

**How to find it:**
1. Order the data in ascending order.
2. If the number of observations is odd, the median is the middle value.
3. If it is even, the median is the arithmetic mean of the two central values.

**Example (same salaries):**
Data: 30, 35, 40, 45, 100 → median = **40 thousand RUB**
With six values: 30, 35, 40, 45, 100, 120 → median = (40+45)/2 = **42.5 thousand RUB**

**Features:**
- Robust to outliers, so it often describes the "typical" value better under asymmetric distributions (e.g., income).
- Widely used together with quartiles and percentiles.

**Key takeaway:** with strongly skewed data, the median is a more honest measure of the "typical" value than the mean.

---
← [Back to overview: Descriptive statistics](01-descriptive-statistics.md) · Related topics: [Mean](01-mean.md), [Percentiles](01-percentiles.md), [Quartiles and IQR](10-iqr-quantiles-outliers.md)