# Solution for Task 3: Drawing Cards Sample Spaces

## 1. Setup & Baseline
Let the standard deck be $C$, containing exactly 52 distinct cards. The mathematical methodology changes significantly based on the replacement rule.

---

## 2. Sample Space Construction

### Event 1: One Card Drawn ($\Omega_1$)
The sample space contains all the individual cards in the deck.
$$\Omega_1 = \{c_1, c_2, \dots, c_{52}\} \implies |\Omega_1| = 52$$

### Event 2: Two Draws With Replacement ($\Omega_2$)
The draws remain **independent**. Because the first card is returned, the sample space is a full Cartesian product.
$$\Omega_2 = \{(c_i, c_j) \mid c_i, c_j \in C\} \implies |\Omega_2| = 52 \times 52 = 2704$$

### Event 3: Two Draws Without Replacement ($\Omega_2'$)
The draws become **dependent**. The first card is permanently removed, meaning the second card must be strictly different ($c_i \neq c_j$).
$$\Omega_2' = \{(c_i, c_j) \mid c_i, c_j \in C, c_i \neq c_j\} \implies |\Omega_2'| = 52 \times 51 = 2652$$

---
> **Commentary / Key Takeaway:** > This task beautifully highlights the transition from independent to dependent events. "Without replacement" structurally shrinks the available pool for the second event, strictly preventing identical pairs like (Ace of Spades, Ace of Spades).