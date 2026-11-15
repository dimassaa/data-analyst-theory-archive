# 📊 ANOVA (analysis of variance)
🌐 [Русская версия](../topics/16-anova.md)

**ANOVA (Analysis of Variance)** — a statistical method for testing whether the means of **three or more groups** differ (categorical factor → continuous variable). It extends the t-test, which works only for two groups.

**Idea:**
Split the total variability of the data into two parts:
1. **Between-group variation** (between group means) — this includes the effect of the factor.
2. **Within-group variation** (inside groups, "noise") — natural spread.

**F-statistic:**
$$
F = \frac{\text{between-group variance}}{\text{within-group variance}}
$$
A large F means group means differ more than can be explained by chance.

**Example:**
Comparing the average order value across three acquisition channels: contextual ads, targeting, SEO.
H₀: the means are equal. An F-test with p-value < 0.05 → reject H₀ → at least one channel differs.

**Assumptions:**
- Observations are independent.
- Data within groups are approximately normal.
- Group variances are approximately equal (homoscedasticity).

**Limitation:**
ANOVA says "there is a difference" but **does not say between which groups**. For that, **post-hoc tests** (Tukey, Bonferroni) are needed — they compare pairs of groups with a correction for multiple comparisons (see [Multiple hypothesis testing](17-multiple-hypothesis-testing.md)).

**Key takeaway:** if there are only two groups, you can use the t-test; for 3+ groups, use ANOVA. Do not search for differences with multiple t-tests: this increases the risk of false positive conclusions due to the multiplicity of comparisons.

---
← [Back to overview: Covariance and ANOVA](16-covariance-and-anova.md) · Related topics: [t-test](04-t-test.md), [Multiple hypothesis testing](17-multiple-hypothesis-testing.md), [Non-parametric tests](17-nonparametric-tests.md)
