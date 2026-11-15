# ✅ Statistical significance in A/B tests

🌐 [Русская версия](../topics/05-statistical-significance.md)

**Statistical significance** is a measure of confidence that the obtained difference between the groups is not random.

**How it is determined:**
- A p-value is calculated for the difference in metrics between the test and control groups.
- A result is considered statistically significant if p-value < α (usually 0.05).

**Example:**
Conversion in the control is 10%, in the test 11.5% with n=4000 per group.
p-value = 0.02 < 0.05 → the result is **statistically significant**: with a 2% error probability we reject the null hypothesis of no difference.

If instead p-value = 0.08 > 0.05 → the result is **not significant at the 5% level**, although the point estimates of the conversions do differ. There is not enough data for a conclusion.

**Interpreting significance:**
- Significance ≠ "large effect". With a large sample you can get a significant but negligible-in-size effect.
- Significance ≠ "certainly reproducible result". There is a type I error probability (α).
- Non-significance ≠ "no effect". The sample may have been insufficient (low power, see [Statistical power](05-test-power.md)).

**Examples of interpretation mistakes:**
- "p=0.049 — significant, but p=0.051 — not significant, let's draw conclusions at the boundary" — forbidden; the significance rule is set before the analysis.
- "A 0.1% increase is significant, so here's the change" — it's important to assess the practical value of the effect (see [Effect size](21-effect-size.md)).

**Key takeaway:** significance indicates that the difference is unlikely to be random, but it does **not** say anything about the magnitude and practical value of the effect. Always look at the confidence interval of the effect, not just the p-value.

---
← [Back to overview: A/B testing](05-ab-testing.md) · Related topics: [p-value](04-p-value.md), [Statistical power](05-test-power.md), [Sample size](05-sample-size.md)