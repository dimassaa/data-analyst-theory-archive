# Hypothesis testing: p-value, type I and II errors, t-test, z-test, chi-squared

🌐 [Русская версия](../topics/04-hypothesis-testing.md)

Testing statistical hypotheses is a fundamental tool of the data analyst for making decisions based on data.

## Basics of the procedure

**A statistical hypothesis** is a claim about the parameters of a distribution or about the properties of a population. Usually two hypotheses are formulated:

- **Null hypothesis (H₀)** — the default claim that we are trying to disprove (e.g., "there is no effect", "there is no difference").
- **Alternative hypothesis (H₁)** — what we want to prove (e.g., "there is an effect", "a difference exists").

**The procedure:**
1. Formulate H₀ and H₁.
2. Choose the significance level α (usually 0.05).
3. Collect data and compute the test statistic.
4. Find the p-value or compare the statistic with the critical value.
5. Make a decision: reject H₀ or fail to reject it.

---

## 🧭 Topics overview

| Topic | File |
|------|------|
| p-value — the key metric | [04-p-value.md](04-p-value.md) |
| Type I and II errors | [04-type-errors.md](04-type-errors.md) |
| Student's t-test | [04-t-test.md](04-t-test.md) |
| z-test | [04-z-test.md](04-z-test.md) |
| Chi-squared test (χ²) | [04-chi-square-test.md](04-chi-square-test.md) |

---

## 📊 Comparison table of tests

| Test | Data type | When used | Statistic |
|----------|------------|-------------------|------------|
| **t-test** | Continuous | Comparing means, σ unknown | t |
| **z-test** | Continuous or proportions | σ known or large samples | z |
| **Chi-squared** | Categorical | Relationship between variables, fit to a distribution | χ² |

**General rule for choosing a test:**
1. If you are comparing the **means** of two groups → t-test (or z when σ is known / n is large).
2. If you are comparing **proportions** or percentages → z-test for proportions (for large n).
3. If you are analyzing **categorical variables** (contingency tables) → chi-squared.

---

## ✅ Summary

- **p-value** — the key metric, but it must be interpreted carefully, taking the effect size and sample size into account.
- **Type I and II errors** — unavoidable risks in any statistical decision. The balance between them is achieved by choosing α and increasing the sample.
- **t-test** — the workhorse tool for comparing means when the variance is unknown.
- **z-test** — convenient for large samples and comparing proportions.
- **Chi-squared** — the main method for working with categorical data.

Related topics: [A/B testing](05-ab-testing.md) · [Confidence intervals](14-confidence-intervals.md) · [Non-parametric tests](17-nonparametric-tests.md) · [ANOVA](16-covariance-and-anova.md)

Understanding these concepts will allow you to run A/B tests correctly, test hypotheses, and make sound decisions based on data. Good luck with your analysis! 📈