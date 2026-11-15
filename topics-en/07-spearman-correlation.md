# 📊 Spearman's rank correlation
🌐 [Русская версия](../topics/07-spearman-correlation.md)

**Spearman correlation coefficient (ρ)** — a measure of the **monotonic** relationship between two variables, computed from **ranks** rather than values.

**Idea:** instead of the original values, their ranks are used (positions in an ordered series), and the Pearson correlation is computed for the ranks.

**Formula for the case without tied ranks:**
$$
\rho = 1 - \frac{6 \sum d_i^2}{n(n^2 - 1)}
$$
where $ d_i $ is the difference between the ranks of the i-th observation for the two variables, and $ n $ is the sample size.

**Interpretation is similar to Pearson:**
- $ \rho > 0 $ — positive monotonic relationship.
- $ \rho < 0 $ — negative monotonic relationship.
- $ \rho \approx 0 $ — no monotonic relationship.

**Advantages over Pearson:**
- Works with **ordinal** (rank) data (e.g., ratings "dissatisfied/neutral/satisfied").
- Captures **any monotonic** relationships, not only strictly linear ones (e.g., exponential growth).
- Robust to **outliers**, since ranks are used rather than values.

**Example:**
We assess whether hotel rating (1–5) and the probability of rebooking are related. ρ = 0.62 → noticeable monotonic relationship: a higher rating means a higher likelihood of returning.

**Insight:** Spearman is "insurance" against violations of the normality and linearity requirements. If you are unsure about the nature of the relationship, start with Spearman and a scatter plot.

---
← [Back to overview: Correlation analysis](07-correlation-analysis.md) · Related topics: [Pearson correlation](07-pearson-correlation.md), [Non-parametric tests](17-nonparametric-tests.md)