# Generalized Linear Models (GLM)

🌐 [Русская версия](../topics/26-glm.md)

### 📈 Generalized Linear Models (GLM)

A **Generalized Linear Model** is an extension of classical linear regression that allows modeling a dependent variable with an **arbitrary distribution** (not only normal) and a **nonlinear relationship** between the mean of the response and the linear predictor.

---

#### 🔹 GLM components

Any GLM consists of three elements:

1. **Random component (response distribution):**
   The dependent variable $ Y $ follows a distribution from the exponential family (normal, binomial, Poisson, gamma, etc.).
   $ Y \sim \text{Distribution}(\mu, \phi) $, where $ \mu = E[Y] $ and $ \phi $ is the dispersion parameter.

2. **Systematic component (linear predictor):**
   Linear combination of predictors:
   $$
   \eta = \beta_0 + \beta_1 X_1 + \dots + \beta_p X_p
   $$

3. **Link function:**
   Connects the expected value of the response $ \mu $ with the linear predictor $ \eta $:
   $$
   g(\mu) = \eta \quad \text{or} \quad \mu = g^{-1}(\eta)
   $$
   The choice of the link function depends on the response distribution and the task.

---

#### 🔹 GLM examples

| Model | Distribution of $ Y $ | Link function $ g(\mu) $ | Mean $ \mu = g^{-1}(\eta) $ | Application |
|--------|------------------------|----------------------------|----------------------------------|------------|
| **Linear regression** | Normal | Identity: $ g(\mu)=\mu $ | $ \mu = \eta $ | Continuous response, normal errors |
| **Logistic regression** | Binomial (Bernoulli) | Logit: $ \log\frac{\mu}{1-\mu} $ | $ \mu = \frac{1}{1+e^{-\eta}} $ | Binary response (0/1) |
| **Poisson regression** | Poisson | Log: $ \log(\mu) $ | $ \mu = e^{\eta} $ | Count data (number of events) |
| **Gamma regression** | Gamma | Inverse or log | $ \mu = 1/\eta $ etc. | Positive continuous with skew (e.g., cost) |

---

#### 🔹 Parameter estimation

The parameters $ \beta $ are estimated by **maximum likelihood**. The log-likelihood function depends on the chosen distribution. Maximization is performed numerically (iteratively reweighted least squares, IRLS).

---

#### 🔹 Interpreting the coefficients

- Coefficients $ \beta_j $ show the change in the **linear predictor** $ \eta $ when $ X_j $ increases by one unit (with other factors held fixed).
- The effect on the mean $ \mu $ depends on the inverse link function.
  - For logistic regression: $ e^{\beta_j} $ — the odds ratio.
  - For Poisson regression: $ e^{\beta_j} $ — the multiplier for the mean number of events (relative risk).
  - For linear: $ \beta_j $ — the direct change in $ \mu $.

---

#### 🔹 Advantages of GLM

- A unified theoretical framework for many models.
- Allows modeling different types of data (binary, count, positive) without response transformations that could violate assumptions.
- Estimates remain consistent and asymptotically normal.

**Drawbacks:** the assumption about the distributional form may be wrong; adequacy checks are needed (residuals, plots).

**Applications in analytics:**
- Logistic regression — binary outcomes (churn, conversion).
- Poisson regression — number of requests, orders per period.
- Gamma regression — cost of damage, time-to-event.
- Generalized Additive Models (GAM) — an extension of GLM with nonlinear functions.

**Insight:** Understanding GLM lets you consciously choose the model for your data type instead of trying to "stretch" linear regression over everything.
### ✅ Summary

| Topic | Key concepts | When to use |
|------|------------------|--------------------|
| **GLM** | Link function, response distribution, exponential family | Modeling different types of dependent variable (binary, count, positive) |

**Key takeaways:**
- GLM provides a universal approach to modeling various types of data, unifying linear and logistic regression.
- The link function and response distribution are chosen according to the type of the dependent variable.

---
Related topics: [Regularization](24-regularization.md) · [Linear regression](15-linear-regression.md) · [Logistic regression](19-logistic-regression.md)