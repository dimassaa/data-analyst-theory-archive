# 🧠 Bayes' theorem

🌐 [Русская версия](../topics/02-bayes-theorem.md)

**Bayes' theorem** allows us to revise the probability of a hypothesis as new data arrive. It connects the prior probability (before observations) with the posterior (after observations).

**Formula:**
$$
P(H \mid E) = \frac{P(E \mid H) \cdot P(H)}{P(E)}
$$
where:
- $ H $ — hypothesis,
- $ E $ — evidence (observed data),
- $ P(H) $ — **prior probability** of the hypothesis (before accounting for the data),
- $ P(E \mid H) $ — **likelihood** (probability of observing data E if hypothesis H is true),
- $ P(E) $ — **total probability** of the evidence (normalizing constant),
- $ P(H \mid E) $ — **posterior probability** of the hypothesis after accounting for the data.

**Example (medical test):**
A disease occurs in 1% of the population (P(H) = 0.01).
The test is accurate: if the disease is present, the test is positive with probability 99% (P(E|H) = 0.99).
If the disease is absent, the test is falsely positive in 5% of cases (P(E|¬H) = 0.05).
A person got a positive result. What is the probability that they are actually sick?

First, find the total probability of a positive test:
$$
P(E) = P(E|H) \cdot P(H) + P(E|\neg H) \cdot P(\neg H) = 0.99 \cdot 0.01 + 0.05 \cdot 0.99 = 0.0099 + 0.0495 = 0.0594
$$
Now apply Bayes' theorem:
$$
P(H \mid E) = \frac{0.99 \cdot 0.01}{0.0594} \approx 0.1667 \ (\approx 16.7\%)
$$

**Interpretation:**
Despite the high test accuracy, the probability that the patient is actually sick given a positive result is only about 17%. This happens because of the low prior probability of the disease (1%). The Bayesian approach forces us to account for the base rate of the phenomenon.

**Practical applications in data analytics:**
- **Spam filters:** the naive Bayes classifier computes the probability that an email is spam based on the frequency of certain words.
- **A/B testing:** the Bayesian approach allows updating metric probabilities as data arrive and gives more intuitive credible intervals.
- **Model diagnostics:** estimating the probability of customer churn, fraud, equipment failure, and similar events.
- **Updating beliefs:** any new evidence should adjust our confidence in a hypothesis, not completely replace it.

**Key takeaway:** Bayes' theorem is the core of Bayesian statistics (see [Foundations of Bayesian statistics](20-bayesian-statistics.md)), where it is applied to continuous parameters.

---
← [Back to overview: Probability theory](02-probability-theory.md) · Related topics: [Conditional probability](02-conditional-probability.md), [Foundations of Bayesian statistics](20-bayesian-statistics.md)