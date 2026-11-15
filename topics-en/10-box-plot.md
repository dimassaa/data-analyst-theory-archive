# 📦 Box Plot

🌐 [Русская версия](../topics/10-box-plot.md)

**Box plot** — a graphical representation of a distribution showing key statistics: the median, quartiles, range, and outliers.

**Elements of a box plot:**
- **Box**: from Q1 to Q3 (contains 50% of data).
- **Line inside the box**: the median (Q2).
- **Whiskers**: extend to the last value not exceeding Q3 + 1.5 × IQR (upper whisker) and not below Q1 - 1.5 × IQR (lower whisker).
- **Points beyond the whiskers**: outliers.

**Example visualization (text representation):**
```
         ┌─────────┐
  |──────┤    |    ├──────|    ●   ●
         └─────────┘
  ←─ whisker ─→ ←─ box ─→ ←─ whisker ─→   outliers
```

**Why a box plot is needed:**
- Assess the **center**, **spread**, **symmetry**, and **presence of outliers** at a glance.
- Convenient for comparing the distributions of several groups (side-by-side box plots).
- More informative than just mean + standard deviation.

**Comparing distributions:**
- A wide box → large spread of data.
- Median shifted toward the edge of the box → skewness.
- Many points beyond the whiskers → the data contains outliers.

**Insight:** the box plot is the best tool for quickly comparing several groups (e.g., conversion by channel). It shows the center, the spread, and the anomalies at the same time.

---
← [Back to overview: Quartiles, IQR, Outliers](10-iqr-quantiles-outliers.md) · Related topics: [Quartiles](10-quantiles-quartiles.md), [IQR](10-iqr.md), [Outliers](10-outliers.md)