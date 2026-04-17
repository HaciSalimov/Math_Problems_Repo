# Solution for Task 6: Combinations in Card Problems

## 1. Setup & Baseline
A standard deck contains 52 cards. A "hand" is an unordered selection of cards without replacement, so we strictly use combinations.

---

## 2. Card Draw Calculations

### Question 1: Exactly 2 hearts in a 5-card hand
There are 13 hearts and 39 non-hearts in a deck. We choose 2 hearts AND 3 non-hearts.
$$\binom{13}{2} \times \binom{39}{3} = 78 \times 9139 = 712,842$$

### Question 2: At least one heart in a 5-card hand
Using the complement rule: Total possible 5-card hands minus the hands that contain NO hearts (chosen purely from the 39 non-hearts).
$$\binom{52}{5} - \binom{39}{5} = 2,598,960 - 575,757 = 2,023,203$$

### Question 3: No face cards (J, Q, K)
There are 12 face cards in a deck ($4 \times 3$), leaving 40 non-face cards. We choose all 5 cards exclusively from the 40 non-face cards.
$$\binom{40}{5} = 658,008$$