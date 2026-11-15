# Logistic Regression

🌐 [Русская версия](../topics/19-logistic-regression.md)

### 📈 Logistic Regression

**Logistic regression** is a statistical model for predicting a **binary dependent variable** (0/1, yes/no, churned/stayed). Unlike linear regression, which predicts a continuous value, logistic regression estimates the **probability** of an event occurring.

---

#### 🧠 Model

Let $ Y \in \{0, 1\} $ be the target variable and $ X_1, \dots, X_p $ the predictors. Logistic regression models the probability $ P(Y=1 \mid X) $ using the **sigmoid function**:

$$
P(Y=1 \mid X) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X_1 + \dots + \beta_p X_p)}}
$$

The logit (log odds) is linear in the predictors:

$$
\log\left( \frac{P(Y=1)}{1 - P(Y=1)} \right) = \beta_0 + \beta_1 X_1 + \dots + \beta_p X_p
$$

Here $ \frac{P}{1-P} $ is the **odds**, and the logarithm of the odds is called the **logit**.

---

#### 🔍 Parameter estimation

The parameters $ \beta $ are estimated by **maximum likelihood** (not OLS as in linear regression). The log-likelihood:

$$
\ell(\beta) = \sum_{i=1}^n \left[ y_i \log(p_i) + (1-y_i) \log(1-p_i) \right]
$$

where $ p_i = P(Y=1 \mid X_i) $. Maximizing $ \ell(\beta) $ is usually done numerically (e.g., the Newton–Raphson algorithm).

---

#### 📊 Interpreting the coefficients

- The coefficient $ \beta_j $ shows the change in the **logit** (log odds) when $ X_j $ increases by one unit.
- More interpretable is the **odds ratio**: $ OR_j = e^{\beta_j} $. It shows how many times the odds of the event are multiplied when $ X_j $ increases by 1.
  - If $ OR > 1 $ — the predictor increases the odds.
  - If $ OR < 1 $ — it decreases them.

**Example:**
Model: $ \log\left( \frac{p}{1-p} \right) = -3 + 0.05 \cdot \text{age} + 0.8 \cdot \text{sex (female=1)} $.
The coefficient for age: 0.05 → OR = e^{0.05} ≈ 1.051. So each year of age multiplies the odds (e.g., of responding to an ad) by 1.051, i.e., increases them by 5.1% (all else being equal).
The coefficient for sex: 0.8 → OR = e^{0.8} ≈ 2.23 — women's odds are 2.23 times higher than men's.

---

#### 🧪 Example: computing a probability

Let $ \beta_0 = -3, \beta_1 = 0.05, \beta_2 = 0.8 $. For a 40-year-old woman:
Logit = -3 + 0.05*40 + 0.8 = -3 + 2 + 0.8 = -0.2.
Probability = $ \frac{1}{1 + e^{0.2}} \approx 0.45 $.

---

#### 💡 Applications in analytics

- **Predicting churn**, **loan default**, **ad clicks**, **purchases**.
- **Estimating the effect of predictors** on a binary outcome while controlling for other variables.
- **Building a propensity score** for quasi-experiments.
- **Baseline classifier** in machine learning (alongside trees and SVM).

**Advantages:**
- Simple interpretation via the odds ratio.
- Outputs probabilities, not just class labels.
- Works well with a moderate number of features.

**Limitations:**
- Assumes linearity in the logit (nonlinear relationships require adding polynomials/splines).
- Sensitive to multicollinearity.
- Does not handle strongly nonlinear boundaries well (in such cases, trees or ensembles are better).

**Key takeaway:** logistic regression is the analyst's workhorse, especially in business problems where interpretability matters. Always check the calibration of probabilities and the discriminative ability (ROC-AUC).
### ✅ Summary

| Topic | Idea | Key concepts | Application |
|------|------|------------------|------------|
| **Logistic regression** | Model of the probability of a binary event | Logit, sigmoid, odds ratio, maximum likelihood | Churn, default, clicks, propensity score |

**Key takeaways:**
- Logistic regression is the main interpretable method for binary classification: it outputs probabilities, not just class labels.
- Coefficients are interpreted through the odds ratio, which makes the model transparent for business.
- Limitations: linearity in the logit, sensitivity to multicollinearity; check the calibration of probabilities and ROC-AUC.

---
Related topics: [Classification metrics](23-classification-metrics.md) · [GLM](26-glm.md) · [Bootstrap](18-bootstrap.md)