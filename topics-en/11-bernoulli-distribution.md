# Bernoulli Distribution

🌐 [Русская версия](../topics/11-bernoulli-distribution.md)

### 🎯 Bernoulli Distribution

**Bernoulli distribution** — the simplest discrete distribution, describing a random experiment with **two possible outcomes**: "success" (1) and "failure" (0). Named after the Swiss mathematician Jakob Bernoulli.

It is the foundation for the binomial distribution and many methods for analyzing binary data.

---

### 📐 Parameters and formula

**Parameter:**
- $ p $ — the probability of success (outcome 1). The probability of failure is $ 1 - p $.

**Probability mass function (PMF):**
$$
P(X = k) =
\begin{cases}
p, & \text{if } k = 1 \ (\text{success}), \\
1 - p, & \text{if } k = 0 \ (\text{failure}).
\end{cases}
$$
Or in general form:
$$
P(X = k) = p^k (1-p)^{1-k}, \quad k \in \{0, 1\}.
$$

**Expected value and variance:**
$$
E[X] = p
$$
$$
\text{Var}(X) = p(1-p)
$$

**Example:**
We flip a coin once. Let "heads" be a success (X=1), "tails" a failure (X=0).
If the coin is fair, $ p = 0.5 $.
Then $ P(X=1) = 0.5 $, $ P(X=0) = 0.5 $.

---

### 🔍 Relationship to the binomial distribution

**Binomial distribution** — the sum of $ n $ independent Bernoulli trials with the same success probability $ p $.
If $ X_i \sim \text{Bernoulli}(p) $ for $ i = 1, \dots, n $ and they are independent, then
$$
Y = X_1 + X_2 + \dots + X_n \sim \text{Binomial}(n, p).
$$

Thus, a Bernoulli trial is one "building block" of a binomial experiment.

---

### 💡 Examples from real analytics

- **Conversion of a single user:** a site visitor either made a purchase (1) or not (0) — this is a Bernoulli trial.
- **Email opening:** a user opened the email (1) or not (0).
- **Banner click:** clicked (1) or not (0).
- **Equipment failure:** during the day a server went down (1) or worked normally (0).

Each such event can be modeled as a Bernoulli random variable with probability $ p $.

---

### 📊 Applications in data analytics

1. **Modeling binary outcomes:**
   Binary features (churn: left/stayed, default: yes/no) are often encoded as 0/1 and analyzed with logistic regression, which estimates $ P(Y=1) = p $ as a function of the predictors.

2. **A/B tests for proportions:**
   Conversion in each group is the proportion of successes (the mean of Bernoulli values). Comparing proportions with a z-test relies on the properties of the binomial distribution, which is built from Bernoulli trials.

3. **Simulations and bootstrap:**
   Generating random binary data (e.g., to estimate test power) is done by sampling from the Bernoulli distribution.

4. **Estimating the probability of an event:**
   The frequency of successes in a sample ($ \hat{p} = \frac{\text{number of successes}}{n} $) is an estimate of the parameter $ p $ of the Bernoulli/binomial distribution.

---

### ⚠️ Important nuances

- **Variance is maximal at $ p = 0.5 $** and decreases toward the extremes. This means that when $ p $ is close to 0 or 1, the outcomes are almost deterministic and the spread is small.
- **Estimating p:** for a series of $ n $ independent Bernoulli trials (i.e., a binomial experiment), an unbiased estimate of $ p $ is the sample proportion of successes $ \hat{p} $.
- **Confidence interval for p:** built based on the normal approximation of the binomial distribution (when $ n $ is large enough and $ p $ is not too close to 0/1) or by exact methods (Clopper–Pearson).

---

### ✅ Summary

| Characteristic | Bernoulli Distribution |
|----------------|------------------------|
| **Type** | Discrete |
| **Parameter** | $ p $ — probability of success |
| **Support** | {0, 1} |
| **PMF** | $ P(X=k) = p^k (1-p)^{1-k} $ |
| **Expected value** | $ p $ |
| **Variance** | $ p(1-p) $ |
| **Relation to binomial** | Sum of n independent Bernoulli trials = Binomial(n, p) |
| **Examples** | Click, purchase, failure, subscription |

**Insight for the analyst:**
The Bernoulli distribution is the simplest model of a binary event, and it underlies the analysis of conversions, A/B tests, and logistic regression. Understanding its properties (especially the variance) helps correctly assess uncertainty in such problems.

Happy learning! 📈