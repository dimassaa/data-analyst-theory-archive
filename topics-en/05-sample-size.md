# 🧮 Sample size for an A/B test

🌐 [Русская версия](../topics/05-sample-size.md)

Sample size is the number of users in each group needed to detect an effect of a chosen size with a given level of confidence.

**What it depends on:**
- **Significance level (α)** — smaller α → larger sample needed.
- **Power (1-β)** — more power → larger sample needed.
- **MDE (minimal detectable effect)** — the smaller the effect that needs to be caught → larger sample needed.
- **Metric variance (σ)** — more spread → larger sample needed.

**Formula for comparing proportions (conversions):**
$$
n = \frac{(z_{1-\alpha/2} + z_{1-\beta})^2 \cdot (p_1(1-p_1) + p_2(1-p_2))}{(p_2 - p_1)^2}
$$
where $ p_1 $ and $ p_2 $ are the baseline and expected conversion rates.

**Example:**
Baseline conversion is 10%, and we want to detect an improvement to 12% (a 20% relative increase).
With α=0.05 and 80% power (z-values 1.96 and 0.84):
numerator = (1.96+0.84)² × (0.1×0.9 + 0.12×0.88) ≈ 7.84 × 0.1956 ≈ 1.53
denominator = (0.02)² = 0.0004
n ≈ 1.53 / 0.0004 ≈ **3825 users per group** (≈ 7650 in total).

Sometimes the pooled sample size for both groups is calculated, so it's important to understand that n in the formula is usually the size of **each** group.

**Key takeaway:** the smaller the effect to detect, the larger the sample needed. If the MDE is very small (e.g., +1%), the sample size can turn out to be practically unattainable — it's worth thinking about whether such a small increase really matters to the business.

---
← [Back to overview: A/B testing](05-ab-testing.md) · Related topics: [Test duration](05-test-duration.md), [Statistical power](05-test-power.md), [Statistical significance](05-statistical-significance.md)