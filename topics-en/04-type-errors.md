# ❌ Type I and II errors

🌐 [Русская версия](../topics/04-type-errors.md)

Two types of errors are possible in hypothesis testing:

| | H₀ is true | H₀ is false |
|---------------------|-----------------------------|------------------------------|
| **Fail to reject H₀** | Correct (1 - α) | **Type II error (β)** |
| **Reject H₀** | **Type I error (α)** | Correct (power = 1 - β) |

- **Type I error (α)** — a false-positive conclusion: we rejected H₀ when it is in fact true. The probability of this error equals the significance level α (usually 5%).
- **Type II error (β)** — a false-negative conclusion: we failed to reject H₀ when it is false. The probability β depends on the effect size, the sample size, and α.

**Statistical power (1 - β)** — the probability of correctly rejecting a false H₀.

**Example:**
- H₀: the drug is ineffective.
- Type I error: saying the drug works when it actually does not (a placebo).
- Type II error: saying the drug does not work when it actually does.

**Key takeaway:** Type I and II errors are linked by a trade-off. Reducing α (e.g., to 0.01) lowers the risk of a false-positive conclusion but increases β and reduces power. To increase power, you can increase the sample size or the effect size.

---
← [Back to overview: Hypothesis testing](04-hypothesis-testing.md) · Related topics: [p-value](04-p-value.md), [Statistical power](05-test-power.md)