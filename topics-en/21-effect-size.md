# 📏 Effect size: Cohen's d and relative uplift

🌐 [Русская версия](../topics/21-effect-size.md)

**Effect size** is a measure of the **magnitude** of an effect, independent of sample size. Unlike the p-value (which answers the question "is there an effect?"), effect size answers the question **"how large is the effect?"**. It is a critical bridge between statistical and practical significance.

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|-------|----------|------|
| Cohen's d | Standardized difference between means | [21-cohens-d.md](21-cohens-d.md) |
| Relative uplift | Percentage growth of a metric relative to a base | [21-relative-uplift.md](21-relative-uplift.md) |

---

## 📊 Comparison table

| Aspect | Cohen's d | Relative uplift |
|--------|-----------|-----------------|
| What it measures | The difference between means in standard deviation units | Percentage growth of a metric |
| Formula | $ d = \frac{\bar{x}_1 - \bar{x}_2}{s_p} $ | $ \frac{\text{test} - \text{control}}{\text{control}} \times 100\% $ |
| Units | Dimensionless (z-scale) | Percent |
| What it's for | Comparing effects across different studies | A formulation understandable to business |

**Key rule:**
- **p-value** speaks to statistical significance (whether the effect is due to chance or not).
- **Effect size** speaks to practical significance (how important it is).

---

## ✅ Summary

- Always report effect size together with the p-value — one without the other is only half the truth.
- Cohen's d is convenient for meta-analysis and comparing studies.
- Relative uplift is the most business-friendly way to describe an A/B test result (e.g., "conversion grew by 12%").

Related topics: [Hypothesis testing](04-hypothesis-testing.md) · [A/B testing](05-ab-testing.md) · [Statistical significance](05-statistical-significance.md)

Good luck with your effect-size analysis! 📊