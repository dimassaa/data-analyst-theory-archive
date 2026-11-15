# 📐 Ordinary Least Squares (OLS)

🌐 [Русская версия](../topics/15-ols.md)

**OLS (Ordinary Least Squares)** is a method for estimating the coefficients of a linear regression by minimizing the **residual sum of squares**:

$$
\min_{b_0, b_1} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 = \min_{b_0, b_1} \sum_{i=1}^{n} (y_i - (b_0 + b_1 x_i))^2
$$

The residual $ e_i = y_i - \hat{y}_i $ is the vertical distance from a point to the line.

**Why squares?**
- They penalize large errors more heavily than small ones.
- They give a single closed-form solution (formula).
- The absolute value ("sum of absolute deviations") has no derivative, making the solution harder.

**Coefficient estimates:**
$$
b_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}, \qquad b_0 = \bar{y} - b_1 \bar{x}
$$

**Example:**
Data: (1, 3), (2, 5), (3, 7). Here the line y = 2x + 1 passes perfectly through the points. A more realistic example has noise: OLS will fit a line minimizing the total error over all points.

**Properties of OLS:**
- When the assumptions hold (linearity, independence, homoscedasticity), the estimates $ b_0, b_1 $ are **unbiased and efficient** (Gauss–Markov theorem).
- Sensitive to **outliers**: a single anomalous x can pull the line strongly toward itself.
- Under multicollinearity (strongly correlated predictors), coefficients become unstable.

**How to evaluate the model:**
- **R²** — the proportion of explained variation.
- **p-value** of the coefficients — whether the predictor's contribution is significant.
- **Residual analysis** — checking the assumptions.

**Key takeaway:** OLS is the standard workhorse for fitting regressions: it has an exact solution, and most statistical libraries use it. If your data contain strong outliers or violated assumptions — consider robust regressions or transformations.

---
← [Back to overview: Linear Regression](15-linear-regression.md) · Related topics: [Simple Linear Regression](15-simple-linear-regression.md), [Checking residual assumptions](04-hypothesis-testing.md)(general checks)