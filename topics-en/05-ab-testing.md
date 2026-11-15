# 🧪 A/B testing: sample size, test duration, statistical significance, power

🌐 [Русская версия](../topics/05-ab-testing.md)

**A/B test** is an experiment in which users are randomly shown two (or more) versions of a product, and the versions are compared to see which one performs better on the target metric. Random assignment makes the compared groups statistically comparable, which allows drawing conclusions about the causal effect of the changes.

A/B tests are the main tool of product analytics and marketing for making evidence-based decisions instead of relying on "intuition" and "personal opinion".

This is an overview page (hub): each topic has its own file.

---

## 🧭 Topics overview

| Topic | Key idea | File |
|------|---------------|------|
| Sample size | How many users are needed for a reliable result | [05-sample-size.md](05-sample-size.md) |
| Test duration | How many weeks the experiment runs for | [05-test-duration.md](05-test-duration.md) |
| Statistical significance | When a result can be considered reliable | [05-statistical-significance.md](05-statistical-significance.md) |
| Statistical power | The probability of detecting a real effect | [05-test-power.md](05-test-power.md) |

---

## 📊 How the parameters are related

```
            ┌──────────────────────────────┐
            │       Sample size (n)        │
            │          determines:         │
            │   ┌──────────────────────┐   │
            │   │    Test duration     │   │
            │   └──────────────────────┘   │
            │   ┌──────────────────────┐   │
            │   │   Significance (α)   │   │
            │   └──────────────────────┘   │
            │   ┌──────────────────────┐   │
            │   │      Power (1-β)     │   │
            │   └──────────────────────┘   │
            └──────────────────────────────┘
```

| Parameter | What it defines | Who chooses |
|----------|------------|--------------|
| Significance level α | Risk of a false positive conclusion | Analyst (usually 5%) |
| Power 1-β | Chance of catching a real effect | Analyst (usually 80%) |
| MDE (minimal detectable effect) | The effect that must not be missed | Analyst + product owner |
| Sample size n | Calculated parameter | Computed from α, β, MDE |

**Key rule:** never "peek" at the data and stop the test as soon as the p-value becomes significant — this distorts the results. The sample size and the analysis date are determined **before** the experiment starts.

---

## ✅ Summary

- **Sample size** is calculated before the launch: it depends on α, power and the minimum effect that needs to be caught.
- **Test duration** = the time needed to accumulate the required sample size, taking calendar effects into account (weeks, holidays).
- **Statistical significance** is reached when the p-value < α on the full sample.
- **Power** — the chance of not missing a real effect; the larger the sample, the higher the power.

Before running any A/B test, be sure to calculate the sample size and fix the schedule in advance.

Related topics: [Hypothesis testing](04-hypothesis-testing.md) · [Confidence intervals](14-confidence-intervals.md) · [Effect size](21-effect-size.md)

Happy experimenting! 📈