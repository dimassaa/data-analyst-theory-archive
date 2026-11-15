# 📊 Product metrics: LTV, CAC, Retention, Churn, ROI, ROMI, ARPU
🌐 [Русская версия](../topics/08-product-metrics.md)

Product metrics help evaluate the effectiveness of a product and marketing, the unit economics, and the overall health of the business. Understanding them is essential for making investment decisions, prioritization, and optimization.

This is an overview page (hub): each metric has its own file.

---

## 🧭 Topics overview

| Metric | What it shows | File |
|---------|----------------|------|
| **LTV** (Lifetime Value) | How much money a customer brings over their entire lifetime | [08-ltv.md](08-ltv.md) |
| **CAC** (Cost of Acquisition) | How much it costs to acquire one customer | [08-cac.md](08-cac.md) |
| **Retention** | The share of customers who stay with the product | [08-retention.md](08-retention.md) |
| **Churn rate** | The share of customers who leave over a period | [08-churn-rate.md](08-churn-rate.md) |
| **ROI** | The ratio of profit to invested funds | [08-roi.md](08-roi.md) |
| **ROMI** | The ratio of marketing profit to marketing costs | [08-romi.md](08-romi.md) |
| **ARPU** | Average revenue per user | [08-arpu.md](08-arpu.md) |

---

## 📊 Comparison table

| Metric | Formula | Period | Question it answers |
|---------|---------|--------|------------------------------|
| **LTV** | Total revenue from a customer / number of customers | Entire customer lifetime | How much one customer brings in total |
| **CAC** | Marketing costs / number of acquired customers | Campaign period | How much acquisition costs |
| **Retention** | (Active in period t) / (active earlier) | Month/week | Do users stay |
| **Churn rate** | Customers who left / all customers over the period | Month/quarter | How many customers we lose |
| **ROI** | (Revenue - costs) / costs | Project/campaign | Did the investment pay off |
| **ROMI** | (Marketing revenue - marketing costs) / costs | Campaign/period | Does marketing pay off |
| **ARPU** | Revenue / number of users | Month | Average revenue per user |

**Basic unit economics check:**
$$
\text{profit per customer} \approx \text{LTV} - \text{CAC}
$$
If LTV > CAC — the business earns on the customer; if not — money "burns up" on acquisition.

---

## ✅ Summary

- Metrics are divided into **economic** (LTV, CAC, ROI, ROMI, ARPU) and **behavioral** (Retention, Churn).
- Economic metrics are linked: ARPU affects LTV, and CAC is compared with LTV.
- Retention and Churn are the "basis" for forecasting LTV and the stability of a subscription business.

Analyze metrics together: revenue growth without accounting for churn/retention can mask problems.

Related topics: [Funnels and cohorts](09-funnels-and-cohorts.md) · [A/B test economics](05-ab-testing.md) · [Effect size](21-effect-size.md)

Good luck with product analytics! 📈