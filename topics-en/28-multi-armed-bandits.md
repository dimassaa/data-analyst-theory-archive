# Multi-armed bandits (MAB)

🌐 [Русская версия](../topics/28-multi-armed-bandits.md)

### 🎰 Multi-armed bandits (Multi-Armed Bandit, MAB)

**A multi-armed bandit** is an adaptive method for allocating traffic (or resources) among several variants (arms) to maximize the total reward (e.g., conversion) during an experiment. Unlike a classical A/B test, where traffic is split evenly for the whole period, MAB dynamically reallocates traffic toward the best variants, reducing losses from showing variants that are clearly weak.

**Origin of the name:** a casino player faces a row of slot machines ("one-armed bandits") with different unknown win probabilities. The task is to maximize the total winnings by choosing machines based on history.

---

#### 🔹 The core idea and the exploration vs. exploitation trade-off

At each step the algorithm must choose which arm to "pull". There are two strategies:

- **Exploitation:** choose the variant that has performed best so far — to maximize the immediate reward.
- **Exploration:** try less-explored variants to learn more about them and possibly find a better one.

An optimal algorithm balances exploration and exploitation. Explore too much — you lose reward; explore too little — you may get stuck on a suboptimal variant.

---

#### 🔹 Popular MAB algorithms

**1. Epsilon-greedy (ε-greedy)**
- With probability $ 1-\varepsilon $ we choose the best known variant (exploitation).
- With probability $ \varepsilon $ we choose a random variant (exploration).
- Simple, but not adaptive: $ \varepsilon $ is usually fixed or decays over time.

**2. UCB (Upper Confidence Bound)**
- For each variant we compute the upper bound of the confidence interval of its mean reward:
  $$
  \text{UCB}_i = \hat{\mu}_i + \sqrt{\frac{2 \ln t}{n_i}}
  $$
  where $ \hat{\mu}_i $ is the current estimate of the mean reward, $ n_i $ is the number of times the variant was shown, and $ t $ is the total number of shows.
- We choose the variant with the maximum UCB.
- The second term encourages rarely shown variants (exploration). Over time it shrinks, increasing exploitation.

**3. Thompson sampling**
- A Bayesian approach: for each variant, a posterior distribution of its conversion probability is maintained (e.g., a beta distribution).
- At each step, for each variant we sample a random value from its posterior distribution.
- We choose the variant with the largest sampled value.
- Naturally balances exploration/exploitation: variants with high uncertainty sometimes yield large samples and get chosen, receiving more data.

**Comparison:**
- Epsilon-greedy is the simplest, but can be inefficient with many variants.
- UCB is deterministic and works well in practice, but is sensitive to assumptions.
- Thompson sampling is probabilistic and usually performs best, especially in non-stationary environments.

---

#### 🔹 Application in A/B testing

A classical A/B test assumes a fixed 50/50 traffic split until statistical significance is reached. Problems:

- During the test, half the users see a potentially worse variant (losses).
- After the test you must wait for it to finish to switch everyone to the best variant.

MAB allows you to:
- **Minimize losses** (regret): the algorithm quickly reallocates traffic to the best variant, reducing exposure of weak ones.
- **Learn continuously**: instead of one final decision — constant adaptation.
- **Work with many variants** (A/B/n) more efficiently than pairwise tests with corrections.

**Limitations of MAB:**
- Doesn't give a clear p-value and confidence intervals like a classical test (though Bayesian superiority probabilities can be computed).
- Sensitive to changes over time: if user behavior changes (e.g., seasonality), the algorithm may switch to a variant that was good in the past but not now.
- Requires fast feedback (reward) — it doesn't suit metrics with a long delay (e.g., LTV) directly.

**When to use it:**
- Many variants (e.g., personalization of headlines, recommendations).
- High interaction frequency and fast feedback (clicks, in-session purchases).
- Strict statistical significance isn't required; maximizing total benefit matters more.

**Example:**
A news site tests 5 headline variants. With Thompson sampling, after a few thousand impressions the algorithm starts giving 80% of the traffic to the best headline while continuing to explore the others in small shares. This increases CTR during the test.

**Key takeaway:** MAB is a powerful tool, but not a replacement for classical A/B testing in all cases. For rigorous conclusions about causality and long-term metrics, a fixed test with a pre-computed sample size is preferable. MAB is good for exploiting knowledge in real time.

### ✅ Summary

| Topic | Key concepts | Application |
|-------|--------------|-------------|
| **Multi-armed bandits** | Exploration vs. exploitation, Epsilon-greedy, UCB, Thompson sampling | Adaptive traffic allocation, real-time optimization |

**Key takeaways:**
- MAB suits dynamic resource allocation when maximizing immediate benefit matters more than rigorous statistical inference.
- The choice between a classical A/B test and MAB depends on your goals: rigorous inference vs. immediate benefit.
- MAB requires fast feedback; it doesn't directly suit metrics with a long delay (LTV).

---
Related topics: [A/B testing](05-ab-testing.md) · [Time series](27-time-series.md) · [Bayesian statistics](20-bayesian-statistics.md)