# 📅 A/B test duration

🌐 [Русская версия](../topics/05-test-duration.md)

Test duration is the period over which the calculated sample size is accumulated.

**Formula:**
$$
\text{Days} = \frac{\text{Required sample size}}{\text{Daily traffic} \times \text{Share of users in the test}}
$$

**Example:**
3800 users per group are needed, two groups → 7600 in total.
Daily traffic is 500 visitors, all of them take part in the test.
Days = 7600 / 500 = **15.2** → round up to 16 days at minimum.

**Factors that lengthen the test:**
- Account for the **purchase cycle** — if a user's purchases happen once a month, the test must last at least a month, otherwise you won't see repeat purchases.
- **Calendar effects**: weekly cycles (weekends and weekdays), holidays, the beginning of the month — Monday results are not comparable with Saturday.
- **Slow accumulation**: not all visitors enter the test, and part of the traffic is allocated to other experiments.

**Typical mistakes:**
- Stopping the test ahead of schedule as soon as the p-value drops below 0.05 ("peeking at the data").
- Extending the test until significance appears also distorts the result (significance is just about to appear, and this is already data mining).
- Not accounting for the time users need to get used to the change (novelty effect) — the reaction in the first days can be abnormal.

**Key takeaway:** fix the analysis date **before** the test starts. Both the test duration and the sample size must be determined in advance, otherwise the statistical conclusions become invalid.

---
← [Back to overview: A/B testing](05-ab-testing.md) · Related topics: [Sample size](05-sample-size.md), [Statistical significance](05-statistical-significance.md)