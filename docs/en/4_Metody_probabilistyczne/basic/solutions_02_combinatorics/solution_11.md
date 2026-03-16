# Solution

## Task 1# Solution for Task 11: Modeling Outcomes

## 1. Distinguishable vs Indistinguishable Objects
* **Question 1:** Indistinguishable linear arrangement of 11 balls (4R, 4B, 3G) uses the permutation of a multiset.
  $$\frac{11!}{4! \cdot 4! \cdot 3!} = 11,550$$
* **Question 2:** Individually labeled balls ($R_1, R_2\dots$) are completely distinct. We arrange all 11.
  $$11! = 39,916,800$$
* **Question 3:** Recording specific labels creates unique permutations out of same-color balls, massively increasing the sample space because identical objects are now treated as completely distinct.

## 2. Recording Order vs Ignoring Order
* **Question 1:** Order ignored (Combinations). $\binom{11}{3} = 165$
* **Question 2:** Order recorded (k-permutations). $P(11,3) = 990$
* **Question 3:** Recording the order multiplies the fundamental combinations by $3!$ (6) because each distinct subset can be arranged sequentially in 6 different ways.

## 3. PIN Code vs Number
* **Question 1:** 4-digit PIN allows any digit anywhere. $10^4 = 10,000$
* **Question 2:** 4-digit number prohibits '0' at the start. $9 \times 10^3 = 9,000$
* **Question 3 & 4:** A PIN is a sequence of characters, while a "number" mathematically cannot have a leading zero. Additionally, codes like $1234$ and $4321$ are distinct because order fundamentally dictates a security sequence.