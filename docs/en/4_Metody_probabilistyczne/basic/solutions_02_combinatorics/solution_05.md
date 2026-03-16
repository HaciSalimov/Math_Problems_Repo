# Solution for Task 5: Combinations

## 1. Setup & Baseline
A combination is a selection of elements where order does not matter and repetition is not allowed. The formula for choosing $k$ elements from $n$ distinct elements is $\binom{n}{k} = \frac{n!}{k!(n-k)!}$.

---

## 2. Committee Calculations

### Question 1: 4 people chosen from 12 students
Order does not matter in a committee. We simply choose 4 out of 12.
$$\binom{12}{4} = \frac{12!}{4! \cdot 8!} = 495$$

### Question 2: Committee contains a particular student
We lock the particular student into the committee (1 way), leaving 3 spots to fill from the remaining 11 students.
$$1 \times \binom{11}{3} = \frac{11!}{3! \cdot 8!} = 165$$

### Question 3: Committee contains at least one of two particular students
Using the complement rule: Total committees minus the committees containing NEITHER of the two particular students. We choose 4 from the remaining 10.
$$\binom{12}{4} - \binom{10}{4} = 495 - 210 = 285$$

### Question 4: Exactly two women (7 men, 5 women)
We must choose exactly 2 women from the 5 available, and exactly 2 men from the 7 available to complete the 4-person committee.
$$\binom{5}{2} \times \binom{7}{2} = 10 \times 21 = 210$$