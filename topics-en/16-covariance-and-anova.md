# 🔄 Covariance and ANOVA
🌐 [Русская версия](../topics/16-covariance-and-anova.md)

**Covariance** measures the joint variation of two variables, and **ANOVA (analysis of variance)** compares the means of several groups through the analysis of variances. Both methods are part of the statistical toolkit for studying relationships and differences.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Covariance | Direction of joint variability of two variables | [16-covariance.md](16-covariance.md) |
| ANOVA | Comparing means across three or more groups | [16-anova.md](16-anova.md) |

---

## 📊 Comparison table

| Aspect | Covariance | ANOVA |
|--------|-----------|-------|
| Question | How do two variables change together? | Do the means of several groups differ? |
| Data type | $ n $ pairs (x, y) — both quantitative | Group (categorical) + quantitative |
| Number of variables | 2 | Factor (groups) + 1 continuous |
| Result | A number (sign + / −) | F-statistic with p-value |
| Relationship to correlation | Normalized covariance = Pearson correlation | F-statistic compares variances |

**How they are connected:**
- Covariance → normalization → Pearson correlation coefficient (see [Pearson correlation](07-pearson-correlation.md)).
- ANOVA compares **between-group variance** with **within-group variance**: F = between-group variance / within-group variance.

---

## ✅ Summary

- **Covariance**: the sign indicates the direction of the relationship (direct/inverse), but the magnitude depends on the scale of the data — hence correlation is more convenient to use.
- **ANOVA**: an extension of the t-test for 3+ groups; it shows whether at least one significant difference exists, without specifying which one (post-hoc tests are needed).

Related topics: [Correlation analysis](07-correlation-analysis.md) · [Hypothesis testing](04-hypothesis-testing.md) · [Non-parametric tests](17-nonparametric-tests.md)

Happy analyzing! 📊
