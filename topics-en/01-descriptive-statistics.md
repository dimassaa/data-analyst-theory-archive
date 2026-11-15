# Descriptive statistics: mean, median, mode, variance, std. deviation, percentiles

🌐 [Русская версия](../topics/01-descriptive-statistics.md)

Descriptive statistics — a set of measures that briefly describe the **central tendency** and **spread** of data. This is the first thing an analyst computes when exploring a new dataset.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | What it shows | File |
|-------|---------------|------|
| Mean (arithmetic) | Center of mass of the data | [01-mean.md](01-mean.md) |
| Median | Middle of the ordered series | [01-median.md](01-median.md) |
| Mode | Most frequent value | [01-mode.md](01-mode.md) |
| Variance | Spread in squared units | [01-variance.md](01-variance.md) |
| Standard deviation | Typical deviation from the mean | [01-standard-deviation.md](01-standard-deviation.md) |
| Percentiles | Position relative to the rest | [01-percentiles.md](01-percentiles.md) |

---

## 📊 Comparison table of metrics

| Metric | What it shows | Sensitivity to outliers | Data type |
|--------|---------------|-------------------------|-----------|
| Mean | Center of mass of the data | High | Numeric |
| Median | Middle of the ordered series | Low | Numeric (ordinal) |
| Mode | Most frequent value | Low | Any (incl. categorical) |
| Variance | Spread in squared units | High | Numeric |
| Std. deviation | Typical deviation from the mean | High | Numeric |
| Percentiles | Position relative to the rest | Low | Numeric (ordinal) |

---

## ✅ Summary

To fully describe data, analysts usually look at **measures of central tendency** (mean, median, mode) and **measures of spread** (variance, standard deviation, quartiles, percentiles). When outliers are present, the median and percentiles are preferred; for symmetric distributions, the mean and standard deviation work well.

Related topics: [Quantiles and outliers (IQR)](10-iqr-quantiles-outliers.md) · [Correlation analysis](07-correlation-analysis.md)

Happy learning data analytics! 📊