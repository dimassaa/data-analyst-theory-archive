# 🎯 Binomial distribution

🌐 [Русская версия](../topics/03-binomial-distribution.md)

**Binomial distribution** is a discrete distribution describing the number of "successes" in a series of $ n $ independent trials with the same probability of success $ p $.

**Parameters:**
- $ n $ — number of trials,
- $ p $ — probability of success in a single trial.

**Formula for the probability of exactly $ k $ successes:**
$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}, \quad k = 0, 1, \ldots, n
$$

**Expected value and variance:**
$$
E[X] = np, \quad \text{Var}(X) = np(1-p)
$$

**Conditions of use:**
- each trial has two outcomes (success/failure),
- the trials are independent,
- the probability of success is constant.

**Examples:**
- tossing a coin 10 times: how many heads come up;
- user conversion: how many of 1000 visitors make a purchase;
- the number of defective items in a batch of 50.

**Use in analytics:**
- A/B tests: comparing proportions (conversions) between groups;
- estimating the proportion of a feature in the population from a sample;
- quality control and forecasting the number of failures.

**Key takeaway:** the binomial distribution with large $ n $ and not too small $ p $ is well approximated by the normal distribution (with parameters $ \mu=np $, $ \sigma=\sqrt{np(1-p)} $). This makes it possible to use z-tests for proportions. It is built up from Bernoulli trials (see [Bernoulli distribution](11-bernoulli-distribution.md)).

---
← [Back to overview: Distributions](03-probability-distributions.md) · Related topics: [Bernoulli distribution](11-bernoulli-distribution.md), [Poisson distribution](03-poisson-distribution.md)