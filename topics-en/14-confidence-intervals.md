# 📏 Confidence intervals: standard error and confidence interval
🌐 [Русская версия](../topics/14-confidence-intervals.md)

**Inferential statistics** — drawing conclusions about a population based on a sample. **Confidence interval (CI)** — a range of values that, with a given level of confidence, contains the true population parameter. It captures the uncertainty of an estimate more precisely than a single "point" figure.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Standard error (SE) | How precisely the sample estimate hits the true value | [14-standard-error.md](14-standard-error.md) |
| Confidence interval | A range covering the true value with a given confidence level | [14-confidence-interval.md](14-confidence-interval.md) |

---

## 📊 How they are connected

```
Confidence interval = point estimate ± critical value × standard error

95% CI ≈ x̄ ± 1.96 × SE        (for normally distributed data, large sample)
95% CI ≈ x̄ ± t(0.975; df) × SE  (when σ is unknown and n is small)
```

| Concept | What it shows | Formula |
|---------|---------------|---------|
| **Standard error of the mean** | Accuracy of the mean estimate | $ \text{SE} = \frac{s}{\sqrt{n}} $ |
| **Confidence interval** | Range of the true mean with confidence 1-α | $ x̄ \pm z \cdot \text{SE} $ |

**Key idea:** the standard error shrinks as the sample grows ($ \propto 1/\sqrt{n} $) — the more data, the narrower the interval and the more precise the estimate.

---

## ✅ Summary

- **SE** is a measure of the precision of a point estimate; it decreases as n grows.
- **CI** is the uncertainty range of an estimate; in practice, the 95% CI is used most often.
- A CI is more informative than a single number: it shows both the estimate and the degree of confidence.
- CIs are widely used in A/B testing: overlapping CIs for two groups indicate that differences are not statistically significant.

Related topics: [CLT](13-central-limit-theorem.md) · [Hypothesis testing](04-hypothesis-testing.md) · [Standard deviation](01-standard-deviation.md) · [A/B testing](05-ab-testing.md)

Happy learning! 📊
