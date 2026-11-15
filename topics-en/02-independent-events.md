# 🎲 Independent events

🌐 [Русская версия](../topics/02-independent-events.md)

**Independent events** — events where the occurrence of one does not affect the probability of the other.

**Formal definition:**
Events A and B are independent if:
$$
P(A \cap B) = P(A) \cdot P(B)
$$
or, equivalently,
$$
P(A \mid B) = P(A) \quad \text{and} \quad P(B \mid A) = P(B)
$$
(provided the probabilities are not zero).

**Example:**
We roll a die and flip a coin.
- A = "the coin lands heads" (P = 0.5)
- B = "the die shows 6" (P = 1/6)

These events are independent: the coin flip has no connection to the die.

Probability of heads **and** a 6 on the die:
$$
P(A \cap B) = 0.5 \times \frac{1}{6} = \frac{1}{12}
$$

**Common mistake:**
Independence does not mean "mutual exclusivity". For example, the events "it rains today" and "I take an umbrella" are dependent, since one affects the probability of the other.

**Practical takeaway for the analyst:**
- When analyzing data, it is important to check whether variables really are independent before applying simplified models.
- A/B tests assume that users in the control and treatment groups are independent (which is ensured by random assignment).

---
← [Back to overview: Probability theory](02-probability-theory.md) · Related topics: [Conditional probability](02-conditional-probability.md), [Bayes' theorem](02-bayes-theorem.md)