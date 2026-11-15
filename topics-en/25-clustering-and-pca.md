# 🧩 Clustering and PCA

🌐 [Русская версия](../topics/25-clustering-and-pca.md)

**Clustering** is an unsupervised learning method that groups similar objects without pre-defined labels. **PCA (Principal Component Analysis)** is a dimensionality reduction method that simplifies data while retaining maximum variation. Both tools are a pillar of exploratory analysis and the foundation of segmentation.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| K-means clustering | Grouping objects by proximity to centroids | [25-k-means.md](25-k-means.md) |
| PCA (principal component analysis) | Dimensionality reduction while preserving variation | [25-pca.md](25-pca.md) |

---

## 📊 Comparison table

| Aspect | K-means | PCA |
|--------|---------|-----|
| Task type | Clustering (unsupervised) | Dimensionality reduction |
| Input | A set of objects with features | A set of objects with features |
| Output | Cluster labels for objects | New coordinates (principal components) |
| Goal | Find hidden groups | Simplify data, remove correlations |
| Approach | Minimizing distances to cluster centroids | Eigenvectors of the covariance matrix |
| Pairing | Often applied after PCA | Often applied before clustering |

---

## ⏭️ Common pipeline

```
Raw data (many features)
        │
        ▼
   PCA (dimensionality reduction, removing excess noise)
        │
        ▼
   K-means (clustering in the new space)
        │
        ▼
   Segment interpretation → business actions
```

Understanding linear algebra (see [Linear algebra](12-linear-algebra.md)) makes both methods much easier to grasp.

---

## ✅ Summary

- **PCA** helps compress data, visualize high dimensions, and "clean" features of multicollinearity.
- **K-means** lets you find segments of users/objects and interpret them.

Related topics: [Linear algebra](12-linear-algebra.md) · [Covariance](16-covariance-and-anova.md) · [Product segmentation](08-product-metrics.md)

Happy discovering patterns! 📊