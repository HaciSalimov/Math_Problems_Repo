# Solution for Task 9: Total Probability from Multiple Plants

## Problem Statement
A certain good is produced by 3 plants. The probabilities of producing a first-quality good by these plants are:
- Plant 1: $0.97$
- Plant 2: $0.90$
- Plant 3: $0.86$

We have a batch of exactly three items, one originating from each plant. We randomly take ONE item from this batch. We need to find the probability that this randomly selected item is of first quality.

---

## Solution & Reasoning

### Step 1: Define the Events and Probabilities
Let's define the following events:
- $H_1$: The selected item comes from Plant 1.
- $H_2$: The selected item comes from Plant 2.
- $H_3$: The selected item comes from Plant 3.
- $Q$: The selected item is of first quality.

Since there is exactly one item from each plant in our pool of 3 items, the probability of selecting an item from any specific plant is equal:
$$P(H_1) = P(H_2) = P(H_3) = \frac{1}{3}$$

The conditional probabilities of the item being first quality, given its source plant, are provided in the problem:
$$P(Q | H_1) = 0.97$$
$$P(Q | H_2) = 0.90$$
$$P(Q | H_3) = 0.86$$

### Step 2: Apply the Law of Total Probability
Since $H_1$, $H_2$, and $H_3$ form a complete partition of our sample space (the item must come from exactly one of these plants), we can use the Law of Total Probability to find the overall probability of selecting a first-quality item:
$$P(Q) = P(Q | H_1)P(H_1) + P(Q | H_2)P(H_2) + P(Q | H_3)P(H_3)$$

Substitute the known values into the equation:
$$P(Q) = \left(0.97 \cdot \frac{1}{3}\right) + \left(0.90 \cdot \frac{1}{3}\right) + \left(0.86 \cdot \frac{1}{3}\right)$$
$$P(Q) = \frac{1}{3} \cdot (0.97 + 0.90 + 0.86)$$
$$P(Q) = \frac{1}{3} \cdot (2.73)$$
$$P(Q) = 0.91$$

There is a $91\%$ chance that the randomly selected item is of first quality.

---
**Commentary / Understanding Check:**
* **Uniform Prior Probabilities:** Unlike Task 6 where machines produced in a $3:2$ ratio, here we explicitly have one item from each plant. This makes the probability of choosing from each plant uniformly $\frac{1}{3}$.
* **Total Probability as a Weighted Average:** The Total Probability formula essentially calculates the weighted average of the individual plant probabilities. Because each plant has an equal weight ($\frac{1}{3}$), the overall probability is just the simple arithmetic mean of $0.97, 0.90$, and $0.86$.