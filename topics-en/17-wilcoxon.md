# 🔗 Wilcoxon Signed-Rank Test

🌐 [Русская версия](../topics/17-wilcoxon.md)

**The Wilcoxon test** (Wilcoxon signed-rank) is a non-parametric test for the hypothesis that the median of the **differences** between paired observations is zero (i.e., there is no difference). It is used for **dependent (paired) samples**.

**Parametric alternative:** paired t-test.

**Idea:** the pair differences $ d_i = x_i - y_i $ are computed, ordered by absolute value (ranked), and the sums of positive and negative ranks are calculated. The stronger the shift, the smaller the p-value.

**Example:**
Task completion time is measured for the same users before and after a design change. If the distribution of the differences is not normal, we use the Wilcoxon test instead of the paired t-test.

**When to use:**
- Paired data (before/after, left/right, two instruments).
- The differences are not normally distributed.
- There are outliers.

**Limitations:**
- It uses only **ranked** data — it does not take into account the magnitude of the differences.
- It does not work if the difference is zero in more than ~5% of the pairs (these must be removed, or special modifications used).

**Key takeaway:** for paired data, this is the "non-parametric paired t-test." If your data have outliers in the differences, Wilcoxon is more reliable.

---
← [Back to overview: Non-parametric Tests](17-nonparametric-tests.md) · Related topics: [Mann–Whitney test](17-mann-whitney.md), [Paired t-test](04-t-test.md)