# Solution for Task 12: Mixed Counting Problem

## 1. Student ID Codes
(2 letters from 5 options, followed by 3 digits from 10 options).
* **Q1 (Repetition allowed):** $5^2 \times 10^3 = 25 \times 1000 = 25,000$
* **Q2 (Letters no repeat, digits repeat):** $P(5,2) \times 10^3 = 20 \times 1000 = 20,000$
* **Q3 (No repeats):** $P(5,2) \times P(10,3) = 20 \times 720 = 14,400$

## 2. Medal Assignment
(12 runners, 3 distinct medals).
* **Q1 (Total):** $P(12,3) = 1,320$
* **Q2 (Two particular runners MUST win):** Choose 2 medals out of 3 for them ($\binom{3}{2}$), arrange the medals between the two ($2!$), and assign the 1 remaining medal to the remaining 10 runners ($10$). 
  $$3 \times 2 \times 10 = 60$$

## 3. Committee Selection
(10 students: 6 men, 4 women. Choose 4).
* **Q1 (Total):** $\binom{10}{4} = 210$
* **Q2 (Exactly 2 women):** $\binom{4}{2} \times \binom{6}{2} = 6 \times 15 = 90$
* **Q3 (At least 1 woman):** Total minus committees with no women (only men).
  $$210 - \binom{6}{4} = 210 - 15 = 195$$

## 4. Circular Seating & 5. Passwords
* **Q4.1 (7 people in a circle):** $(7-1)! = 6! = 720$
* **Q4.2 (Two sit together):** $5! \times 2! = 240$
* **Q5.1 (5 chars from 36 options, repeat allowed):** Sequence with repetition. $36^5 = 60,466,176$
* **Q5.2 (No repeat allowed):** k-permutation. $P(36,5) = 45,239,040$