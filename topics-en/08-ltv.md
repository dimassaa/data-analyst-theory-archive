# 💰 LTV (Lifetime Value)
🌐 [Русская версия](../topics/08-ltv.md)

**LTV (Lifetime Value)** — the total profit (or revenue) a customer brings to the company over their entire interaction (life cycle).

**Formula (basic):**
$$
\text{LTV} = \text{ARPU} \times \text{expected customer lifetime}
$$
Expected lifetime: $ \frac{1}{\text{churn rate}} $ (for subscription services).

**Refined formula accounting for gross margin:**
$$
\text{LTV} = \text{ARPU} \times \text{margin} \times \frac{1}{\text{churn}}
$$

**Example:**
A subscription service: average monthly payment 1000 RUB, churn = 5% per month.
Expected lifetime = 1/0.05 = 20 months.
LTV = 1000 × 20 = **20,000 RUB.**

**What LTV depends on:**
- Price level (ARPU).
- Customer retention (churn, retention).
- Additional sales (cross-sell, up-sell).
- Profit margin.

**How LTV is increased:**
- Improving the product and service quality (growth of retention).
- Loyalty programs, subscriptions.
- Upsells and expanding the product line.

**Insight:** LTV is a key metric for estimating acceptable acquisition costs. If LTV > CAC, the unit economics works and the business can scale. NPS, segmentation, and cohort analysis help understand which customer groups have higher LTV.

---
← [Back to overview: Product metrics](08-product-metrics.md) · Related topics: [CAC](08-cac.md), [ARPU](08-arpu.md), [Churn](08-churn-rate.md), [Retention](08-retention.md)