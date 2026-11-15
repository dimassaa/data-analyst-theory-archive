# 📊 Student's t-test

🌐 [Русская версия](../topics/04-t-test.md)

The **t-test** is used to compare mean values when the standard deviation of the population is **unknown** and is estimated from the sample.

**Types of t-test:**
1. **One-sample** — comparing the mean of a sample with a known value.
2. **Independent samples** — comparing the means of two unrelated groups.
3. **Paired (dependent)** — comparing the means of two related measurements (e.g., before and after treatment).

**Formula for independent samples (with equal variances):**
$$
t = \frac{\bar{x}_1 - \bar{x}_2}{s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}
$$
where $ s_p $ is the pooled standard deviation.

**Degrees of freedom:** $ df = n_1 + n_2 - 2 $.

**Conditions of use:**
- The data are approximately normally distributed (especially for small samples).
- For independent samples — independence of observations.

**Example:**
We test a new version of a website: control group (n₁=100, average conversion 10%, s₁=2%) and test group (n₂=100, average 12%, s₂=2%).
H₀: μ₁ = μ₂.
We compute t ≈ 7.07, p-value < 0.001 → we reject H₀; the difference is statistically significant.

**Key takeaway:** the t-test is robust to moderate deviations from normality for sufficiently large samples (n > 30). For strong skewness, it is better to use non-parametric alternatives (e.g., the Mann–Whitney U test).

---
← [Back to overview: Hypothesis testing](04-hypothesis-testing.md) · Related topics: [z-test](04-z-test.md), [Mann–Whitney](17-mann-whitney.md), [Confidence intervals](14-confidence-intervals.md)