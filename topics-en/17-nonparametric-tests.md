# 🔀 Non-parametric Tests and Multiple Hypothesis Testing

🌐 [Русская версия](../topics/17-nonparametric-tests.md)

**Non-parametric (distribution-free) tests** make no assumptions about the shape of the distribution (e.g., normality), so they are widely used when the classical tests (t-test, ANOVA) are inappropriate due to outliers, small samples, or heavily skewed data. In addition, when testing several hypotheses at once, a **multiple testing correction** is needed to avoid inflating the probability of a type I error.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|------|---------------|------|
| Mann–Whitney test | Comparing two independent groups by ranks | [17-mann-whitney.md](17-mann-whitney.md) |
| Wilcoxon test (signed-rank) | Comparing two dependent (paired) measurements | [17-wilcoxon.md](17-wilcoxon.md) |
| Multiple hypothesis testing | Corrections for repeated testing | [17-multiple-hypothesis-testing.md](17-multiple-hypothesis-testing.md) |

---

## 📊 Comparison table

| Test | Sample type | Idea | Parametric analog |
|------|-------------|------|--------------------------|
| **Mann–Whitney (U)** | Independent groups | Compares distributions/ranks | t-test for independent samples |
| **Wilcoxon (signed-rank)** | Paired (dependent) | Pair differences | Paired t-test |
| **Bonferroni / FDR** | Any (many tests) | Correction for the number of comparisons | — |

---

## 🧠 Which test to use

```
Are the data normal?
├── Yes → t-test (2 groups) or ANOVA (3+)
└── No / outliers present / little data
    ├── 2 independent groups → Mann–Whitney
    ├── 2 paired measurements → Wilcoxon
    └── Many hypotheses in parallel → multiple testing correction
```

**Important:** non-parametric tests check for differences in distributions, not differences in means. They do not require normality, but they are less powerful than parametric tests when the latter's assumptions hold.

---

## ✅ Summary

- Use non-parametric tests when the assumptions of parametric tests cannot be trusted.
- When running many tests simultaneously, always apply multiple testing corrections — otherwise the results are statistically invalid.
- When P > 0.05, check power and effect sizes to understand whether it's "really no effect" or "not enough data."

Related topics: [Hypothesis testing](04-hypothesis-testing.md) · [Effect size](21-effect-size.md) · [Spearman correlation](07-spearman-correlation.md)

Good luck with your statistical analysis! 📊