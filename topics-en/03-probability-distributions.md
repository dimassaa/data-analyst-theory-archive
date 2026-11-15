# Distributions: normal, binomial, Poisson

🌐 [Русская версия](../topics/03-probability-distributions.md)

The fundamental distributions that a data analyst most often encounters in their work. Understanding their properties is necessary for correct statistical inference, modeling, and forecasting.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Distribution | Data type | Parameters | File |
|---------------|------------|-----------|------|
| Normal (Gaussian) | Continuous | $ \mu, \sigma $ | [03-normal-distribution.md](03-normal-distribution.md) |
| Binomial | Discrete (number of successes) | $ n, p $ | [03-binomial-distribution.md](03-binomial-distribution.md) |
| Poisson | Discrete (number of events) | $ \lambda $ | [03-poisson-distribution.md](03-poisson-distribution.md) |

---

## 📊 Comparison table

| Characteristic | Normal | Binomial | Poisson |
|----------------|------------|--------------|----------|
| **Data type** | Continuous | Discrete (number of successes) | Discrete (number of events) |
| **Parameters** | $ \mu, \sigma $ | $ n, p $ | $ \lambda $ |
| **Expected value** | $ \mu $ | $ np $ | $ \lambda $ |
| **Variance** | $ \sigma^2 $ | $ np(1-p) $ | $ \lambda $ |
| **Shape** | Bell-shaped, symmetric | Depends on $ p $: can be skewed | Skewed to the right (right tail) |
| **When used** | Means, sums, errors | Proportions, binary outcomes | Rare events, counts per interval |
| **Examples** | Height, weight, IQ | Conversion, defects | Calls, failures, traffic |

---

## 🎯 Practical rule for choosing a distribution

- If you are analyzing **means or sums** of a large number of values → think of the normal distribution (CLT).
- If the data are **the number of successes in a fixed number of trials** (e.g., the number of clicks out of N impressions) → binomial.
- If the data are **a count of events per period/area**, and the events are rare relative to the opportunities → Poisson.

**Links between distributions:**
- The binomial distribution is approximated by the **normal** distribution for large $ n $ and moderate $ p $.
- The binomial distribution tends to the **Poisson** distribution for large $ n $, small $ p $, and $ np = \lambda $.
- The same limit transitions underlie the z-test for proportions.

Knowing these three distributions covers most of the basic analyst tasks, from hypothesis testing to forecasting.

Related topics: [Bernoulli distribution](11-bernoulli-distribution.md) · [CLT](13-central-limit-theorem.md) · [Hypothesis testing](04-hypothesis-testing.md)

Happy learning! 📈