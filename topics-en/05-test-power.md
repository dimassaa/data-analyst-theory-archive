# 💪 Statistical test power

🌐 [Русская версия](../topics/05-test-power.md)

**Test power (1-β)** — the probability that the test **rejects the null hypothesis when it is indeed false**. In other words, the chance of detecting a real effect if one exists.

**Power formula:**
$$
\text{Power} = P(\text{reject } H_0 \mid H_0 \text{ is false}) = 1 - \beta
$$
where β is the probability of a type II error (missing a real effect).

**What power depends on:**
- **Sample size**: the larger n, the higher the power.
- **Effect size**: the larger the real effect, the easier it is to detect.
- **Significance level α**: the smaller α, the lower the power (at a fixed n).
- **Data variability**: less spread → higher power.

**Example:**
If the real conversion improvement is 10% → 11%, and we sized the sample to detect a 2 p.p. effect with 80% power, then at 80% power in 80% of such experiments we will see a significant result and in 20% we will not (a type II error), even though the effect really exists.

**Key takeaway:** if a test comes back "not significant", the question is: was the power sufficient? If a real effect existed but the sample was small, the test "won't notice" it. Low power makes the conclusion "the change had no effect" unreliable.

---
← [Back to overview: A/B testing](05-ab-testing.md) · Related topics: [Sample size](05-sample-size.md), [Type I and II errors](04-type-errors.md), [Statistical significance](05-statistical-significance.md)