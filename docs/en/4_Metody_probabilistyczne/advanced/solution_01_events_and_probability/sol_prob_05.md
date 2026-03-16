# Solution for Task 5: Probability of Water Volume Intervals

## Problem Statement
We consider the volume of water a concrete culvert can conduct per second. Let $A$ and $B$ be the events corresponding to the water volume falling into specific intervals. We are given:
- $P(A) = 0.6$ (Interval $\langle 125, 250 \rangle$)
- $P(B) = 0.7$ (Interval $(200, 300\rangle$)
- $P(A \cup B) = 0.8$ (The union of these events)

We need to calculate:
1. $P(A')$ (Complementary event to $A$)
2. $P(A \cap B)$ (Intersection of events)
3. $P(A' \cap B')$ (Neither event occurs)

---

## Solution & Reasoning

### 1. Probability of the Complementary Event ($P(A')$)
The probability of an event NOT happening is exactly 1 minus the probability of the event happening.
$$P(A') = 1 - P(A)$$
$$P(A') = 1 - 0.6 = 0.4$$

### 2. Probability of the Intersection ($P(A \cap B)$)
We can use the general addition rule (inclusion-exclusion principle) and rearrange it to solve for the intersection:
$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$
Rearranging for $P(A \cap B)$:
$$P(A \cap B) = P(A) + P(B) - P(A \cup B)$$
$$P(A \cap B) = 0.6 + 0.7 - 0.8$$
$$P(A \cap B) = 1.3 - 0.8 = 0.5$$

### 3. Probability of Neither Event ($P(A' \cap B')$)
To find the probability that the water volume falls outside BOTH intervals, we apply **De Morgan's Laws**, which state that the intersection of complements is the complement of the union:
$$A' \cap B' = (A \cup B)'$$
Now we can simply use the property of complementary events again:
$$P(A' \cap B') = P((A \cup B)') = 1 - P(A \cup B)$$
$$P(A' \cap B') = 1 - 0.8 = 0.2$$

---
**Commentary / Understanding Check:**
* **Complementary Rule:** Sub-task 1 utilizes the axiom that the sum of probabilities of an event and its complement is always 1 (the certain event).
* **Inclusion-Exclusion:** Sub-task 2 shows that if we know the union, we can easily find the intersection (and vice versa) because the overlap must bridge the gap between the sum of individual probabilities and the total union.
* **De Morgan's Laws:** Sub-task 3 elegantly translates a logical "NOT A and NOT B" statement into a "NOT (A or B)" statement, greatly simplifying the calculation.