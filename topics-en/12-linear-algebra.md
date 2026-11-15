# ➗ Linear algebra: vectors, matrices, dot product, matrix multiplication
🌐 [Русская версия](../topics/12-linear-algebra.md)

Linear algebra is the mathematical foundation of many data analysis and machine learning methods: regressions, PCA, neural networks. For a data analyst, it is enough to understand the core concepts: vectors, matrices, and operations on them.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Vectors | An ordered set of numbers with direction and magnitude | [12-vectors.md](12-vectors.md) |
| Matrices | Tables of numbers, linear transformations | [12-matrices.md](12-matrices.md) |
| Dot product | A single number reflecting vector "similarity" | [12-dot-product.md](12-dot-product.md) |
| Matrix multiplication | Composition of linear transformations | [12-matrix-multiplication.md](12-matrix-multiplication.md) |

---

## 📊 Comparison table

| Concept | Definition | Size | Example use in DS |
|---------|------------|------|-------------------|
| **Vector** | $ (x_1, x_2, \ldots, x_n) $ | $ n $ | Features of a single data row |
| **Matrix** | Table $ m \times n $ | $ m \times n $ | Dataset: rows × features |
| **Dot product** | $ \sum x_i y_i $ | scalar | Vector similarity, linear models, neural networks |
| **Matrix multiplication** | $ C = A \cdot B $ | $ (m \times n)\cdot(n \times k) \to m \times k $ | Linear transformations, PCA, neural networks |

---

## 🧠 Concept hierarchy

```
Vector (data row)
   └─ operations: addition, scalar multiplication, dot product
Matrix (dataset / transformation)
   └─ operations: multiply by vector, matrix multiplication, transpose
Dot product — the simplest measure of similarity between two vectors
```

**Key idea for the analyst:** data is represented as a **matrix** (rows are observations, columns are features), and mathematical models are the result of **multiplying matrices and vectors**. Understanding these operations allows you to intuitively grasp how regressions, PCA, and neural networks work.

---

## ✅ Summary

- Vectors and matrices are the language that data and models "speak."
- The dot product measures vector similarity and is at the heart of linear models.
- Matrix multiplication is the composition of transformations that neural networks and PCA are built from.

Related topics: [Simple linear regression](15-simple-linear-regression.md) · [PCA](25-pca.md) · [Linear algebra basics in analysis](06-math-analysis-and-algebra.md)

Happy learning! 📊
