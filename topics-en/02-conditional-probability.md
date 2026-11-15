# 🔗 Conditional probability

🌐 [Русская версия](../topics/02-conditional-probability.md)

**Conditional probability** — the probability of event A given that event B has already occurred. Denoted $ P(A \mid B) $.

**Formula:**
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad \text{if } P(B) > 0
$$

**Intuition:**
We restrict the space of elementary outcomes to those where B has occurred, and look at what share of them A occupies.

**Example:**
A deck has 52 cards.
- A = "draw an ace"
- B = "draw a card of the spade suit"

There are 4 aces, 13 spades, and 1 ace of spades.

Unconditional probability of drawing an ace: $ P(A) = 4/52 = 1/13 $.
Conditional probability of drawing an ace given that the card is a spade:
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)} = \frac{1/52}{13/52} = \frac{1}{13}
$$
Here $ P(A \mid B) = P(A) $ — so events A and B are independent (the suit does not affect the card value).

**Another example, with dependence:**
An urn holds 3 red and 2 blue balls. We draw two balls **without replacement**.
- A = "the first ball is red"
- B = "the second ball is red"

Probability that the second ball is red **given** that the first was red:
After the first draw, 2 red and 2 blue balls remain, 4 balls in total.
$$
P(B \mid A) = \frac{2}{4} = 0.5
$$
Whereas the unconditional probability $ P(B) $ equals $ 3/5 = 0.6 $. The events are dependent.

**Practical takeaway:**
Conditional probabilities are the foundation for understanding causal relationships. In data analysis they are used for segmentation (e.g., the probability of a purchase given a visit to a certain page) and for building predictive models.

---
← [Back to overview: Probability theory](02-probability-theory.md) · Related topics: [Independent events](02-independent-events.md), [Bayes' theorem](02-bayes-theorem.md)