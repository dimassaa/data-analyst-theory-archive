# Central Limit Theorem (CLT)

🌐 [Русская версия](../topics/13-central-limit-theorem.md)

### 📊 Central Limit Theorem (CLT)

The Central Limit Theorem (CLT) is one of the most important theorems in mathematical statistics. It explains why the normal distribution appears everywhere and serves as the basis for constructing confidence intervals and hypothesis testing. Without it, modern data analytics and A/B testing are unthinkable.

---

### 🧠 Statement of the CLT

Let $ X_1, X_2, \ldots, X_n $ be independent and identically distributed random variables (i.i.d.) with expected value $ \mu $ and finite variance $ \sigma^2 $.
Then, as $ n \to \infty $, the distribution of the **sample mean** $ \bar{X} = \frac{1}{n} \sum_{i=1}^n X_i $ converges to a normal distribution:

$$
\bar{X} \xrightarrow{d} \mathcal{N}\left( \mu, \frac{\sigma^2}{n} \right)
$$

Equivalently, the standardized statistic:

$$
Z = \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} \xrightarrow{d} \mathcal{N}(0, 1)
$$

**Important:** the CLT does not require the data itself to be normally distributed. The original distribution can be anything (discrete, continuous, skewed), as long as a finite mean and variance exist.

---

### 🔍 Conditions of applicability

1. **Independence of observations** — sample values must not influence each other (e.g., sampling with replacement from a large population).
2. **Identical distribution** — all observations are drawn from the same distribution.
3. **Finite variance** — if the variance is infinite (e.g., the Cauchy distribution), the CLT fails.

In practice the conditions may be slightly violated, but the theorem still gives a good approximation for a sufficiently large $ n $.

---

### 📈 How large should n be?

There is no universal answer — it all depends on the shape of the original distribution.

- If the original distribution is **symmetric and without heavy tails** (uniform, normal), the mean is almost normal already at $ n = 5–10 $.
- If the distribution is **skewed** (exponential, lognormal), $ n = 30–50 $ may be required.
- If the distribution **has strong outliers** or is heavily skewed, maybe $ n > 100 $ is needed.

**Practical rule:** $ n \ge 30 $ is often used as a guideline, but it is always helpful to check graphically or with normality tests.

---

### 🎲 Intuitive example

Imagine rolling a die. The distribution of a single roll is discrete uniform: each value from 1 to 6 has probability 1/6. It does not look like a normal distribution at all.

Now take the **mean** of 2 rolls. Possible values: 1, 1.5, 2, 2.5, ..., 6. The distribution of the mean already becomes more bell-shaped, although it remains discrete.

At $ n = 10 $ rolls, the distribution of the mean is almost perfectly approximated by a normal curve. This is the CLT in action.

---

### 💡 Why is this important for a data analyst?

1. **Confidence intervals**
   Even if the original data are not normal, we can build a confidence interval for the mean using the normal approximation (or the t-distribution when σ is unknown) for a sufficiently large n:
   $$
   \bar{X} \pm z_{\alpha/2} \cdot \frac{s}{\sqrt{n}}
   $$
   This is the basis of most statistical inference.

2. **Hypothesis testing**
   The z-test and t-test rely on the normality of the sample mean (thanks to the CLT), not on the normality of the data itself. So we can compare means in A/B tests even when a metric (e.g., time on site) is not normally distributed.

3. **Estimating precision**
   The standard error of the mean $ SE = \sigma / \sqrt{n} $ shows how accurately the sample mean estimates the true mean. As the sample grows, the error decreases proportionally to $ 1/\sqrt{n} $.

4. **Modeling and simulations**
   Understanding the CLT helps with bootstrapping, estimating test power, and interpreting results.

---

### ⚠️ Common misconceptions

- **"The CLT says the data become normal at large n."**
  False. The data itself does not change: its distribution remains the original one. What becomes normal is the **distribution of the sample mean** (or sum), not the individual observations.

- **"The CLT works for any distribution."**
  Not quite: a finite variance is required. For distributions with heavy tails (e.g., Pareto with parameter α ≤ 2), the CLT may fail, and the mean will not converge to normal.

- **"For n > 30 you can always use the normal approximation."**
  This is a rule of thumb, but if the distribution is extremely skewed or there are outliers, far more observations might be needed, or non-parametric methods adopted.

---

### ✅ Summary

| Characteristic | Description |
|----------------|----------|
| **What it states** | The distribution of the sample mean approaches normal as n grows, regardless of the original distribution (given finite variance). |
| **Conditions** | Independence, identical distribution, finite variance. |
| **Practical value** | Allows building confidence intervals, testing hypotheses, and assessing the precision of the mean. |
| **Limitations** | Inapplicable to distributions with infinite variance; the approximation may require large n under strong skewness. |
| **Typical threshold n** | Often 30, but depends on the shape of the original distribution. |

**Key takeaway:** the CLT is a bridge that allows the normal distribution and the methods based on it (z-tests, confidence intervals) to be applied to a broad class of problems, even when the original data are far from normal. It is the foundation on which a large part of analytical practice rests.

Happy learning! 📈