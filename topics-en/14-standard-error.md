# 📉 Standard error (SE)
🌐 [Русская версия](../topics/14-standard-error.md)

**Standard error (SE)** — a measure of the inaccuracy of a sample estimate. It shows how far the "sample mean" can deviate from the true population mean.

**Standard error of the mean formula:**
$$
\text{SE} = \frac{s}{\sqrt{n}}
$$
where $ s $ is the sample standard deviation, $ n $ is the sample size.

**Example:**
Among 100 users the average order value is 500 RUB, standard deviation s = 150 RUB.
SE = 150 / √100 = 150 / 10 = **15 RUB**.
This means the sample mean deviates from the true mean by approximately 15 RUB.

**Interpretation:**
- The **larger the sample**, the **smaller the SE** (the denominator √n grows).
- The **smaller the spread** of data, the smaller the SE.
- SE is the "standard deviation of sample means" when the experiment is repeated many times.

**Important distinction:**
- **Standard deviation (SD)** describes the spread of individual observations in the data.
- **Standard error (SE)** describes the inaccuracy of the sample mean estimate. SE is always smaller than SD when n > 1.

**Applications:**
- Constructing confidence intervals (see [Confidence interval](14-confidence-interval.md)).
- Comparing group means in tests (SE is used in the t-statistic).
- Estimating the accuracy of forecasts and regression coefficients.

**Key takeaway:** to halve the uncertainty of an estimate, you need to quadruple the sample size (because SE ∝ 1/√n). This explains why "collecting more data" becomes an expensive endeavor at later stages.

---
← [Back to overview: Confidence intervals](14-confidence-intervals.md) · Related topics: [Confidence interval](14-confidence-interval.md), [Standard deviation](01-standard-deviation.md), [CLT](13-central-limit-theorem.md)
