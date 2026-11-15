# 🛒 Conversion Funnel

🌐 [Русская версия](../topics/09-conversion-funnel.md)

**Conversion funnel** — a description of the user's path to a target action as a sequence of stages. At each step some users "drop off", which is why the shape becomes a funnel.

**Classic example (e-commerce):**
1. Visiting the site
2. Viewing a product
3. Adding to cart
4. Placing an order
5. Payment

**Key funnel metrics:**
- **Conversion** at each stage: the share of users who moved from stage i to stage i+1:
$$
\text{Stage conversion} = \frac{\text{number of users at stage i+1}}{\text{number of users at stage i}} \times 100\%
$$
- **Overall conversion** — the share of users who completed the entire funnel (from the first to the last step).

**Example:**
The site is visited by 10,000 people. Added to cart — 2,000. Purchased — 300.
- Conversion "to cart" = 2000/10000 = 20%.
- Conversion "from cart to purchase" = 300/2000 = 15%.
- Overall conversion = 300/10000 = 3%.

**Why analyze the funnel:**
- Find the stage with the largest percentage of "drop-off" — that is the bottleneck.

**Methods for working with the funnel:**
- A/B testing of individual stages (e.g., simplifying the order form).
- Segment analysis (mobile vs desktop, new vs returning).
- Analysis of time between steps (as in [Test duration analysis](05-test-duration.md)).

**Pitfalls:**
- Counting the funnel "from the point of entry" — not all users enter through the first step.
- Ignoring that a single user may go through the funnel over several visits.
- Mixing different traffic segments.

**Insight:** the funnel shows where users are lost, but not why. Qualitative data (heatmaps, session recordings, surveys) and experiments are needed to find out the reasons.

---
← [Back to overview: Funnels and Cohorts](09-funnels-and-cohorts.md) · Related topics: [Cohort Analysis](09-cohort-analysis.md), [Product Metrics](08-product-metrics.md)