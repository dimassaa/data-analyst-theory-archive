# 📅 Month-over-month (MoM)

🌐 [Русская версия](../topics/06-mom.md)

**MoM (month-over-month)** — comparing a metric with the previous month. Shows the short-term dynamics of the metric.

**Formula:**
$$
\text{MoM (\%)} = \frac{\text{current month} - \text{previous month}}{\text{previous month}} \times 100
$$

**Example:**
Revenue in May is 420 thousand RUB, in April 400 thousand RUB.
MoM = (420-400)/400 × 100 = **+5%**.

**Analogues for other periods:**
- **WoW (week-over-week)** — comparison with the previous week. Often used for operational monitoring.
- **QoQ (quarter-over-quarter)** — for a more stable picture than MoM.

**Limitations of MoM:**
- Highly subject to **seasonality**: comparing January with December is meaningless for New Year retail, and February with January for fitness clubs.
- Volatile months can be misleading.

**When MoM is useful:**
- Monitoring rapid changes (launching new features, traffic channels).
- Product metrics (ARPU, retention) where a quick reaction is needed.

**Key takeaway:** when comparing with the previous month, always check whether the change is related to seasonality. If there is annual cyclicality, use YoY as the main measure and MoM for operational monitoring.

---
← [Back to overview: Mathematical analysis and algebra](06-math-analysis-and-algebra.md) · Related topics: [Year-over-year](06-yoy.md), [Percentage change](06-percentage-change.md)