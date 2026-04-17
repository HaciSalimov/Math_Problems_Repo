# Solution for Task 8: Sequences with Repetition

## 1. Setup & Baseline
A sequence of length $k$ over an $n$-element set where order matters and repetition is allowed uses the formula $n^k$. 

---

## 2. Sequence Calculations

### Question 1: 5-digit PIN codes (digits may repeat)
There are 10 available digits (0-9). Each of the 5 positions has 10 independent options.
$$10^5 = 10 \times 10 \times 10 \times 10 \times 10 = 100,000$$

### Question 3: All digits different
If no digit can repeat, this becomes a k-permutation problem. We choose an ordered 5 from 10.
$$P(10,5) = 10 \times 9 \times 8 \times 7 \times 6 = 30,240$$

### Question 2: At least one repeated digit
Using the complement rule: Total possible PIN codes minus the PIN codes where all digits are strictly different.
$$10^5 - P(10,5) = 100,000 - 30,240 = 69,760$$