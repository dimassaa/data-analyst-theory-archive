# 📌 Retention
🌐 [Русская версия](../topics/08-retention.md)

**Retention (retention rate)** — the share of customers (or users) who continue to use the product a certain time after their first contact.

**Classic cohort formula:**
$$
\text{Retention} = \frac{\text{number of cohort customers active in period} \; t}{\text{number of cohort customers at acquisition}} \times 100\%
$$

**Example:**
A cohort of 1000 users acquired in January. In February, 500 are active, in March — 400.
- Retention for the 1st month = 500/1000 = **50%**.
- Retention for the 2nd month = 400/1000 = **40%**.

**Retention formats:**
- **Cohort-based** — as in the example: anchor on a cohort and watch its dynamics.
- **Rolling/period-based** — the share of users active in the current period among those active in the previous one (close to 1 - churn).

**Why analyze retention:**
- It shows whether the user values the product (a product quality metric).
- False growth expectations: a high inflow of new users with low retention means a "leaky bucket".
- The basis for forecasting LTV and the stability of a subscription business.

**Cohort analysis is a great tool:**
- Comparing the retention curves of different cohorts shows whether the product has improved (see [Cohort analysis](09-cohort-analysis.md)).

**Insight:** retention is one of the most important product metrics. Even with active user acquisition, if retention is weak, traffic investments do not pay off — compensating for growth becomes pouring money into a "holey bucket".

---
← [Back to overview: Product metrics](08-product-metrics.md) · Related topics: [Churn rate](08-churn-rate.md), [Cohort analysis](09-cohort-analysis.md), [LTV](08-ltv.md)