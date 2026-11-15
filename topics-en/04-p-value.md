# 📉 p-value

🌐 [Русская версия](../topics/04-p-value.md)

**p-value** is the probability of obtaining the observed value of the statistic (or a more extreme one) if the null hypothesis is true.

**Interpretation:**
- A small p-value (usually < 0.05) means that the data are unlikely under H₀, so H₀ is rejected.
- A large p-value means that the data are consistent with H₀; there is no basis for rejection.

**Example:**
We check whether the average salary in group A differs from group B.
H₀: the means are equal.
We obtained p-value = 0.03. This means: if the means really were equal, the probability of seeing such a difference (or larger) is 3%. Since this is less than 0.05, we reject H₀ and conclude that the difference is statistically significant.

**Common misconceptions:**
- p-value is **not the probability that H₀ is true**.
- p-value is **not the probability of being wrong when rejecting H₀**.
- A large p-value does not prove H₀; it only indicates a lack of evidence against it.

**Key takeaway:** the p-value depends on the sample size. With very large samples, even tiny effects can be statistically significant, so always assess practical significance (effect size), not just the p-value.

---
← [Back to overview: Hypothesis testing](04-hypothesis-testing.md) · Related topics: [Type I and II errors](04-type-errors.md), [Effect size (Cohen's d)](21-cohens-d.md)