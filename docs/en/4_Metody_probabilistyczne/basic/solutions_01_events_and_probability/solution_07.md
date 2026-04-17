# Solution for Task 7: Probabilities in Die Rolling

## 1. Setup & Baseline
Each individual face of a fair die has a $1/6$ probability. We analyze the specific subsets within the previously defined exponential sample spaces.

---

## 2. Probability Calculations

### A. One Die Roll ($|\Omega_1| = 6$)
* **Event $A_1$ (Even):** Valid faces are $\{2, 4, 6\}$.
  $$P(A_1) = \frac{3}{6} = \frac{1}{2}$$
* **Event $B_1$ (> 4):** Valid faces are $\{5, 6\}$.
  $$P(B_1) = \frac{2}{6} = \frac{1}{3}$$
* **Event $C_1$ ($\le 3$):** Valid faces are $\{1, 2, 3\}$.
  $$P(C_1) = \frac{3}{6} = \frac{1}{2}$$

### B. Two Die Rolls ($|\Omega_2| = 36$)
* **Event $A_2$ (Sum is 7):** There are 6 favorable combinations.
  $$P(A_2) = \frac{6}{36} = \frac{1}{6}$$
* **Event $B_2$ (Both same):** Outcomes are $\{(1,1), \dots, (6,6)\}$.
  $$P(B_2) = \frac{6}{36} = \frac{1}{6}$$
* **Event $C_2$ (Sum $\ge 10$):** There are 6 favorable combinations (e.g., (4,6), (5,5), (6,4)...).
  $$P(C_2) = \frac{6}{36} = \frac{1}{6}$$

### C. Three Die Rolls ($|\Omega_3| = 216$)
* **Event $A_3$ (Sum is 10):** There are 27 exact permutations.
  $$P(A_3) = \frac{27}{216} = \frac{1}{8}$$
* **Event $B_3$ (Exactly two same):** We calculate this logically using combinatorics:
  $$P(B_3) = \frac{3 \text{ (positions)} \times 6 \text{ (pair faces)} \times 5 \text{ (remaining faces)}}{216} = \frac{90}{216} = \frac{5}{12}$$
* **Event $C_3$ (Two 2s and one 3):** There are exactly 3 valid permutations: $(2,2,3), (2,3,2), (3,2,2)$.
  $$P(C_3) = \frac{3}{216} = \frac{1}{72}$$
* **Custom Event $D_3$:** All completely different dice.
  $$P(D_3) = \frac{6 \times 5 \times 4}{216} = \frac{120}{216} = \frac{5}{9}$$

---
> **Commentary / Key Takeaway:** > When analyzing 216 outcomes, writing down every tree branch is inefficient. Applying **Combinatorics** (as seen in event $B_3$) allows us to mathematically construct the favorable outcomes.