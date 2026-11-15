# Data Analyst Theory Archive

[![Languages](https://img.shields.io/badge/languages-English%20%7C%20Русский-orange)](#-languages)

A structured, interview-ready archive of the **complete statistical and product-analytic theory** a data analyst needs — from descriptive statistics and hypothesis testing to A/B experiments, product metrics, and the ML-adjacent topics every analyst is expected to know.

The archive covers **28 topics** across **182 Markdown files**. Multi-part topics are split into small, focused pages so each concept is its own readable note, connected by "← Back to overview" links.

---

## 🚀 Start here

| Language | Index |
|----------|-------|
| 🇬🇧 English | **[INDEX-en.md](INDEX-en.md)** |
| 🇷🇺 Русский | **[INDEX.md](INDEX.md)** |

Each English page links to its Russian version (and vice versa) via the 🌐 line under the title.

---

## 📚 Topics

<details open>
<summary><strong>The full list — click any topic to open its overview page</strong></summary>

| № | Topic | English | Русский |
|---|-------|---------|---------|
| 1 | Descriptive statistics | [Overview](topics-en/01-descriptive-statistics.md) | [Обзор](topics/01-descriptive-statistics.md) |
| 2 | Probability theory | [Overview](topics-en/02-probability-theory.md) | [Обзор](topics/02-probability-theory.md) |
| 3 | Probability distributions | [Overview](topics-en/03-probability-distributions.md) | [Обзор](topics/03-probability-distributions.md) |
| 4 | Hypothesis testing | [Overview](topics-en/04-hypothesis-testing.md) | [Обзор](topics/04-hypothesis-testing.md) |
| 5 | A/B testing | [Overview](topics-en/05-ab-testing.md) | [Обзор](topics/05-ab-testing.md) |
| 6 | Math analysis & algebra for analysts | [Overview](topics-en/06-math-analysis-and-algebra.md) | [Обзор](topics/06-math-analysis-and-algebra.md) |
| 7 | Correlation analysis | [Overview](topics-en/07-correlation-analysis.md) | [Обзор](topics/07-correlation-analysis.md) |
| 8 | Product metrics (LTV, CAC, retention…) | [Overview](topics-en/08-product-metrics.md) | [Обзор](topics/08-product-metrics.md) |
| 9 | Funnels and cohorts | [Overview](topics-en/09-funnels-and-cohorts.md) | [Обзор](topics/09-funnels-and-cohorts.md) |
| 10 | Quartiles, IQR and outliers | [Overview](topics-en/10-iqr-quantiles-outliers.md) | [Обзор](topics/10-iqr-quantiles-outliers.md) |
| 11 | Bernoulli distribution | [Page](topics-en/11-bernoulli-distribution.md) | [Страница](topics/11-bernoulli-distribution.md) |
| 12 | Linear algebra | [Overview](topics-en/12-linear-algebra.md) | [Обзор](topics/12-linear-algebra.md) |
| 13 | Central Limit Theorem | [Page](topics-en/13-central-limit-theorem.md) | [Страница](topics/13-central-limit-theorem.md) |
| 14 | Confidence intervals | [Overview](topics-en/14-confidence-intervals.md) | [Обзор](topics/14-confidence-intervals.md) |
| 15 | Linear regression | [Overview](topics-en/15-linear-regression.md) | [Обзор](topics/15-linear-regression.md) |
| 16 | Covariance and ANOVA | [Overview](topics-en/16-covariance-and-anova.md) | [Обзор](topics/16-covariance-and-anova.md) |
| 17 | Non-parametric tests | [Overview](topics-en/17-nonparametric-tests.md) | [Обзор](topics/17-nonparametric-tests.md) |
| 18 | Bootstrap | [Page](topics-en/18-bootstrap.md) | [Страница](topics/18-bootstrap.md) |
| 19 | Logistic regression | [Page](topics-en/19-logistic-regression.md) | [Страница](topics/19-logistic-regression.md) |
| 20 | Bayesian statistics | [Page](topics-en/20-bayesian-statistics.md) | [Страница](topics/20-bayesian-statistics.md) |
| 21 | Effect size | [Overview](topics-en/21-effect-size.md) | [Обзор](topics/21-effect-size.md) |
| 22 | Handling missing data | [Page](topics-en/22-missing-data.md) | [Страница](topics/22-missing-data.md) |
| 23 | Binary classification metrics | [Page](topics-en/23-classification-metrics.md) | [Страница](topics/23-classification-metrics.md) |
| 24 | Regularization (L1/L2) | [Page](topics-en/24-regularization.md) | [Страница](topics/24-regularization.md) |
| 25 | Clustering and PCA | [Overview](topics-en/25-clustering-and-pca.md) | [Обзор](topics/25-clustering-and-pca.md) |
| 26 | Generalized Linear Models (GLM) | [Page](topics-en/26-glm.md) | [Страница](topics/26-glm.md) |
| 27 | Time series | [Overview](topics-en/27-time-series.md) | [Обзор](topics/27-time-series.md) |
| 28 | Multi-armed bandits | [Page](topics-en/28-multi-armed-bandits.md) | [Страница](topics/28-multi-armed-bandits.md) |

</details>

> Subtopic pages (e.g. `01-mean.md`, `05-sample-size.md`, `08-ltv.md`) are listed inside each overview page — 182 files in total.

---

## 📁 Repository structure

```
.
├── README.md          ← this landing page
├── INDEX-en.md        ← English index: every topic and subtopic, with file names
├── INDEX.md           ← Russian index
├── topics/            ← Russian original notes
│   ├── 01-descriptive-statistics.md   ← overview page (hub) for topic 01
│   ├── 01-mean.md                     ← one subtopic page
│   ├── …
└── topics-en/         ← English mirror of topics/
```

---

## ✅ What's inside

- **Descriptive statistics, probability theory, distributions** — the mathematical core.
- **Hypothesis testing and experiments** — t-test, z-test, chi-squared, A/B testing, sample size, power, non-parametric tests, bootstrap, multi-armed bandits.
- **Product analytics** — LTV, CAC, retention, churn, ROI/ROMI, ARPU, funnels, cohorts.
- **Regression and modeling basics** — linear/logistic regression, OLS, GLM, regularization, clustering, PCA, classification metrics, time series.

## 🚫 What's deliberately *not* inside

These belong to Data Science / ML engineering rather than a base analyst toolkit:

- Advanced ML (ensembles, neural networks, deep learning)
- NLP, computer vision, recommendation systems
- MLOps, deployment, pipelines, big-data tooling
- Measure-theoretic probability, SVD/eigendecomposition, convex optimization

