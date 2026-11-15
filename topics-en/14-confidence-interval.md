# 📏 Confidence interval (CI)
🌐 [Русская версия](../topics/14-confidence-interval.md)

**Confidence interval** — a range of values that, with a given probability (confidence level, typically 95%), covers the true value of a population parameter.

**Formula for the 95% CI of the mean (large sample):**
$$
\bar{x} \pm 1.96 \cdot \text{SE} = \bar{x} \pm 1.96 \cdot \frac{s}{\sqrt{n}}
$$
For small samples, instead of z=1.96, the Student's t-value with df = n-1 is used.

**Example:**
Average order value 500 RUB, SE = 15.
95% CI = (500 - 1.96×15; 500 + 1.96×15) = (500 - 29.4; 500 + 29.4) = **(470.6; 529.4)** RUB.

**Correct interpretation:**
- "If the experiment is repeated many times and a 95% CI is constructed each time, then in 95% of cases the interval will cover the true mean."
- It is **incorrect** to say: "the probability that the true mean lies in the interval is 95%" (the true value is fixed; the interval is random).

**How the CI changes:**
- Larger sample → narrower interval.
- Higher confidence level (99% vs 95%) → wider interval.
- Greater spread → wider interval.

**Applications in analytics:**
- **A/B testing**: if the 95% CI of the conversion uplift does not contain 0, the effect is significant. If the interval contains 0, no conclusion can be drawn.
- **Reports**: instead of "average conversion 3%," it is more correct to write "95% CI: 2.7%–3.4%."
- Estimating the accuracy of model forecasts.

**Key takeaway:** a CI provides more information than a single number: it shows both the estimate and its degree of reliability. In product reports, always include CIs for key metrics — this is a safeguard against overconfidence.

---
← [Back to overview: Confidence intervals](14-confidence-intervals.md) · Related topics: [Standard error](14-standard-error.md), [Statistical significance](05-statistical-significance.md), [CLT](13-central-limit-theorem.md)
