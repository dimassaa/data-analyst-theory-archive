# 📏 z-test

🌐 [Русская версия](../topics/04-z-test.md)

The **z-test** is similar to the t-test but is used in two cases:
- the standard deviation of the population $ \sigma $ is **known**,
- the sample is **large** (usually n > 30), and by the Central Limit Theorem the sample mean is normally distributed, while the sample standard deviation estimates σ well.

**Formula for comparing means:**
$$
z = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}
$$
If σ is unknown but the samples are large, we substitute sample standard deviations.

**The z-test is also used for proportions:**
$$
z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{\hat{p}(1-\hat{p}) \left( \frac{1}{n_1} + \frac{1}{n_2} \right)}}
$$
where $ \hat{p} $ is the pooled proportion.

**Example:**
In an A/B test the conversion in the control is 10% (n₁=1000), and in the test 12% (n₂=1000).
z = (0.12-0.10) / sqrt(0.11*0.89*(1/1000+1/1000)) ≈ 1.43.
p-value ≈ 0.15 > 0.05 → we fail to reject H₀; there is no significant difference.

**Key takeaway:** the z-test is often used in web analytics to compare conversions and CTR thanks to its simplicity and the asymptotic normality of proportions.

---
← [Back to overview: Hypothesis testing](04-hypothesis-testing.md) · Related topics: [t-test](04-t-test.md), [Sample size (A/B)](05-sample-size.md), [CLT](13-central-limit-theorem.md)