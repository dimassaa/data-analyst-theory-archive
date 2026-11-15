# ⚖️ Multiple Hypothesis Testing

🌐 [Русская версия](../topics/17-multiple-hypothesis-testing.md)

**Multiple hypothesis testing** is a situation where you test several hypotheses at the same time (or consecutively). In this case, the risk of at least one type I error rises sharply.

**The problem:**
At a significance level of α = 0.05, each individual test has a 5% chance of a false positive. With 20 tests, the expected number of false positives ≈ 1. This undermines the validity of any conclusions.

**Formula:**
$$
P(\text{at least one type I error}) = 1 - (1 - \alpha)^k
$$
where k is the number of tests. With α=0.05 and k=20: 1 - 0.95²⁰ ≈ 0.64 (64%!).

**Control methods:**
1. **Bonferroni correction:** $ \alpha_{\text{adjust}} = \alpha / k $. Simple but very conservative — it reduces power.
2. **Holm's correction:** an iterative adjustment, more powerful than Bonferroni.
3. **FDR control (False Discovery Rate):** the Benjamini–Hochberg method, which controls the proportion of false rejections among the rejected hypotheses. More powerful than Bonferroni and widely used in genomics, neuroscience, and A/B tests.
4. **Some A/B platforms** (VWO, Optimizely) have a built-in correction for multiple testing.

**Example:**
In an A/B test we check 5 metrics at once (conversion, average check, retention...). Without correction, the probability of at least one false positive ≈ 23%. If rigor is needed, apply FDR correction.

**Key takeaway:** multiple hypothesis testing is one of the most common mistakes in product analytics. If you compare several metrics or several A/B tests in parallel, always account for multiplicity. Otherwise "significant" results will just be noise.

---
← [Back to overview: Non-parametric Tests](17-nonparametric-tests.md) · Related topics: [p-value](04-p-value.md), [A/B testing](05-ab-testing.md), [Effect size](21-effect-size.md)