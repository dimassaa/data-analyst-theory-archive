# Fundamentals of Bayesian statistics

🌐 [Русская версия](../topics/20-bayesian-statistics.md)

### 🧠 Fundamentals of Bayesian statistics

The Bayesian approach to statistics fundamentally differs from the frequentist one. While frequentist statistics treats probabilities as limiting frequencies of events under infinite repetition of an experiment, the Bayesian approach treats them as a **degree of belief** in a hypothesis, which is updated as new data arrive.

---

#### 📐 Bayes' theorem (briefly)

$$
P(\theta \mid D) = \frac{P(D \mid \theta) \cdot P(\theta)}{P(D)}
$$

- $ \theta $ — model parameter(s) (e.g., mean, coefficient).
- $ D $ — observed data.
- $ P(\theta) $ — **prior distribution**: our belief about $ \theta $ before seeing the data.
- $ P(D \mid \theta) $ — **likelihood**: the probability of observing such data given $ \theta $.
- $ P(D) $ — **normalizing constant (evidence)**, so that the distribution integrates to 1.
- $ P(\theta \mid D) $ — **posterior distribution**: updated belief after accounting for the data.

---

#### 📊 Prior and posterior distributions

The **prior distribution** expresses our knowledge or assumptions about the parameter before analyzing the current data. It can be:
- **Informative** — based on past research, expert estimates (e.g., conversion is usually around 5%).
- **Non-informative (weak)** — expressing minimal information (e.g., a uniform distribution over a wide interval, or a normal with huge variance).
- **Conjugate** — chosen so that the posterior distribution has the same mathematical form as the prior (convenient for analytical computations). Example: a beta prior for a binomial probability.

The **posterior distribution** is the result of applying Bayes' theorem. It combines prior beliefs and data. As the amount of data grows, the posterior depends less on the prior and is increasingly determined by the likelihood.

**Example:**
Suppose we are testing a new button on a website and want to estimate the conversion $ p $.
- A priori we assume $ p $ follows a beta distribution Beta(α=2, β=8) — mean 0.2, moderate confidence.
- We observe 100 visitors and 30 clicks (successes).
- The likelihood is binomial: $ P(D \mid p) \propto p^{30} (1-p)^{70} $.
- The posterior is Beta(2+30, 8+70) = Beta(32, 78). The mean ≈ 32/110 ≈ 0.291.
We obtain an updated estimate of the conversion probability and its uncertainty.

---

#### 🔍 Credible Intervals

Instead of a confidence interval (interpreted in the frequentist sense), Bayesian analysis uses the **credible interval (CrI)**. It is a range of values within which the parameter lies with a given **probability** (e.g., 95%), according to the posterior distribution.

The interpretation is intuitive: "With 95% probability the true conversion rate lies in the interval [0.21, 0.38]." This is exactly what is often incorrectly attributed to confidence intervals in frequentist statistics.

Types of credible intervals:
- **Central (equal-tailed)**: from the 2.5th to the 97.5th percentile of the posterior distribution.
- **Highest Posterior Density Interval (HPDI)**: the narrowest interval containing the given share of probability.

**Example (continued):**
The posterior is Beta(32, 78). The 95% central credible interval can be computed via quantiles: approximately [0.21, 0.38]. That is, with probability 0.95 the conversion rate lies in this range.

---

#### 💡 Application in data analytics

- **A/B testing**: the Bayesian approach allows updating the probabilities of variant effectiveness as data arrive, computing the probability that B is better than A, and stopping the test earlier than the classic frequentist design.
- **Forecasting**: estimating the uncertainty of model predictions (Bayesian neural networks, hierarchical models).
- **Personalization**: Bayesian bandits for adaptive traffic allocation.
- **Parameter estimation** taking expert knowledge and small samples into account.

**Advantages:**
- Natural interpretation of probabilities and intervals.
- Ability to incorporate prior information.
- Flexibility in modeling hierarchical structures.

**Limitations:**
- Computational complexity (MCMC is often required).
- Subjectivity in choosing the prior distribution (can be mitigated by using weak priors).
- Requires a deeper understanding of statistics.

**Insight:** Even if you don't become a Bayesian, understanding Bayesian logic helps avoid misinterpreting frequentist results and gives additional tools for complex problems.
### ✅ Summary

| Topic | Essence | Key concepts | Application |
|------|------|------------------|------------|
| **Bayesian statistics** | Updating beliefs about parameters based on data | Prior/posterior, likelihood, credible interval, MCMC | A/B tests, forecasting with uncertainty, personalization |

**Key takeaways:**
- The Bayesian approach gives intuitive probabilistic statements and incorporates prior knowledge.
- Understanding Bayesian logic helps avoid misinterpreting frequentist results.
- Limitations: computational complexity (MCMC), subjectivity in choosing the prior distribution.

---
Related topics: [Bayes' theorem](02-bayes-theorem.md) · [Multi-armed bandits](28-multi-armed-bandits.md) · [A/B testing](05-ab-testing.md)