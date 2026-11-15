# 📈 Relative uplift

🌐 [Русская версия](../topics/21-relative-uplift.md)

**Relative uplift** is the percentage growth of a metric in the test group relative to the control group. It is the most intuitive way for business to describe an experiment's result.

**Formula:**
$$
\text{Uplift (\%)} = \frac{\text{test} - \text{control}}{\text{control}} \times 100
$$

**Example:**
Conversion in the control is 10%, in the test 11.5%.
Uplift = (11.5 - 10) / 10 × 100 = **+15%** (relative).

**Important distinctions:**
- +15% relative → 1.5 absolute percentage points (10% → 11.5%).
- Growth from 10% to 20% is **+100% relative** and **+10 p.p.**. Be precise in your wording so stakeholders aren't confused.

**Interpretation:**
- A positive uplift means the metric improved.
- A negative one means it worsened.
- 0% — no change.

**Difference from Cohen's d:**
- Uplift is understandable to any manager ("conversion grew by 12%").
- Cohen's d standardizes the difference (see [Cohen's d](21-cohens-d.md)) — more convenient for comparing with other studies.

**Key takeaway:** use (percentage) uplift when reporting to business, but always alongside a confidence interval and significance so the number is not just a "point" estimate. Also track absolute changes in p.p. where appropriate (low bases, where 100% is not that much).

---
← [Back to overview: Effect size](21-effect-size.md) · Related topics: [Cohen's d](21-cohens-d.md), [Statistical significance](05-statistical-significance.md), [Percentage change](06-percentage-change.md)