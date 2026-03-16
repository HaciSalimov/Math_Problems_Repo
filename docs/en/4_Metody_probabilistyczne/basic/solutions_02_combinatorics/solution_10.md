# Solution for Task 10: Urn Models

## 1. Setup & Baseline
An urn contains 5 red, 4 blue, and 3 green balls (12 balls total). The counting model shifts dramatically depending on whether the order of drawing is recorded or ignored.

---

## 2. Urn Calculations

### Question 1: Order is ignored (Combinations)
Drawing 3 balls without replacement, ignoring order.
$$\binom{12}{3} = \frac{12!}{3! \cdot 9!} = 220$$

### Question 2: Exactly two red balls (Order ignored)
Choose 2 red from 5, and 1 non-red from the remaining 7 balls.
$$\binom{5}{2} \times \binom{7}{1} = 10 \times 7 = 70$$

### Question 3: Order is recorded (k-permutations)
Drawing 3 balls without replacement, but order matters.
$$P(12,3) = 12 \times 11 \times 10 = 1,320$$

### Question 4: Exactly two red balls (Order recorded)
We take the combinations found in Q2 and multiply by the number of ways to arrange those 3 specific drawn balls ($3!$).
$$70 \times 3! = 70 \times 6 = 420$$