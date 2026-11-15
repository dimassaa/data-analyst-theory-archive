# 🔢 Matrices
🌐 [Русская версия](../topics/12-matrices.md)

**Matrix** — a rectangular table of numbers with $ m $ rows and $ n $ columns. The size of the matrix is denoted $ m \times n $.

**Notation:**
$$
A = \begin{pmatrix}
a_{11} & a_{12} & \ldots & a_{1n}\\
a_{21} & a_{22} & \ldots & a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1} & a_{m2} & \ldots & a_{mn}
\end{pmatrix}
$$

**Example:**
Data matrix for three clients across three features:

$$
\begin{pmatrix}
25 & 50{,}000 & 3\\
30 & 70{,}000 & 5\\
41 & 90{,}000 & 1
\end{pmatrix}
$$
(rows are clients; columns are age, income, purchases)

**Key operations:**
- **Addition** — element-wise, same dimensions required.
- **Scalar multiplication** — multiply all elements.
- **Multiply by a vector/matrix** (see [Matrix multiplication](12-matrix-multiplication.md)).
- **Transpose**: swap rows ↔ columns.

**Identity matrix** — a "neutral" matrix with ones on the diagonal and zeros elsewhere; multiplying by it does not change the matrix.

**Why matrices matter to analysts:**
- **Dataset** = matrix (rows are observations, columns are features).
- **Regressions and models** are expressed through matrix equations.
- **PCA, SVD, neural networks** — all involve operations on matrices.

**Key takeaway:** any tabular data (SQL, pandas, Excel) can be conveniently viewed as a matrix. Understanding matrix operations helps you see how statistical libraries work "under the hood."

---
← [Back to overview: Linear algebra](12-linear-algebra.md) · Related topics: [Matrix multiplication](12-matrix-multiplication.md), [Vectors](12-vectors.md)
