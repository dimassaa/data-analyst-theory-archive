# 📈 Pearson correlation coefficient
🌐 [Русская версия](../topics/07-pearson-correlation.md)

**Pearson correlation coefficient (r)** — a measure of the **linear** relationship between two quantitative variables.

**Formula:**
$$
r = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 \cdot \sum (y_i - \bar{y})^2}}
$$

**Interpretation:**
- $ r > 0 $ — positive relationship (growth of one variable is associated with growth of the other).
- $ r < 0 $ — negative relationship (growth of one is associated with decline of the other).
- $ r \approx 0 $ — no linear relationship.
- $ |r| $ close to 1 — strong linear relationship.

| Value | Interpretation |
|----------|---------------|
| 0.0–0.1 | none/very weak relationship |
| 0.1–0.3 | weak relationship |
| 0.3–0.5 | moderate relationship |
| 0.5–0.7 | noticeable relationship |
| 0.7–0.9 | strong relationship |
| 0.9–1.0 | very strong relationship |

(for the module of r; the same ranges with a negative sign apply to a negative relationship)

**Example:**
We analyze the relationship between ad spend and revenue over 12 months. r = 0.87 → strong positive linear relationship: more ads → more revenue (but this does not prove causation!).

**Requirements:**
- Variables are quantitative (interval/ratio).
- The relationship is approximately **linear**.
- Both variables are approximately normally distributed (when testing significance).
- High sensitivity to **outliers** (a single anomalous point can strongly change r).

**Insight:** Pearson measures only linearity. If the relationship is non-linear (e.g., U-shaped), r can be close to zero even though a real dependency exists. In such cases, visually check the scatter plot and use Spearman.

---
← [Back to overview: Correlation analysis](07-correlation-analysis.md) · Related topics: [Spearman correlation](07-spearman-correlation.md), [Covariance](16-covariance-and-anova.md), [Outliers](10-iqr-quantiles-outliers.md)