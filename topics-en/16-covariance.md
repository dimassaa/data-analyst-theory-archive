# 🔄 Covariance
🌐 [Русская версия](../topics/16-covariance.md)

**Covariance** — a measure of the joint variability of two random variables. It shows in which direction they "move together."

**Formula (for a sample):**
$$
\text{Cov}(x, y) = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{n-1}
$$

**Interpreting the sign:**
- **Cov > 0** — higher x → higher y (positive relationship).
- **Cov < 0** — higher x → lower y (inverse relationship).
- **Cov ≈ 0** — no linear relationship.

**Example:**
We analyze pairs (advertising spend, revenue).
Typically, both values are above average together or below average together → Cov > 0.

**Limitation:**
The magnitude of covariance **depends on the scale** of the variables: if revenue is measured in rubles or in thousands of rubles, the covariance changes by a thousandfold, even though the relationship is the same. Therefore, to compare the strength of the relationship, a normalized version is used — the **Pearson correlation coefficient**:
$$
r = \frac{\text{Cov}(x, y)}{s_x s_y}, \quad r \in [-1, 1]
$$

**Why covariance matters:**
- Understanding the joint behavior of two variables.
- It is part of the **covariance matrix** — the foundation of PCA (see [PCA](25-pca.md)).
- It serves as a building block for correlation and regression.

**Key takeaway:** the sign of covariance is useful, but because it depends on the scale, always switch to Pearson correlation when describing the strength of a relationship.

---
← [Back to overview: Covariance and ANOVA](16-covariance-and-anova.md) · Related topics: [Pearson correlation](07-pearson-correlation.md), [PCA](25-pca.md)
