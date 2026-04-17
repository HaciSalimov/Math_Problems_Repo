# Solution for Task 8: Probabilities in Card Drawing

## 1. Setup & Baseline
A standard deck has 52 cards. We apply the multiplication rule, closely observing how the rule of replacement directly affects the denominators in our equations.

---

## 2. Probability Calculations

### A. One Card Drawn ($|\Omega_1| = 52$)
* **Event $A_1$ (Heart):** $$P(A_1) = \frac{13}{52} = \frac{1}{4}$$
* **Event $B_1$ (King):** $$P(B_1) = \frac{4}{52} = \frac{1}{13}$$
* **Event $C_1$ (Not a face card):** $$P(C_1) = \frac{40}{52} = \frac{10}{13}$$

### B. Two Cards Drawn (With Replacement)
* **Event $A_2$ (Both hearts):** $$P(A_2) = \frac{13}{52} \times \frac{13}{52} = \frac{1}{16}$$
* **Event $B_2$ (Same rank):** The first card can be anything. The second must match its rank ($4$ choices out of $52$).
  $$P(B_2) = 1 \times \frac{4}{52} = \frac{1}{13}$$
* **Event $C_2$ (At least one Ace):** Using the complement rule:
  $$1 - P(\text{no Aces}) \implies 1 - \left(\frac{48}{52}\right)^2 = \frac{25}{169}$$

### C. Two Cards Drawn (Without Replacement)
* **Event $A_3$ (Both hearts):** The second draw updates to 12 remaining hearts out of 51 cards.
  $$P(A_3) = \frac{13}{52} \times \frac{12}{51} = \frac{1}{17}$$
* **Event $B_3$ (Same rank):** The first card can be anything. Only 3 matching ranks remain out of the 51 left in the deck.
  $$P(B_3) = 1 \times \frac{3}{51} = \frac{1}{17}$$
* **Event $C_3$ (One King, One Queen):** $$P(C_3) = 2 \times \left(\frac{4}{52} \times \frac{4}{51}\right) = \frac{8}{663}$$
* **Custom Event $D_2'$:** Ace then King.
  $$P(D_2') = \frac{4}{52} \times \frac{4}{51} = \frac{4}{663}$$

---
> **Commentary / Key Takeaway:** > Drawing without replacement introduces **Conditional Probability**. The denominator physically shrinks to 51, and the numerator accurately updates based on the assumption of the first draw's success.