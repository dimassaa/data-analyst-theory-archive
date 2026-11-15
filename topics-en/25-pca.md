# 📉 PCA (principal component analysis)

🌐 [Русская версия](../topics/25-pca.md)

**PCA (Principal Component Analysis)** is a dimensionality reduction method: it finds new orthogonal directions (principal components) along which the data has maximum spread. It rotates the data into new coordinates and lets you discard "insignificant" directions.

**The idea:**
1. The data is centered (the mean is subtracted).
2. The **covariance matrix** of the features is built (see [Covariance](16-covariance.md)).
3. Its **eigenvectors** (principal components) and **eigenvalues** (share of explained variation) are found.
4. The data is projected onto the first few components.

**Example:**
A dataset with 100 features. The first 5 principal components explain 85% of the variation → you can work with 5 "compressed" features instead of 100. This speeds up models and reduces overfitting.

**What PCA gives you:**
- **Dimensionality reduction**: fewer features — less noise and overfitting.
- **Visualization**: the first 2–3 components let you plot high-dimensional data on a plane.
- **Removing multicollinearity**: the new features are orthogonal (uncorrelated).

**Interpretation:**
- Each component is a linear combination of the original features.
- **Loadings** show which original features contribute most to a component — you can "read" the meaning of a component.

**Limitations:**
- Components are hard to explain to business ("what does principal component #3 mean?").
- PCA assumes **linear** structures.
- Requires **standardization** of features, otherwise features with large variance dominate.

**Key takeaway:** PCA is often used **together with** clustering: first reduce dimensionality, then cluster (see [K-means](25-k-means.md)). For product segmentation, PCA helps surface "latent factors" of user behavior.

---
← [Back to overview: Clustering and PCA](25-clustering-and-pca.md) · Related topics: [K-means](25-k-means.md), [Covariance](16-covariance.md), [Matrices](12-matrices.md)