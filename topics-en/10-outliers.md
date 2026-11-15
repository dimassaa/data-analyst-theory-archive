# ⚠️ Outliers (anomalies)

🌐 [Русская версия](../topics/10-outliers.md)

**Outlier (anomaly)** — an observation that differs significantly from the rest of the data.

**Detection rule using the IQR:**
$$
\text{Outlier} = x_i \text{ such that } x_i < Q1 - 1.5 \times \text{IQR} \;\text{ or }\; x_i > Q3 + 1.5 \times \text{IQR}
$$

**Example:**
Q1=4, Q3=12, IQR=8.
Lower bound: 4 - 1.5×8 = 4 - 12 = -8.
Upper bound: 12 + 1.5×8 = 12 + 12 = 24.
All values > 24 or < -8 are outliers.

**Types of outliers:**
- **Data errors**: typos, system failures, duplicates.
- **Rare but real events**: fraud, large purchases, equipment failures.
- **Evidence of subgroups**: data from different groups is mixed, and an "outlier" for one group is normal for another.

**What to do with outliers:**
1. **Understand**: is it an error or a real phenomenon.
2. **Remove** (if it is an error or the goal of the analysis is typical behavior).
3. **Use robust methods**: median, IQR, Spearman — instead of mean, standard deviation, Pearson.
4. **Analyze separately**: if the outlier is an important segment (e.g., VIP customers).

**Insight:** outliers are not always the enemy. In fraud analytics, infrastructure monitoring, and risk assessment, outliers are exactly the data you need to find. Removing outliers without understanding their nature is a common mistake that destroys valuable information.

---
← [Back to overview: Quartiles, IQR, Outliers](10-iqr-quantiles-outliers.md) · Related topics: [IQR](10-iqr.md), [Box plot](10-box-plot.md), [Pearson Correlation](07-pearson-correlation.md)(outliers distort r)