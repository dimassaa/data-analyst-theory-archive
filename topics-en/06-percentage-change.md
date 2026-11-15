# ➗ Percentage change

🌐 [Русская версия](../topics/06-percentage-change.md)

**Percentage change** is a relative measure of a change in a value, showing by what percentage the value grew or fell relative to the original.

**Formula:**
$$
\text{Increase (\%)} = \frac{\text{new} - \text{old}}{\text{old}} \times 100
$$

**Interpretation rules:**
- A positive result → growth.
- A negative result → decline.
- A result of 0 → the value did not change.

**Example 1 (growth):**
Revenue in January is 100 thousand RUB, in February 115 thousand RUB.
Increase = (115-100)/100 × 100 = **+15%**.

**Example 2 (decline):**
Revenue in March is 120 thousand RUB, in April 90 thousand RUB.
Increase = (90-120)/120 × 100 = **-25%**.

**Division by zero:**
If the old value is equal to 0, the formula doesn't work (division by zero). In that case the increase is formally infinite, but such a situation should be flagged separately.

**Common mistakes:**
- Symmetry: a 50% increase and a 50% decrease do **not** return to the original value. 100 → +50% → 150 → -50% → 75.
- Confusion between percentage points (p.p.) and percent: growth from 10% to 15% is an increase of **5 p.p.**, not 5% (relatively it's +50%).

**Key takeaway:** always clarify what the change is measured in: percent (relative) or percentage points (absolute) — they give different numbers.

---
← [Back to overview: Mathematical analysis and algebra](06-math-analysis-and-algebra.md) · Related topics: [Year-over-year](06-yoy.md), [Month-over-month](06-mom.md)