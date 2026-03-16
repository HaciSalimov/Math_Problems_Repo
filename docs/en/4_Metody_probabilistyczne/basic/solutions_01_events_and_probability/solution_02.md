# Solution for Task 2: Die Rolling Sample Spaces

## 1. Theoretical Setup
We are rolling a fair six-sided die. Each roll is completely independent of the previous one. The base set of outcomes for a single roll is the integers from 1 to 6.

## 2. Step-by-Step Construction
* **One Roll ($\Omega_1$)**: 
  $$\Omega_1 = \{1, 2, 3, 4, 5, 6\} \implies |\Omega_1| = 6$$

* **Two Consecutive Rolls ($\Omega_2$)**: 
  Represented as ordered pairs $(x,y)$.
  $$\Omega_2 = \{(1,1), (1,2), \dots, (6,6)\} \implies |\Omega_2| = 6^2 = 36$$

* **Three Consecutive Rolls ($\Omega_3$)**: 
  Represented as ordered triplets $(x,y,z)$. Drawing a full tree diagram here becomes highly impractical.
  $$\Omega_3 = \{(1,1,1), (1,1,2), \dots, (6,6,6)\} \implies |\Omega_3| = 6^3 = 216$$

---
> **Commentary / Key Takeaway:** > Applying the Fundamental Counting Principle shows that $n$ rolls of a 6-sided die will generate a sample space of size $6^n$. Because order matters, an outcome like $(1, 6)$ is a distinct elementary event from $(6, 1)$.