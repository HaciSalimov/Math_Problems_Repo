# Solution for Task 6: Total Probability and Bayes' Theorem

## Problem Statement
Identical products from 2 automated machines are on a conveyor belt. 
- The production ratio of Machine 1 to Machine 2 is $3:2$.
- Machine 1 produces $65\%$ first-grade products.
- Machine 2 produces $85\%$ first-grade products.

We need to calculate:
1. The probability that a randomly selected product is first-grade (using the Total Probability formula).
2. The probability that a product was made by Machine 1, *given* that it is already known to be first-grade (using Bayes' Theorem).

---

## Solution & Reasoning

### Step 1: Define Events and A Priori Probabilities
Let's define the fundamental events:
- $M_1$: The product was manufactured by Machine 1.
- $M_2$: The product was manufactured by Machine 2.
- $F$: The product is of first-grade quality.

From the production ratio $3:2$, we can determine the probabilities of selecting a product from each machine:
$$P(M_1) = \frac{3}{3 + 2} = \frac{3}{5} = 0.60$$
$$P(M_2) = \frac{2}{3 + 2} = \frac{2}{5} = 0.40$$

We are also given the conditional probabilities of a product being first-grade depending on the machine:
$$P(F | M_1) = 0.65$$
$$P(F | M_2) = 0.85$$

### 1. Total Probability of a First-Grade Product ($P(F)$)
Since a product must come from either Machine 1 or Machine 2 (they form a partition of the sample space), we use the Law of Total Probability:
$$P(F) = P(F | M_1) \cdot P(M_1) + P(F | M_2) \cdot P(M_2)$$
$$P(F) = (0.65 \cdot 0.60) + (0.85 \cdot 0.40)$$
$$P(F) = 0.39 + 0.34 = 0.73$$
So, there is a $73\%$ chance that a randomly selected product is first-grade.

### 2. Probability it came from Machine 1 given it is First-Grade ($P(M_1 | F)$)
Now, we have new information: the product *is* first-grade. We want to update our belief about which machine produced it. We use Bayes' Theorem:
$$P(M_1 | F) = \frac{P(F | M_1) \cdot P(M_1)}{P(F)}$$
$$P(M_1 | F) = \frac{0.39}{0.73}$$
$$P(M_1 | F) \approx 0.5342 \quad (\text{or } 53.42\%)$$

---
**Commentary / Understanding Check:**
* **Total Probability:** Sub-task 1 shows how to find the overall probability of an event ($F$) when that event can occur through multiple distinct paths or causes ($M_1$ and $M_2$).
* **Bayesian Updating:** Sub-task 2 is the core of Bayesian inference. Before testing the product, our "prior" belief that it came from Machine 1 was $60\%$. However, after observing the "evidence" that the product is first-grade, our "posterior" belief drops to $53.42\%$. Why? Because Machine 2 is much better at producing first-grade items ($85\%$ vs $65\%$), so finding a first-grade item slightly increases the likelihood that Machine 2 made it.