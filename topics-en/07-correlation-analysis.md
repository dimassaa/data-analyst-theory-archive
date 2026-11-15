# 🔗 Correlation analysis: Pearson and Spearman correlation
🌐 [Русская версия](../topics/07-correlation-analysis.md)

**Correlation** is a statistical measure that shows the strength and direction of the relationship between two variables. It tells us **how** variables behave together (grow, fall, or are unrelated), but it does **not explain why** (causation is a separate question).

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Type of relationship | File |
|------|-----------|------|
| Pearson correlation coefficient | Linear, for quantitative data | [07-pearson-correlation.md](07-pearson-correlation.md) |
| Spearman's rank correlation | Monotonic, for ordinal data or non-linear relationships | [07-spearman-correlation.md](07-spearman-correlation.md) |

---

## 📊 Comparison table

| Characteristic | Pearson (r) | Spearman (ρ) |
|----------------|------------|-------------|
| **Type of relationship** | Linear | Monotonic (any) |
| **Data type** | Quantitative | Ordinal or quantitative with outliers |
| **Sensitivity to outliers** | High | Low |
| **Distribution requirement** | Approximately normal | None |
| **Sign interpretation** | +positive / −negative | +positive / −negative |

**Range of values:** from **-1** (perfect negative relationship) to **+1** (perfect positive relationship). A value of **0** means no linear relationship.

**Practical rule of choice:**
1. Data are quantitative, the relationship looks linear, and there are no strong outliers → **Pearson**.
2. Ordinal data, or the relationship is non-linear but monotonic, or there are outliers → **Spearman**.

---

## ⚠️ Critically important warning

**Correlation ≠ causation.** Two metrics may correlate, but the relationship may be caused by a third confounding (hidden) variable or just coincidence. For example, ice cream sales correlate with sales of hot drinks — not because of a direct relationship, but because of the weather (temperature).

Always check whether there is a reasonable explanation for the relationship before drawing conclusions.

---

## ✅ Summary

- **Pearson** — for linear relationships of quantitative variables (incl. in regression, factor analysis).
- **Spearman** — universal: works with any monotonic relationships, ranks, and outliers.
- Correlation shows the strength and direction of a relationship, but does not prove causation.

Related topics: [Covariance](16-covariance-and-anova.md) · [Linear regression basics](15-linear-regression.md) · [Outliers and IQR](10-iqr-quantiles-outliers.md)(outliers affect Pearson)

Good luck with your analysis! 📊