# 📈 Linear Regression: Simple Linear Regression and OLS

🌐 [Русская версия](../topics/15-linear-regression.md)

**Linear regression** is one of the most popular statistical methods: it models the relationship between a target variable and one or more predictors. It is widely used for forecasting, for analyzing the effect of predictors, and for building baseline models.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|------|---------------|------|
| Simple linear regression | One dependent variable, one predictor, a straight line | [15-simple-linear-regression.md](15-simple-linear-regression.md) |
| OLS (Ordinary Least Squares) | How the coefficients are fitted: minimizing errors | [15-ols.md](15-ols.md) |

---

## 📊 Comparison table

| Aspect | Simple regression | OLS |
|--------|-------------------|-----|
| What it describes | Model $ y = a + bx $ | A method for estimating parameters |
| Number of predictors | One | Any number (special case: one) |
| Goal | Prediction and understanding the relationship | Find the coefficients that minimize the residual sum of squares |

**Formula of the simple model:**
$$
\hat{y} = b_0 + b_1 x
$$
where $ b_0 $ is the intercept, $ b_1 $ is the slope coefficient, $ x $ is the predictor, and $ \hat{y} $ is the prediction.

**The slope coefficient $ b_1 $** — the key interpretation: when $ x $ increases by 1 unit, the prediction of $ y $ changes by $ b_1 $ on average.

**Model quality:**
- **R² (coefficient of determination)** — the proportion of the variance of $ y $ explained by the model: from 0 (no explanation) to 1 (perfect fit).
- **Residuals** — the difference $ y - \hat{y} $; analyzing them is part of model diagnostics.

---

## ⚠️ Caveats

- Regression shows **association**, not causation.
- Valid conclusions rely on **assumptions**: linearity, independent residuals, normally distributed residuals, homoscedasticity.
- **Outliers** strongly affect the coefficients — run an exploratory analysis first (see [Outliers](10-outliers.md)).

---

## ✅ Summary

- Linear regression models a continuous target variable as a linear combination of predictors.
- **OLS** — the standard way to estimate coefficients (minimizing the residual sum of squares).
- R² and residual analysis let you assess how good the model is.

Related topics: [Correlation analysis](07-correlation-analysis.md) · [Covariance](16-covariance-and-anova.md) · [Logistic regression](19-logistic-regression.md)(for binary outcomes)

Happy modeling! 📊