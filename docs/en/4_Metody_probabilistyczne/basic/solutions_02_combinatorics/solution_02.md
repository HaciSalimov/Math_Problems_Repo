# Solution for Task 2: Permutations

## 1. Setup & Baseline
A permutation is an arrangement of all elements in a set where order matters and repetition is not allowed. The formula is $P_n = n!$.

---

## 2. Arrangement Calculations

### Question 1: Arranging 8 different books on a shelf
All 8 distinct books are arranged in a linear row.
$$P_8 = 8! = 40,320$$

### Question 2: 8 people, two MUST sit next to each other
We bind the two specific people together into a single "block". This leaves us with 7 total items (6 individuals + 1 block) to arrange. The two people can also swap places within their block ($2!$).
$$\text{Arrangements} = 7! \cdot 2! = 5040 \cdot 2 = 10,080$$

### Question 3: 8 people, two must NOT sit next to each other
We use the sum rule/complement logic. We take the total unrestricted arrangements and subtract the arrangements where they sit together.
$$\text{Arrangements} = 8! - (7! \cdot 2!) = 40320 - 10080 = 30,240$$

### Question 4: Ordering 10 questions if the first is fixed
Since the 1st position is permanently locked, we only have the remaining 9 questions left to arrange linearly.
$$\text{Arrangements} = 9! = 362,880$$