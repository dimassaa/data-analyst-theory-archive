# 📉 Variance

🌐 [Русская версия](../topics/01-variance.md)

**Variance** — a measure of how spread out the data are around the mean value. It shows how strongly values deviate from the average.

**Sample formula (unbiased estimate):**
$$
s^2 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n - 1}
$$

**Population formula:**
$$
\sigma^2 = \frac{\sum_{i=1}^{n} (x_i - \mu)^2}{n}
$$

**Interpretation:**
The larger the variance, the more spread out the data.

**Example:**
Salaries: 30, 35, 40, 45, 100. Mean = 50.
Deviations: -20, -15, -10, -5, +50. Squares: 400, 225, 100, 25, 2500. Sum = 3250.
Variance (for the population) = 3250 / 5 = **650 (thousand RUB)²**.

**Features:**
- The unit of measurement is the square of the original quantity (e.g., "thousand RUB squared"), which is not always convenient to interpret.
- Always non-negative.

**Key takeaway:** variance is hard to interpret because of its squared units — in practice the standard deviation is used more often.

---
← [Back to overview: Descriptive statistics](01-descriptive-statistics.md) · Related topics: [Standard deviation](01-standard-deviation.md), [Covariance](16-covariance-and-anova.md)