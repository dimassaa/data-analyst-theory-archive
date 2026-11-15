# 📊 Quartiles, IQR and Outliers

🌐 [Русская версия](../topics/10-iqr-quantiles-outliers.md)

Quartiles, the interquartile range (IQR) and outliers are tools for describing data distributions and detecting anomalies. These metrics are **robust to outliers** (unlike the mean and standard deviation) and are therefore especially useful with real data, which almost always contains anomalies.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic                        | Key idea                            | File                                                   |
| --------------------------- | -------------------------------------- | ------------------------------------------------------ |
| Quantiles and quartiles     | Dividing data into shares | [10-quantiles-quartiles.md](10-quantiles-quartiles.md) |
| Interquartile range (IQR) | Robust measure of spread               | [10-iqr.md](10-iqr.md)                                 |
| Box plot     | Visual representation of a distribution | [10-box-plot.md](10-box-plot.md)                       |
| Outliers                     | Detecting and handling anomalies       | [10-outliers.md](10-outliers.md)                       |

---

## 📊 Comparison table

| Concept | What it shows | Formula / rule | Robustness to outliers |
|---------|----------------|-------------------|------------------------|
| **Quantiles** | The value below which p% of data lie | Sorting + interpolation | ✓ High |
| **Quartiles (Q1, Q2, Q3)** | 25%, 50%, 75% quantiles | Similarly | ✓ High |
| **IQR** | Spread of the middle 50% | $ Q3 - Q1 $ | ✓ High |
| **Box plot** | Visual of a distribution | Q1, Q3, whiskers, outliers | ✓ Visual |
| **Outliers** | Anomalous values | Beyond Q1-1.5·IQR or Q3+1.5·IQR | Depends on the rule |

**How they are related:**
1. First the **quartiles** are computed (Q1, Q2=median, Q3).
2. From the quartiles the **IQR** is calculated (the spread of the middle 50%).
3. The IQR is used to build a **box plot** and detect **outliers**.

---

## ✅ Summary

- Quartiles give a complete picture of a distribution without distortion from outliers.
- IQR is a robust alternative to the standard deviation for assessing spread.
- Box plot is a clear tool for quickly comparing the distributions of several groups.
- Outliers are not always errors: sometimes they are crucial data (fraud, system failures, superusers).

Related topics: [Descriptive Statistics](01-descriptive-statistics.md) · [Percentiles](01-percentiles.md) · [Pearson Correlation](07-pearson-correlation.md)(outliers affect r)

Good luck with your anomaly analysis! 📈