# Methods for handling missing data

🌐 [Русская версия](../topics/22-missing-data.md)

### 🧩 Methods for handling missing data

Missing values in data are an inevitable problem. Ignoring them can lead to biased estimates and incorrect conclusions. The choice of method depends on the **missingness mechanism** (MCAR, MAR, MNAR).

**Types of missingness:**
- **MCAR (Missing Completely At Random)** — the probability of a missing value does not depend on either observed or missing values.
- **MAR (Missing At Random)** — the probability of missingness depends on observed variables but not on the missing value itself.
- **MNAR (Missing Not At Random)** — the probability of missingness depends on the missing value itself (the hardest case).

---

#### 🔹 Simple methods

1. **Listwise deletion**
   We remove all observations with any missing value.
   *Pros:* simplicity.
   *Cons:* data loss; possible bias if missingness is not MCAR.

2. **Pairwise deletion**
   Available observations are used for each pair of variables.
   *Cons:* different samples for different correlations, not recommended.

3. **Mean/median/mode imputation**
   Missing values are replaced with the mean (for continuous data), the median (in the presence of outliers) or the mode (for categorical data).
   *Pros:* fast.
   *Cons:* underestimates variance, distorts correlations, may introduce bias.

4. **Constant imputation** (e.g., 0 or "Unknown").
   Suitable when a missing value is itself informative.

---

#### 🔹 Advanced methods

5. **Regression imputation**
   A model (linear/logistic) is built to predict the missing variable based on other variables.
   *Pros:* uses relationships between features.
   *Cons:* underestimates uncertainty, may inflate correlations.

6. **k-NN imputation**
   A missing value is filled with the mean (or median) of the nearest neighbors' values in the feature space.
   *Pros:* accounts for multivariate dependencies.
   *Cons:* sensitive to scale, computationally expensive.

7. **Multiple imputation** — the gold standard.

---

#### 🔹 Multiple Imputation (MI)

**Idea:** instead of a single fill-in, several (usually 5–10) plausible datasets are created where the missing values are filled with random draws from the posterior distribution of the missing variable. Then each dataset is analyzed separately, and the results are combined according to Rubin's rules.

**Algorithm:**
1. A model is built for the missing variable (usually via MICE — Multiple Imputation by Chained Equations).
2. m datasets with imputed values are generated.
3. On each dataset, the statistic of interest (e.g., a regression coefficient) and its standard error are computed.
4. The final estimate is the average across the m datasets.
   The final standard error accounts for both within-imputation and between-imputation variability:
   $$
   SE_{\text{total}} = \sqrt{\frac{1}{m}\sum_{i=1}^m SE_i^2 + \left(1+\frac{1}{m}\right) \cdot \frac{1}{m-1}\sum_{i=1}^m (\hat{\theta}_i - \bar{\theta})^2}
   $$

**Pros:**
- Preserves the uncertainty associated with missing values.
- Gives unbiased estimates under MAR.
- Modern standard in scientific research.

**Cons:**
- Requires more computation.
- Harder to implement and explain.

**Example (simplified):**
A dataset has missing income values. Using MICE, we create 5 versions of the dataset where income is filled with different plausible values. We build a churn model on each, obtaining 5 coefficients for income. The final coefficient is the average, and the standard error accounts for the spread among these 5 estimates.

**Insight:** In most practical tasks it is enough to start with simple methods (median, mean) and compare the results with more advanced ones. For critical conclusions, especially when there are many missing values (>5–10%), apply multiple imputation.
### ✅ Summary

| Topic | Key concepts | Practical value |
|------|------------------|------------------------|
| **Missing data** | MCAR/MAR/MNAR, simple imputation, multiple imputation | Preserving data and the correctness of conclusions with incomplete data |

**Key takeaways:**
- Missing values require a deliberate approach: from simple deletion to multiple imputation — depending on the mechanism (MCAR/MAR/MNAR) and the proportion of missing values.
- Incomplete data is no reason to panic, but ignoring the missingness mechanism leads to biased conclusions.

---
Related topics: [Effect size](21-effect-size.md) · [Classification metrics](23-classification-metrics.md)