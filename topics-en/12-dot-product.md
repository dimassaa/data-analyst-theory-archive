# ✨ Dot product
🌐 [Русская версия](../topics/12-dot-product.md)

**Dot product** — an operation that maps two vectors to a single number.

**Formula:**
$$
\vec{x} \cdot \vec{y} = \sum_{i=1}^{n} x_i y_i = x_1 y_1 + x_2 y_2 + \ldots + x_n y_n
$$

**Example:**
$ \vec{x} = (2, 3) $, $ \vec{y} = (4, 1) $.
Dot product = 2×4 + 3×1 = 8 + 3 = **11**.

**Geometric meaning:**
$$
\vec{x} \cdot \vec{y} = \|\vec{x}\| \cdot \|\vec{y}\| \cdot \cos(\theta)
$$
where θ is the angle between the vectors. Therefore:
- Dot product = 0 → vectors are **perpendicular** (orthogonal).
- Positive → vectors point in the "same direction."
- Negative → vectors point in "opposite directions."

**Why it matters to analysts:**
- **Similarity measure**: in cosine similarity, documents/users are compared via a normalized dot product.
- **Linear models**: the prediction of a regression or neural network is a dot product of model weights and a feature vector: $ \hat{y} = w_1 x_1 + w_2 x_2 + \ldots + b $.
- **Correlation**: the Pearson correlation coefficient is expressed through centered vectors and their dot product (see [Pearson correlation](07-pearson-correlation.md)).

**Key takeaway:** the dot product is the fundamental operation of "weighted summation." It connects data with model weights, which is why neither regressions nor neural networks can work without it.

---
← [Back to overview: Linear algebra](12-linear-algebra.md) · Related topics: [Vectors](12-vectors.md), [Simple linear regression](15-simple-linear-regression.md)
