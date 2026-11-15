# 📏 Interquartile Range (IQR)

🌐 [Русская версия](../topics/10-iqr.md)

**IQR (Interquartile Range)** — the difference between the third and first quartiles. It shows the spread of the **middle 50%** of data.

**Formula:**
$$
\text{IQR} = Q3 - Q1
$$

**Example:**
Data: 2, 4, 6, 8, 10, 12, 14.
Q1 = 4, Q3 = 12.
IQR = 12 - 4 = **8**.

**Interpretation:**
- IQR shows the range in which the main (typical) values lie.
- The larger the IQR, the wider the spread of the data.
- Unlike the standard deviation, IQR is **not sensitive to outliers** (a single anomalous value will not change it much).

**What the IQR is used for:**
- Detecting **outliers** (the 1.5 × IQR rule, see [Outliers](10-outliers.md)).
- As an alternative to the standard deviation when the data is heavily skewed or contains outliers.
- Building a **box plot** (see [Box plot](10-box-plot.md)).

**Example:**
Data: 2, 4, 6, 8, 10, 12, 100 (outlier). Q1=4, Q3=12. IQR=8 (unchanged even though the outlier = 100).
Standard deviation would change significantly.

**Insight:** the IQR is a "robust" interquartile distance that gives information about the central part of the data. If the standard deviation is distorted by outliers, the IQR remains a reliable reference.

---
← [Back to overview: Quartiles, IQR, Outliers](10-iqr-quantiles-outliers.md) · Related topics: [Quartiles](10-quantiles-quartiles.md), [Box plot](10-box-plot.md), [Outliers](10-outliers.md)