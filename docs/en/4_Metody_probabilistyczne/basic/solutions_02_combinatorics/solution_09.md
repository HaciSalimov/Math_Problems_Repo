# Solution for Task 9: Digit Restrictions

## 1. Setup & Baseline
Unlike a PIN code, a standard "number" cannot start with the digit '0'. The first position only has 9 options (1-9), while other positions have 10 (0-9).

---

## 2. Number Calculations

### Question 1: Total 5-digit numbers
The first digit has 9 options. The remaining 4 digits each have 10 independent options.
$$9 \times 10 \times 10 \times 10 \times 10 = 9 \times 10^4 = 90,000$$

### Question 2: Even 5-digit numbers
The last digit must be even (0, 2, 4, 6, 8 $\implies$ 5 options). The first digit cannot be 0 (9 options). The middle 3 can be anything (10 options each).
$$9 \times 10 \times 10 \times 10 \times 5 = 45,000$$

### Question 3: No repeated digits
The first digit has 9 options (1-9). The second digit has 9 options (0 is now available, but the first digit is excluded). The rest follow $8 \times 7 \times 6$.
$$9 \times 9 \times 8 \times 7 \times 6 = 27,216$$

### Question 4: At least one repeated digit
Total 5-digit numbers minus the 5-digit numbers with completely distinct digits.
$$90,000 - 27,216 = 62,784$$