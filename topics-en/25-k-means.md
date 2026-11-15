# 🧩 K-means clustering

🌐 [Русская версия](../topics/25-k-means.md)

**K-means** is one of the most popular clustering algorithms: it splits objects into k groups (clusters), trying to make objects within a group as similar as possible and objects across groups as different as possible.

**Algorithm (iterative):**
1. Choose k (the number of clusters).
2. Initialize k cluster centroids (randomly or with smart heuristics).
3. Assign each object to the nearest centroid.
4. Recalculate centroids as the means of their clusters' objects.
5. Repeat steps 3–4 until the centroids stop changing.

**Example:**
Customer segmentation of an online store by features (purchase frequency, average order value). K-means with k=3 will identify: "rare cheap", "frequent average", "rare expensive" — segments that can be worked with separately (marketing, pricing).

**How to choose k:**
- **Elbow method**: the quality metric (sum of distances to centroids) drops sharply up to k*, then declines slowly.
- **Silhouette score**: a trade-off between cluster density and their separability.

**Limitations:**
- **k must be set in advance** (hard to guess).
- Sensitive to **feature scale** — always standardize your data.
- **Outliers** severely distort centroids.
- Only finds **spherical** clusters; complex shapes require other methods (DBSCAN, hierarchical clustering).
- Can give different results across runs (depends on initialization).

**Key takeaway:** typical use cases — user segmentation, document classification, image compression. Remember: the clusters found are a hypothesis about the data structure that must be interpreted and confirmed with business context.

---
← [Back to overview: Clustering and PCA](25-clustering-and-pca.md) · Related topics: [PCA](25-pca.md), [Vectors](12-vectors.md), [Impact of outliers](10-outliers.md)