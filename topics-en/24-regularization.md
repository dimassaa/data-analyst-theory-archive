# Regularization (L1/L2) in multiple regression

🌐 [Русская версия](../topics/24-regularization.md)

### 📉 Regularization (L1/L2) in the context of multiple regression

When building multiple linear regression with a large number of predictors, there is a risk of **overfitting**: the model fits the training data too closely, including noise, and generalizes poorly to new data. Regularization is a method of combating overfitting by adding a penalty for the magnitude of the coefficients to the loss function.

---

#### 🔹 The problem with plain OLS

Multiple regression: $ y = \beta_0 + \beta_1 x_1 + \dots + \beta_p x_p + \varepsilon $.
OLS minimizes the residual sum of squares:
$$
\text{RSS} = \sum_{i=1}^n (y_i - \hat{y}_i)^2
$$
If there are many predictors or they are strongly correlated, the coefficient estimates become unstable (high variance), and the model predicts poorly on new data.

---

#### 🔹 The idea of regularization

A **penalty term** that depends on the magnitude of the coefficients (except the intercept $ \beta_0 $) is added to the loss function. The goal is to reduce the absolute values of the coefficients, "shrinking" them toward zero, which reduces model complexity.

The new objective function:
$$
\text{Loss} = \text{RSS} + \lambda \cdot \text{Penalty}(\beta)
$$
where $ \lambda \ge 0 $ is the regularization hyperparameter controlling the strength of the penalty.

- $ \lambda = 0 $ → plain OLS.
- $ \lambda \to \infty $ → all coefficients tend to zero, only $ \beta_0 $ (the mean) remains.

---

#### 🔹 L2 regularization (Ridge regression)

The penalty equals the sum of the **squares** of the coefficients:
$$
\text{Penalty}_{L2} = \sum_{j=1}^p \beta_j^2
$$
Objective function:
$$
\text{Loss} = \text{RSS} + \lambda \sum_{j=1}^p \beta_j^2
$$

**Properties:**
- Coefficients are shrunk toward zero but never become exactly zero (except as $ \lambda \to \infty $).
- Reduces the variance of estimates, especially under multicollinearity.
- The solution has an analytical form: $ \hat{\beta} = (X^T X + \lambda I)^{-1} X^T y $, where $ I $ is the identity matrix (except the first element if the intercept is not regularized).
- Suitable when all features matter but need to be "muted".

**Example:**
Predicting a house price from 100 characteristics. Many features correlate (area, number of rooms). Ridge will reduce the coefficients, keeping all features but with smaller values.

---

#### 🔹 L1 regularization (Lasso regression)

The penalty equals the sum of the **absolute values** of the coefficients:
$$
\text{Penalty}_{L1} = \sum_{j=1}^p |\beta_j|
$$
Objective function:
$$
\text{Loss} = \text{RSS} + \lambda \sum_{j=1}^p |\beta_j|
$$

**Properties:**
- Can zero out coefficients, i.e., perform **feature selection**.
- The solution has no analytical form; coordinate descent or LARS is usually used.
- Suitable when only a few predictors are assumed to really matter (sparse model).

**Geometric intuition:** the constraint on the sum of coefficient magnitudes has the shape of a diamond, which zeroes out some coefficients at the vertices — unlike the circle in Ridge.

**Example:**
Predicting customer churn based on 500 behavioral features. Lasso will keep, say, the 20 most important ones and zero out the rest, simplifying the model.

---

#### 🔹 L1 vs L2

| Characteristic | Ridge (L2) | Lasso (L1) |
|----------------|------------|------------|
| Penalty | $ \sum \beta_j^2 $ | $ \sum |\beta_j| $ |
| Zeroing coefficients | No (except λ→∞) | Yes |
| Robustness to multicollinearity | Good | Worse, may pick a random one from correlated features |
| Analytical solution | Yes | No |
| Use case | When all features are potentially useful | When feature selection is needed |

**Elastic Net** combines both penalties:
$$
\text{Loss} = \text{RSS} + \lambda_1 \sum |\beta_j| + \lambda_2 \sum \beta_j^2
$$
It allows combining feature selection with Ridge's robustness under strong correlation.

---

#### 🔹 Choosing $ \lambda $

The hyperparameter $ \lambda $ is tuned via **cross-validation** (usually k-fold). Often a sequence of λ values is used and the one that minimizes the mean squared error on the validation folds is selected. In libraries (scikit-learn) `RidgeCV` and `LassoCV` are available.

**Insight:** Regularization is essential with a large number of features (p > n or p comparable to n). Even with few features, light regularization often improves prediction by reducing overfitting.
### ✅ Summary

| Topic | Key concepts | When to use |
|------|------------------|--------------------|
| **Regularization** | L1 (Lasso), L2 (Ridge), Elastic Net, hyperparameter λ | Multiple regression at risk of overfitting, feature selection |

**Key takeaways:**
- Regularization is a must-have tool with a large number of features (p > n or p comparable to n).
- L1 (Lasso) zeroes out weights and performs feature selection; L2 (Ridge) stabilizes coefficients under multicollinearity.
- The hyperparameter λ is tuned via cross-validation (RidgeCV, LassoCV).

---
Related topics: [Linear regression](15-linear-regression.md) · [K-means](25-k-means.md) · [PCA](25-pca.md) · [GLM](26-glm.md)