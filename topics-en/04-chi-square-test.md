# 🔲 Chi-squared test (χ²)

🌐 [Русская версия](../topics/04-chi-square-test.md)

**Chi-squared** is used to analyze **categorical data**. There are two main types:

1. **Goodness-of-fit test** — checks whether the observed frequency distribution matches the expected (theoretical) distribution.
2. **Test of independence** — checks whether there is a relationship between two categorical variables in a contingency table.

**Formula:**
$$
\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}
$$
where $ O_i $ is the observed frequency and $ E_i $ is the expected frequency under H₀.

**Degrees of freedom:**
- For goodness of fit: $ df = k - 1 $, where k is the number of categories.
- For independence: $ df = (r-1)(c-1) $, where r and c are the numbers of rows and columns.

**Example (test of independence):**
We check whether sex is related to product preference.

|          | Product A | Product B | Total |
|----------|-----------|-----------|-------|
| Men      | 30        | 20        | 50    |
| Women    | 25        | 35        | 60    |
| Total    | 55        | 55        | 110   |

Expected frequencies under independence: for cell (M, A) = (50*55)/110 = 25, and so on.
We compute χ² ≈ 3.67, df = 1, p-value ≈ 0.055 > 0.05 → at the 5% level we fail to reject H₀; there is no significant relationship.

**Conditions:**
- The observations are independent.
- The expected frequency in each cell must be ≥ 5 (otherwise Fisher's exact test is used).

**Key takeaway:** χ² is often used to analyze contingency tables, test the homogeneity of distributions, and also in tests of normality (e.g., Pearson's goodness-of-fit test).

---
← [Back to overview: Hypothesis testing](04-hypothesis-testing.md) · Related topics: [z-test for proportions](04-z-test.md), [Pearson correlation](07-pearson-correlation.md)