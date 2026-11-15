# 📊 Normal distribution (Gaussian)

🌐 [Русская версия](../topics/03-normal-distribution.md)

**Normal distribution** is a continuous distribution that describes many natural phenomena in which values are symmetrically grouped around the mean.

**Parameters:**
- $ \mu $ — expected value (mean),
- $ \sigma $ — standard deviation (spread).

**Probability density:**
$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2} \right)
$$

**Shape:** the famous bell-shaped curve, symmetric about $ \mu $.

**Key property — the three-sigma rule (68–95–99.7):**
- ≈68% of the data lie within $ \mu \pm 1\sigma $,
- ≈95% — within $ \mu \pm 2\sigma $,
- ≈99.7% — within $ \mu \pm 3\sigma $.

**Examples:**
- the height of people of a given sex and age,
- measurement errors,
- results of standardized tests (IQ).

**Use in analytics:**
- Many statistical tests (t-test, ANOVA) assume the normality of residuals or data.
- Central Limit Theorem: the mean of a large sample tends to a normal distribution regardless of the distribution of the original data. This is the foundation for building confidence intervals and hypothesis testing.
- Used in regression models and machine learning (e.g., Gaussian processes).

**Key takeaway:** even if your data are not normal, you can often analyze the sample mean, which thanks to the CLT will be normally distributed (given a sufficiently large sample size).

---
← [Back to overview: Distributions](03-probability-distributions.md) · Related topics: [CLT](13-central-limit-theorem.md), [Confidence intervals](14-confidence-intervals.md)