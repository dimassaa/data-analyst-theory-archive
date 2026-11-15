# 📈 Percentiles

🌐 [Русская версия](../topics/01-percentiles.md)

**Percentile** — a value below which a certain percentage of observations falls. For example, the 90th percentile is the value below which 90% of the data lie.

**Special cases:**
- **Median** = 50th percentile.
- **Quartiles**:
  - 1st quartile (Q1) = 25th percentile,
  - 2nd quartile (Q2) = median,
  - 3rd quartile (Q3) = 75th percentile.
- **Deciles** (every 10%) and others.

**How to compute:**
1. Sort the data in ascending order.
2. Find the rank: $ \text{rank} = \frac{p}{100} \times (n+1) $, where p is the percentile and n is the number of observations.
3. If the rank is an integer, take the corresponding value; if fractional, interpolate between the neighboring values.

**Example:**
Data: 2, 4, 6, 8, 10, 12, 14.
25th percentile: rank = 25/100 × 8 = 2 → 2nd value = **4**.
90th percentile: rank = 90/100 × 8 = 7.2 → interpolation between the 7th (14) and 8th (none) — we take 14.

**Features:**
- Robust to outliers and give a complete picture of the distribution.
- Widely used for comparison (e.g., "your income is higher than 80% of the population").
- The basis for building a box plot.

**Key takeaway:** percentiles are the most reliable way to describe a distribution in the presence of outliers and asymmetry.

---
← [Back to overview: Descriptive statistics](01-descriptive-statistics.md) · Related topics: [Median](01-median.md), [Quartiles and IQR](10-iqr-quantiles-outliers.md)