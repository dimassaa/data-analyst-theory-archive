# Probability theory: independent events, conditional probability, Bayes' theorem

🌐 [Русская версия](../topics/02-probability-theory.md)

Probability theory underpins statistical inference, A/B testing, risk assessment, and many machine learning algorithms. Three key concepts are covered here, all especially important for a data analyst.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Independent events | One event does not affect another | [02-independent-events.md](02-independent-events.md) |
| Conditional probability | Probability in a restricted outcome space | [02-conditional-probability.md](02-conditional-probability.md) |
| Bayes' theorem | Revising a hypothesis probability given new data | [02-bayes-theorem.md](02-bayes-theorem.md) |

---

## 📊 Comparison table

| Concept | Formula | Key idea | Typical application |
|---------|---------|----------|---------------------|
| **Independent events** | $ P(A \cap B) = P(A) \cdot P(B) $ | One event does not affect another | Checking model assumptions, random group splitting |
| **Conditional probability** | $ P(A \mid B) = \frac{P(A \cap B)}{P(B)} $ | Probability in a restricted outcome space | Segmentation, funnel analysis, transitions between states |
| **Bayes' theorem** | $ P(H \mid E) = \frac{P(E \mid H) P(H)}{P(E)} $ | Revising a hypothesis probability given new data | Classification, forecasting, A/B tests, model updating |

---

## 🧠 How the concepts connect

- **Independence** is checked via the equality of conditional and unconditional probabilities: $ P(A \mid B) = P(A) $.
- **Bayes' theorem** uses **conditional probabilities** to update beliefs — this is the core of Bayesian statistics (see [20-bayesian-statistics.md](20-bayesian-statistics.md)).

---

## ✅ Summary

Key takeaway: probability theory is not abstract mathematics but a practical tool for the analyst. Understanding conditional probabilities and Bayesian reasoning helps avoid false conclusions, interpret test results correctly, and build more reliable predictive models.

Related topics: [Bernoulli distribution](11-bernoulli-distribution.md) · [Hypothesis testing](04-hypothesis-testing.md) · [Foundations of Bayesian statistics](20-bayesian-statistics.md)

Happy learning! 📈