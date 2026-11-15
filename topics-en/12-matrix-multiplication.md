# 🔗 Matrix multiplication
🌐 [Русская версия](../topics/12-matrix-multiplication.md)

**Matrix multiplication** — a linear algebra operation that generalizes the dot product. The result is a matrix whose each element is the dot product of a row from the first matrix and a column from the second.

**Dimension rule:**
A matrix $ A $ of size $ m \times n $ can be multiplied by a matrix $ B $ of size $ n \times k $. The result $ C = A \cdot B $ has size $ m \times k $. The inner dimension $ n $ must match.

**Element formula:**
$$
c_{ij} = \sum_{t=1}^{n} a_{it} b_{tj}
$$

**Example:**
$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \quad
B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}
$$
$$
A \cdot B = \begin{pmatrix}
1\cdot5 + 2\cdot7 & 1\cdot6 + 2\cdot8\\
3\cdot5 + 4\cdot7 & 3\cdot6 + 4\cdot8
\end{pmatrix}
= \begin{pmatrix} 19 & 22 \\ 43 & 50 \end{pmatrix}
$$

**Important properties:**
- **Non-commutative**: in general, $ A \cdot B \neq B \cdot A $ (order matters!).
- **Associative**: $ (A \cdot B) \cdot C = A \cdot (B \cdot C) $.
- **Distributive**: $ A \cdot (B + C) = A \cdot B + A \cdot C $.

**Why it matters to analysts:**
- **Data matrix × model weights** = predictions for all rows at once (one operation instead of a loop).
- **PCA and SVD** reduce to a decomposition of the covariance matrix (see [PCA](25-pca.md)).
- **Neural networks** are multi-layer matrix multiplication.

**Key takeaway:** matrix multiplication is a way to compute many dot products simultaneously. In linear models, it allows you to recalculate predictions for the entire dataset with a single "matrix stroke," which is what makes computations fast.

---
← [Back to overview: Linear algebra](12-linear-algebra.md) · Related topics: [Matrices](12-matrices.md), [Dot product](12-dot-product.md), [PCA](25-pca.md)
