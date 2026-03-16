# Solution for Task 7: k-Permutations

## 1. Setup & Baseline
A k-permutation is an ordered selection of $k$ elements from an $n$-element set without repetition. The formula is $P(n,k) = \frac{n!}{(n-k)!}$.

---

## 2. Ordered Selection Calculations

### Question 1: First three places among 12 runners
Order strictly matters for 1st, 2nd, and 3rd place. We select an ordered 3 from 12.
$$P(12,3) = 12 \times 11 \times 10 = 1,320$$

### Question 2: 4-digit numbers with distinct digits from 1–9
Order matters (a number is a sequence), and digits cannot repeat. We choose an ordered 4 from 9.
$$P(9,4) = 9 \times 8 \times 7 \times 6 = 3,024$$

### Question 3: Divisible by 5
To be divisible by 5, the last digit MUST be '5' (since '0' is not in the set 1-9). The last digit is locked (1 way). We choose an ordered 3 for the remaining positions from the remaining 8 digits.
$$1 \times P(8,3) = 1 \times 8 \times 7 \times 6 = 336$$