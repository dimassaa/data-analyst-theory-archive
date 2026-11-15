# 📍 Vectors
🌐 [Русская версия](../topics/12-vectors.md)

**Vector** — an ordered set of numbers representing a point in n-dimensional space or a direction with magnitude.

**Notation:**
$$
\vec{x} = (x_1, x_2, \ldots, x_n)
$$

**Example:**
A client's feature vector: (age=25, income=50,000, purchases=3) — a point in 3-dimensional space.

**Operations on vectors:**
- **Addition**: $ (x_1 + y_1, x_2 + y_2, \ldots) $ — element-wise.
- **Scalar multiplication**: $ (c \cdot x_1, c \cdot x_2, \ldots) $ — stretching/compressing.
- **Dot product** (see [Dot product](12-dot-product.md)).
- **Norm (length)**: $ \|\vec{x}\| = \sqrt{x_1^2 + x_2^2 + \ldots + x_n^2} $.

**Addition example:**
User income in January = (30,000, 2, 10), in February = (40,000, 3, 15).
Total over two months = (70,000, 5, 25).

**Why vectors matter to analysts:**
- Every row in a dataset is a feature vector.
- Many algorithms (clustering, kNN, PCA, neural networks) operate on vectors.
- Distances between vectors are the basis for grouping similar objects (see [K-means clustering](25-k-means.md)).

**Key takeaway:** a vector is simply "one data row" or "one point in feature space." All operations you perform row-by-row in pandas/Excel are vector manipulations.

---
← [Back to overview: Linear algebra](12-linear-algebra.md) · Related topics: [Dot product](12-dot-product.md), [K-means clustering](25-k-means.md)
