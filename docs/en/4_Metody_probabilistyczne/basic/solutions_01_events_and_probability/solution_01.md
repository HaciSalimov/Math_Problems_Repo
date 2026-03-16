# Solution for Task 1: Coin Tossing Sample Spaces

## 1. Theoretical Setup
For a fair coin, the elementary outcomes are $H$ (Heads) and $T$ (Tails). Because the coin is tossed sequentially, **the order of outcomes strictly matters**. We construct the sample space using the multiplication principle.

## 2. Step-by-Step Construction
* **One Toss ($\Omega_1$)**: 
  The sample space contains individual, discrete outcomes.
  $$\Omega_1 = \{H, T\} \implies |\Omega_1| = 2$$

* **Two Tosses ($\Omega_2$)**: 
  The outcomes are structured as ordered pairs.
  $$\Omega_2 = \{(H,H), (H,T), (T,H), (T,T)\} \implies |\Omega_2| = 2^2 = 4$$

* **Three Tosses ($\Omega_3$)**: 
  The outcomes are structured as ordered triplets.
  $$\Omega_3 = \{(H,H,H), (H,H,T), \dots, (T,T,T)\} \implies |\Omega_3| = 2^3 = 8$$

---
> **Commentary / Key Takeaway:** > Since each toss is a strictly independent event with 2 possible outcomes, the total size of the sample space for $n$ tosses grows exponentially as $2^n$. Each elementary outcome represents the exact chronological history of the coin.