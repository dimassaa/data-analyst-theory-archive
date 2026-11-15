# Bootstrap

🌐 [Русская версия](../topics/18-bootstrap.md)

### 📊 Bootstrap

**Bootstrap** is a method of non-parametric statistical inference based on repeatedly generating "pseudo-samples" from the original data by random sampling **with replacement**. It allows estimating the distribution of almost any statistic (mean, median, correlation coefficient, model parameters, etc.) without strict assumptions about the shape of the underlying distribution.

---

#### 🔁 The core idea

Let there be a sample $ X = (x_1, x_2, \dots, x_n) $ of size $ n $. We want to estimate the accuracy of some statistic $ \hat{\theta} $ (e.g., the mean). Bootstrap works as follows:

1. From the original sample we draw $ n $ elements **randomly with replacement** — obtaining a bootstrap sample $ X^*_1 $.
2. On this sample we compute the statistic of interest $ \hat{\theta}^*_1 $.
3. We repeat steps 1–2 a large number of times $ B $ (usually 1000–10000).
4. We obtain a set of values $ \hat{\theta}^*_1, \hat{\theta}^*_2, \dots, \hat{\theta}^*_B $ that approximates the sampling distribution of the statistic.
5. From this set we can compute the standard error, confidence intervals, bias, etc.

**Key idea:** the original sample is treated as a "miniature population", and bootstrap imitates the process of repeatedly drawing samples from this population.

---

#### 🧮 Example: confidence interval for the mean

Suppose we have 10 values:
$$ 3, 5, 7, 8, 10, 12, 14, 16, 18, 20 $$

The mean $ \bar{x} = 11.3 $. We want a 95% confidence interval for the mean.

**Bootstrap procedure:**
- Randomly select 10 numbers with replacement, e.g., $ (5, 18, 3, 20, 8, 12, 10, 16, 14, 14) $.
- Compute the mean of this bootstrap sample: $ \bar{x}^*_1 = 12.0 $.
- Repeat, say, 5000 times, obtaining 5000 means.
- Sort them and take the 2.5th and 97.5th percentiles — this is the **percentile bootstrap interval**.

If we computed this analytically via the t-distribution, the interval would be similar, but bootstrap does not require the normality assumption.

**Types of bootstrap confidence intervals:**
- **Percentile**: simply take the quantiles of the distribution of bootstrap statistics.
- **Bias-corrected and accelerated (BCa)**: accounts for bias and skewness, more accurate.
- **bootstrap-t**: models the distribution of the studentized statistic.

---

#### 💡 Application in data analytics

- Estimating confidence intervals for metrics whose distribution is unknown (e.g., median, coefficient of variation, quantiles).
- Estimating the accuracy of machine learning model predictions (e.g., bootstrap aggregating or bagging).
- Checking the robustness of A/B test results when assumptions are violated.
- Estimating the bias and variance of parameter estimates.

**Advantages:**
- Does not require normality.
- Applicable to complex statistics.
- Simple to implement (resampling).

**Limitations:**
- The original sample must be representative (random) — otherwise bootstrap will not help.
- Can perform poorly for very small n (< 10).
- Not suitable for strongly dependent data (time series) without special modifications (block bootstrap).

**Insight:** Bootstrap is a "universal hammer" for estimating uncertainty when analytical formulas are unavailable or assumptions are violated. In Python it is easy to implement with `numpy` or `sklearn.utils.resample`.
### ✅ Summary

| Topic | Essence | Key concepts | Application |
|------|------|------------------|------------|
| **Bootstrap** | Resampling with replacement to estimate the distribution of a statistic | Bootstrap samples, standard error, percentile intervals | Confidence intervals without assumptions, assessing model accuracy |

**Key takeaways:**
- Bootstrap is a powerful non-parametric tool for estimating uncertainty: it allows building confidence intervals and assessing the accuracy of estimates without relying on data normality.
- Applicable to complex statistics (median, quantiles, coefficient of variation) and simple to implement.
- Limitations: requires a representative (random) sample; without modifications (block bootstrap) it is incorrectly applied to time series.

---
Related topics: [Confidence intervals](14-confidence-intervals.md) · [Logistic regression](19-logistic-regression.md) · [Bayesian statistics](20-bayesian-statistics.md)