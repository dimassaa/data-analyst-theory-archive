# 📏 Standard deviation

🌐 [Русская версия](../topics/01-standard-deviation.md)

**Standard deviation** — the square root of the variance. It returns the spread in the same units of measurement as the data themselves.

**Formula:**
$$
s = \sqrt{s^2}
$$

**Example:**
From the previous example, variance = 650 → standard deviation = √650 ≈ **25.5 thousand RUB**

**Interpretation:**
This is the "typical" deviation from the mean. If the distribution is close to normal, about 68% of the data lie within ±1 standard deviation of the mean.

**Features:**
- The most popular measure of spread thanks to its understandable units.
- As sensitive to outliers as the mean.

**Key takeaway:** for data with outliers, prefer the IQR instead of the standard deviation (robust measure of spread).

---
← [Back to overview: Descriptive statistics](01-descriptive-statistics.md) · Related topics: [Variance](01-variance.md), [Standard error](14-confidence-intervals.md), [Outliers (IQR)](10-iqr-quantiles-outliers.md)