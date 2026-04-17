# Solution for Task 3: Permutations with Repeated Elements

## 1. Setup & Baseline
When arranging a multiset where some objects are identical, we divide the total permutations ($n!$) by the factorial of each repeating group ($n_1! \cdot n_2! \dots$) to remove duplicate indistinguishable arrangements.

---

## 2. Multiset Calculations

### Question 1: Arrangements of MISSISSIPPI
The word has 11 total letters. Frequencies: M(1), I(4), S(4), P(2).
$$\text{Arrangements} = \frac{11!}{4! \cdot 4! \cdot 2! \cdot 1!} = \frac{39,916,800}{24 \cdot 24 \cdot 2 \cdot 1} = 34,650$$

### Question 2: Arrangements of STATISTICS
The word has 10 total letters. Frequencies: S(3), T(3), I(2), A(1), C(1).
$$\text{Arrangements} = \frac{10!}{3! \cdot 3! \cdot 2! \cdot 1! \cdot 1!} = \frac{3,628,800}{6 \cdot 6 \cdot 2} = 50,400$$

### Question 3: Arrangements of STATISTICS starting with S
If we lock one 'S' in the very first position, we are left with 9 letters to arrange. The new frequencies are: S(2), T(3), I(2), A(1), C(1).
$$\text{Arrangements} = \frac{9!}{2! \cdot 3! \cdot 2! \cdot 1! \cdot 1!} = \frac{362,880}{2 \cdot 6 \cdot 2} = 15,120$$