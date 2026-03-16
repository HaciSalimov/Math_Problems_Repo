# Solution for Task 1: Recognizing Counting Models

## 1. Baseline & Methodology
To choose the correct combinatorial model, we must systematically answer the decision tree questions: Are we using all objects? Does order matter? Are repetitions allowed? Are objects distinguishable?

---

## 2. Categorizing the Scenarios

### Scenario 1: Arranging 7 students in a line
All 7 distinct students are being arranged, order strictly matters, and no student can be repeated.
**Model:** Permutation

### Scenario 2: Choosing 4 members of a committee from 12 people
We are selecting only some objects (4 out of 12), and the order of selection does not matter for a standard committee.
**Model:** Combination

### Scenario 3: Assigning gold, silver, and bronze medals among 15 athletes
We are choosing a subset (3 out of 15), order strictly matters (Gold is different from Bronze), and an athlete cannot win twice.
**Model:** k-permutation (ordered selection without repetition)

### Scenario 4: Forming a 6-digit PIN code
We are selecting digits where order matters, and the same digit can be used in multiple positions independently.
**Model:** Sequence with repetition

### Scenario 5: Arranging the letters of the word BANANA
All letters are arranged, but some letters (like the 3 'A's and 2 'N's) are identical and indistinguishable.
**Model:** Permutation with repeated elements

### Scenario 6: Seating 6 people around a round table
All objects are used, but they are arranged in a circle where only the relative position matters, not the absolute seat.
**Model:** Circular permutation