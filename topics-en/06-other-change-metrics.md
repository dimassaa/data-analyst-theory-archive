# 🧮 Other change metrics

🌐 [Русская версия](../topics/06-other-change-metrics.md)

Besides percentage change, YoY and MoM, there are other metrics used to track dynamics.

**Absolute change:**
$$
\Delta = \text{new} - \text{old}
$$
Shows by how many units the value changed. For example, revenue grew by 15 thousand RUB.

**QoQ (Quarter-over-Quarter):**
$$
\text{QoQ (\%)} = \frac{\text{current quarter} - \text{previous quarter}}{\text{previous quarter}} \times 100
$$
Smooths out the noise that's present in MoM, but reacts to changes more slowly.

**WoW (Week-over-Week):**
$$
\text{WoW (\%)} = \frac{\text{current week} - \text{previous week}}{\text{previous week}} \times 100
$$
Used for operational monitoring (daily/weekly reports).

**Compound Annual Growth Rate (CAGR)** — the average annual growth rate:
$$
\text{CAGR} = \left( \frac{\text{final}}{\text{initial}} \right)^{\frac{1}{n}} - 1
$$
where n is the number of years. CAGR shows the average annual growth rate over the period, smoothing intermediate fluctuations.

**CAGR example:**
An investment grew from 100 thousand RUB to 200 thousand RUB over 2 years.
CAGR = (200/100)^(1/2) - 1 = √2 - 1 ≈ **41.4% per year**.

**Key takeaway:** CAGR is convenient for comparing long-term dynamics, while WoW/MoM/QoQ are for short-term monitoring. The choice of metric depends on the decision horizon: operational (day/week), monthly or strategic (year).

---
← [Back to overview: Mathematical analysis and algebra](06-math-analysis-and-algebra.md) · Related topics: [Month-over-month](06-mom.md), [Percentage change](06-percentage-change.md)