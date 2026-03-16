# Solution for Task 8: Probability of Coded Pulse Sequences

## Problem Statement
Coded information consists of seven pulses of types $A$, $B$, and $C$ in the following quantities:
- 4 pulses of $A$
- 2 pulses of $B$
- 1 pulse of $C$
Total pulses: $4 + 2 + 1 = 7$.

Assuming a completely random arrangement of these pulses, we need to find the probability that:
1. The first received pulse will be $A$.
2. The first received pulse will be $A$ or $C$.
3. The first two pulses will be $A$ and $C$ in that order.

---

## Solution & Reasoning

Since the arrangement is random, we can treat this like drawing objects from a bag without replacement. Each of the 7 positions is equally likely to be occupied by any of the available pulses.

### 1. The first received pulse will be $A$
There are 7 possible pulses that could be first, and 4 of them are of type $A$. Using the classical definition of probability:
$$P(\text{1st is } A) = \frac{\text{Number of } A \text{ pulses}}{\text{Total pulses}} = \frac{4}{7}$$

### 2. The first received pulse will be $A$ or $C$
Since a single pulse cannot be both $A$ and $C$ at the same time, these are mutually exclusive events. We simply add their individual probabilities:
$$P(\text{1st is } A \cup \text{1st is } C) = P(\text{1st is } A) + P(\text{1st is } C)$$
$$P(\text{1st is } A \cup \text{1st is } C) = \frac{4}{7} + \frac{1}{7} = \frac{5}{7}$$

### 3. The first two pulses will be $A$ and $C$ in that order
This scenario involves two dependent steps: receiving an $A$ first, AND THEN receiving a $C$ second. We use the general multiplication rule:
$$P(\text{1st is } A \cap \text{2nd is } C) = P(\text{1st is } A) \cdot P(\text{2nd is } C \mid \text{1st is } A)$$

- The probability of receiving $A$ first is $\frac{4}{7}$.
- **If** an $A$ was received first, there are now $7 - 1 = 6$ pulses remaining in the sequence (3 of $A$, 2 of $B$, 1 of $C$).
- The conditional probability of receiving a $C$ second, given that the first was $A$, is $\frac{1}{6}$.

Now, multiply them together:
$$P(\text{sequence } AC) = \frac{4}{7} \cdot \frac{1}{6} = \frac{4}{42} = \frac{2}{21}$$

---
**Commentary / Understanding Check:**
* **Classical Probability:** Parts 1 and 2 rely on a direct ratio of favorable outcomes to total possible outcomes, assuming a uniform distribution (complete randomness).
* **Mutually Exclusive vs. Dependent Events:** Part 2 shows mutually exclusive events (using the Addition Rule). Part 3 illustrates dependent events without replacement (using the Multiplication Rule). The outcome of the first event physically changes the sample space for the second event (from 7 pulses down to 6).