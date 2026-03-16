# Solution for Task 6: Probabilities in Coin Tossing

## 1. Setup & Baseline
Since the coin is fair, $P(H) = P(T) = 0.5$. We utilize Laplace’s classical probability definition: taking the ratio of favorable outcomes to total outcomes.

---

## 2. Probability Calculations

### A. One Coin Toss ($|\Omega_1| = 2$)
* **Event $A_1$ (Heads):** $$P(A_1) = \frac{1}{2}$$
* **Event $B_1$ (Tails):** $$P(B_1) = \frac{1}{2}$$
* **Event $C_1$ (Not tails):** $$P(\{H\}) = \frac{1}{2}$$

### B. Two Coin Tosses ($|\Omega_2| = 4$)
* **Event $A_2$ (Exactly one head):** Favorable outcomes are $\{(H,T), (T,H)\}$.
  $$P(A_2) = \frac{2}{4} = \frac{1}{2}$$
* **Event $B_2$ (At least one head):** $$P(B_2) = \frac{3}{4}$$
* **Event $C_2$ (Both the same):** Favorable outcomes are $\{(H,H), (T,T)\}$.
  $$P(C_2) = \frac{2}{4} = \frac{1}{2}$$

### C. Three Coin Tosses ($|\Omega_3| = 8$)
* **Event $A_3$ (Exactly two heads):** Favorable outcomes are $\{(H,H,T), (H,T,H), (T,H,H)\}$.
  $$P(A_3) = \frac{3}{8}$$
* **Event $B_3$ (At least one tail):** Using the complement rule ($1 - P(\text{all heads})$):
  $$P(B_3) = 1 - \frac{1}{8} = \frac{7}{8}$$
* **Custom Event $D_3$:** First and last toss are different.
  $$P(D_3) = \frac{4}{8} = \frac{1}{2}$$

---
> **Commentary / Key Takeaway:** > For complex events like $B_3$ ("at least one"), calculating the probability using the **Complement Rule** prevents tedious and error-prone manual counting.