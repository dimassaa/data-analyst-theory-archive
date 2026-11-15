# 🔀 Mann–Whitney U Test

🌐 [Русская версия](../topics/17-mann-whitney.md)

**The Mann–Whitney test** (Mann–Whitney U) is a non-parametric test for the hypothesis that two **independent** samples come from the same distribution, or that the distribution of one sample is shifted relative to the other.

**Parametric alternative:** t-test for independent samples.

**Idea:** we replace the values with ranks (ordinal positions) and compare the mean ranks of the groups. It does not assume normality.

**Formula for the U statistic (conceptual):**
U shows how often the elements of one group exceed the elements of the other. The closer (smaller) U is to 0, the stronger the difference in distributions.

**Example:**
We test two interface designs by task completion time. The data are skewed and contain outliers. The Mann–Whitney test checks whether there is a significant difference in the distributions, without relying on normality.

**When to use:**
- The data are **not normally** distributed (outliers, strong skew).
- The data are **ordinal** (ratings, scores, ranks).
- A small sample, when the t-test is unreliable.

**Limitations:**
- It does not directly estimate the **effect size** (that must be computed separately).
- It is less powerful than the t-test when normality truly holds (the price of being assumption-free).

**Key takeaway:** the U test is the non-parametric counterpart of the t-test for independent groups. For dependent (paired) data, use the Wilcoxon test.

---
← [Back to overview: Non-parametric Tests](17-nonparametric-tests.md) · Related topics: [Wilcoxon test](17-wilcoxon.md), [t-test](04-t-test.md), [Spearman correlation](07-spearman-correlation.md)