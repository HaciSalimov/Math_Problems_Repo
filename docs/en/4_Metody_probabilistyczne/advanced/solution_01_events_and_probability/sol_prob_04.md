# Solution for Task 4: Probability of a Parallel Circuit

## Problem Statement
A fragment of an electrical network consists of two elements connected in parallel: $a_1$ and $a_2$. Let $A_i$ (for $i=1, 2$) denote the event that element $a_i$ remains functional for at least time $t$.

We need to calculate the probability of continuous current flow through this system for at least time $t$, given that:
- $P(A_1) = p$
- $P(A_2) = p$
- $P(A_1 \cap A_2) = p^2$

---

## Solution & Reasoning

### Step 1: Define the Event for Current Flow
Since the elements $a_1$ and $a_2$ are connected in **parallel**, the current will flow if **at least one** of the elements is functional. In set theory, "at least one" corresponds to the union of the two events. 
Let $A$ be the event of continuous current flow:
$$A = A_1 \cup A_2$$

### Step 2: Calculate the Probability of the Union
To find the probability of the union of two events, we use the general addition rule (also known as the Inclusion-Exclusion Principle):
$$P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2)$$

### Step 3: Substitute the Given Values
We substitute the probabilities provided in the problem statement into our formula:
$$P(A) = p + p - p^2$$
$$P(A) = 2p - p^2$$

We can also factor this result to show it in a different form:
$$P(A) = p(2 - p)$$

---
**Commentary / Understanding Check:**
* **Parallel Circuit Logic:** A parallel circuit represents the logical "OR" operation ($\cup$). The system works if $A_1$ works, OR $A_2$ works, OR both work.
* **Inclusion-Exclusion Principle:** Why do we subtract $P(A_1 \cap A_2)$? Because when we add $P(A_1)$ and $P(A_2)$, we count the scenario where *both* elements work twice. Subtracting the intersection corrects this double-counting.
* **Independence:** The fact that $P(A_1 \cap A_2) = P(A_1) \cdot P(A_2) = p \cdot p = p^2$ strongly implies that the failures of elements $a_1$ and $a_2$ are completely **independent** events.