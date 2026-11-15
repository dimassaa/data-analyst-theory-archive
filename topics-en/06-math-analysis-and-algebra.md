# 📈 Mathematical analysis and algebra for the data analyst

🌐 [Русская версия](../topics/06-math-analysis-and-algebra.md)

The tools for working with numbers and data that are used in Excel, many analytics services, SQL and Python. Knowledge of these basic concepts is necessary for reading charts, interpreting metrics, performing calculations and implementing data analysis projects.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | File |
|------|------|
| Reading charts and graphs | [06-reading-charts.md](06-reading-charts.md) |
| Trends | [06-trends.md](06-trends.md) |
| Percentage change | [06-percentage-change.md](06-percentage-change.md) |
| Year-over-year (YoY) | [06-yoy.md](06-yoy.md) |
| Month-over-month (MoM) | [06-mom.md](06-mom.md) |
| Other change metrics | [06-other-change-metrics.md](06-other-change-metrics.md) |

---

## 📊 Groups of change metrics

| Comparison type | Example wording | Formula (increase) |
|----------------|----------------------|-------------------|
| Percentage change | "grew by 15%" | $ \frac{\text{new}-\text{old}}{\text{old}} \times 100 $ |
| YoY (year-over-year) | "revenue in October vs October last year" | $ \frac{Y_1 - Y_0}{Y_0} \times 100 $ |
| MoM (month-over-month) | "revenue in May vs April" | $ \frac{M_1 - M_0}{M_0} \times 100 $ |
| QoQ (quarter-over-quarter) | "revenue in Q2 vs Q1" | $ \frac{Q_1 - Q_0}{Q_0} \times 100 $ |

YoY removes seasonality, so it is preferred over MoM for business metrics with cyclicality.

---

## ✅ Summary

Percentage changes are measured with one and the same base formula, and the chosen comparison type (YoY, MoM, QoQ) depends on how you want to account for seasonality and the length of the business cycle. Trends and correct chart reading let you detect anomalies and patterns in the data faster.

Related topics: [Descriptive statistics](01-descriptive-statistics.md) · [Time series](27-time-series.md) · [Product metrics](08-product-metrics.md)

Good luck with your analysis! 📊