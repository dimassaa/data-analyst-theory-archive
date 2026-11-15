# 📐 Cohen's d

🌐 [Русская версия](../topics/21-cohens-d.md)

**Cohen's d** is a standardized effect size for the difference between two means. It shows by how many standard deviations the group means differ.

**Formula:**
$$
d = \frac{\bar{x}_1 - \bar{x}_2}{s_p}
$$
where $ \bar{x}_1, \bar{x}_2 $ are the group means and $ s_p $ is the pooled standard deviation:
$$
s_p = \sqrt{\frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}}
$$

**Example:**
Control: mean conversion 10%, sd=2%. Test: 12%, sd=2%. Equal n.
d = (12 - 10) / 2 = **1.0** → strong effect (a difference of one standard deviation).

**Empirical interpretation guidelines (per Cohen):**
| |d| | Interpretation |
|-----|---------------|
| 0.0–0.2 | Small effect |
| 0.2–0.5 | Small/moderate |
| 0.5–0.8 | Medium effect |
| 0.8+ | Large effect |

**Why standardization:**
- d is dimensionless, so effects from different studies can be compared (meta-analysis).
- It does not depend on units of measurement (rubles, seconds, percentages — everything is converted into "standard deviations").

**Limitations:**
- Sensitive to outliers (they distort sd).
- Does not replace uncertainty intervals — it is useful to report a confidence interval for d.

**Key takeaway:** Cohen's d is the "common language" of effect size. In A/B tests, research papers, and reports, d lets you quickly gauge how large a difference is, regardless of the original units.

---
← [Back to overview: Effect size](21-effect-size.md) · Related topics: [Relative uplift](21-relative-uplift.md), [t-test](04-t-test.md), [Standard deviation](01-standard-deviation.md)