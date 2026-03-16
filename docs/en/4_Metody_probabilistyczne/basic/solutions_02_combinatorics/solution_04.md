# Solution for Task 4: Circular Permutations

## 1. Setup & Baseline
When objects are arranged in a continuous circle, rotations represent the exact same arrangement. To fix the circle, we lock one person in place, leaving $(n-1)!$ permutations for the rest.

---

## 2. Circular Arrangement Calculations

### Question 1: 7 people around a round table
Applying the standard circular permutation formula for $n=7$:
$$\text{Arrangements} = (7-1)! = 6! = 720$$

### Question 2: Two particular people MUST sit together
Bind the two people into a single "block". There are now 6 conceptual entities arranged in a circle, giving $(6-1)! = 5!$ ways. The two people can swap places within their block ($2!$).
$$\text{Arrangements} = 5! \cdot 2! = 120 \cdot 2 = 240$$

### Question 3: Two particular people MUST sit opposite each other
1. Place Person A anywhere at the table (this fixes the circle, 1 way).
2. Person B must sit strictly in the seat opposite to Person A (1 way).
3. The remaining 5 people are linearly arranged in the 5 empty, distinguishable seats left.
$$\text{Arrangements} = 1 \cdot 1 \cdot 5! = 120$$