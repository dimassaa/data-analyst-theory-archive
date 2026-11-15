# 📈 Simple Linear Regression

🌐 [Русская версия](../topics/15-simple-linear-regression.md)

**Simple linear regression** is a model describing the relationship between one dependent variable $ y $ and one predictor $ x $ using a straight line.

**Formula:**
$$
\hat{y} = b_0 + b_1 x
$$
- $ b_0 $ — the intercept (the value of $ \hat{y} $ at $ x = 0 $),
- $ b_1 $ — the slope coefficient (the average change in $ y $ when $ x $ increases by 1),
- $ \hat{y} $ — the predicted value.

**Example:**
$$
\text{revenue} = 50 + 2 \cdot \text{number of ad impressions (thousand)}
$$
At 0 impressions, revenue ≈ 50 thousand; each extra 1,000 impressions adds ≈ 2 thousand in revenue.

**Typical tasks:**
- Forecasting (sales by season, demand by price).
- Estimating the effect of a predictor (how much the metric grows when the input changes).

**How the line is fitted:**
The coefficients are fitted by ordinary least squares — the line for which the sum of squared vertical deviations of the points from the line is minimal (see [OLS](15-ols.md)).

**Assessing quality:**
- **R²** — the proportion of explained variation in $ y $. R² = 0.8 → 80% of the spread is explained by the model.
- **Residual analysis**: the residuals should be scattered randomly with no clear patterns; patterns indicate nonlinearity of the relationship or a missing predictor.

**Assumptions (for valid conclusions):**
- Linearity of the relationship.
- Independence of observations.
- Residuals are normally distributed and have constant variance (homoscedasticity).

**Key takeaway:** interpret $ b_1 $ as the "average effect" of the predictor, but remember: correlation ≠ causation. The relationship can be distorted by a third variable that affects both.

---
← [Back to overview: Linear Regression](15-linear-regression.md) · Related topics: [OLS](15-ols.md), [Pearson correlation](07-pearson-correlation.md), [Outliers](10-outliers.md)