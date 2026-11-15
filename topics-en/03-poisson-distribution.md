# 📞 Poisson distribution

🌐 [Русская версия](../topics/03-poisson-distribution.md)

**Poisson distribution** is a discrete distribution describing the number of events occurring over a fixed interval of time or space, provided the events are independent and occur at a constant average rate.

**Parameter:**
- $ \lambda $ — the average number of events per interval (the rate).

**Formula for the probability of exactly $ k $ events:**
$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad k = 0, 1, 2, \ldots
$$

**Expected value and variance:**
$$
E[X] = \lambda, \quad \text{Var}(X) = \lambda
$$
(note: the variance equals the mean!)

**Conditions of use:**
- the events occur independently of one another,
- the probability of an event in an infinitesimally small interval is proportional to the length of the interval,
- two events cannot occur at the same time.

**Examples:**
- the number of calls to a call center per hour;
- the number of typos on a page of text;
- the number of server failures per day;
- the number of cars passing an intersection per minute.

**Use in analytics:**
- modeling load (traffic, requests to a service);
- analyzing rare events (insurance claims, breakdowns);
- forecasting demand in some services (e.g., the number of orders in an online store per hour).

**Key takeaway:** the Poisson distribution is closely related to the binomial one: if $ n $ is large, $ p $ is small, and $ np = \lambda $ stays constant, the binomial distribution tends to the Poisson. This is useful for rare events in large samples.

---
← [Back to overview: Distributions](03-probability-distributions.md) · Related topics: [Binomial distribution](03-binomial-distribution.md), [CLT](13-central-limit-theorem.md)