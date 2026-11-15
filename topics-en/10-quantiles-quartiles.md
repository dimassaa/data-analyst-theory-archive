# 📈 Quantiles and Quartiles

🌐 [Русская версия](../topics/10-quantiles-quartiles.md)

**Quantile** — the value below which a given proportion of observations lies.

**Special cases of quantiles:**
- **Median** = 50th quantile (Q2).
- **Quartiles**: Q1 = 25th quantile, Q3 = 75th quantile.
- **Deciles**: 10th, 20th, ..., 90th quantiles.
- **Percentiles**: the same as quantiles, expressed in percentages.

**How to compute quartile Q1 (the 25th quantile):**
1. Sort the data in ascending order.
2. Find the position: $ \text{position} = 0.25 \times (n+1) $.
3. If the position is an integer — take the value; if fractional — interpolate.

**Example:**
Data: 2, 4, 6, 8, 10, 12, 14.
- Q1: position = 0.25 × 8 = 2 → 2nd value = **4**.
- Q2 (median): position = 0.5 × 8 = 4 → 4th value = **8**.
- Q3: position = 0.75 × 8 = 6 → 6th value = **12**.

**Quartiles divide the data into four equal parts:**
- 25% of data < Q1,
- 50% of data < Q2 (median),
- 75% of data < Q3,
- 100% of data < Q3.

**Why quartiles are needed:**
- They describe the shape of a distribution without distortion from outliers.
- They underlie the calculation of IQR and box plots.
- They give quick intuition: if Q1=10, Q3=50, then the middle 50% of data lies in the range 10–50.

**Insight:** quartiles give a complete picture of a distribution even in the presence of outliers, unlike the mean and standard deviation, which can be "shifted" by anomalous values.

---
← [Back to overview: Quartiles, IQR, Outliers](10-iqr-quantiles-outliers.md) · Related topics: [IQR](10-iqr.md), [Box plot](10-box-plot.md), [Percentiles](01-percentiles.md)