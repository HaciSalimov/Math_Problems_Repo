# Solution for Task 1: Basic Operations on Events

## Problem Statement
Given the sample space $\Omega = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\}$ and events:
- $A = \{\omega_1, \omega_3, \omega_5\}$
- $B = \{\omega_2, \omega_3, \omega_4\}$

We need to find the results of basic set operations: union, intersection, and differences.

---

## Solution & Reasoning

### 1. Union of events ($A \cup B$)
The union of two events contains all the outcomes that are in $A$, in $B$, or in both.
$$A \cup B = \{\omega_1, \omega_2, \omega_3, \omega_4, \omega_5\} = \Omega$$

### 2. Intersection of events ($A \cap B$)
The intersection of two events contains only the outcomes that are present in **both** $A$ and $B$. The only common element is $\omega_3$.
$$A \cap B = \{\omega_3\}$$

### 3. Difference of events ($B \setminus A$)
This operation means we take all elements of $B$ and remove any elements that also belong to $A$.
- $B = \{\omega_2, \omega_3, \omega_4\}$
- $A$ contains $\omega_3$, so we remove it from $B$.
$$B \setminus A = \{\omega_2, \omega_4\}$$

### 4. Difference of events ($A \setminus B$)
Similarly, we take all elements of $A$ and remove any elements that also belong to $B$.
- $A = \{\omega_1, \omega_3, \omega_5\}$
- $B$ contains $\omega_3$, so we remove it from $A$.
$$A \setminus B = \{\omega_1, \omega_5\}$$

---
**Commentary / Understanding Check:**
* **Sample Space:** The complete set of all possible elementary outcomes is $\Omega$. In this case, the union of $A$ and $B$ covers the entire sample space.
* **Events as Sets:** This problem demonstrates that in probability theory, events are simply sets of outcomes, and logical operations ("OR", "AND", "NOT") directly translate to set operations (Union, Intersection, Difference).