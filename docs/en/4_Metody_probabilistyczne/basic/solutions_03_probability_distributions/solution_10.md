# Solution for Task 10: Multinomial Model Calculations

## 1. Setup & Baseline
We are drawing $n = 6$ candies independently. The base probabilities for each flavor category are:
* Strawberry ($p_1$) = 0.40
* Lemon ($p_2$) = 0.35
* Mint ($p_3$) = 0.25

---

## 2. Probability Calculation

### Scenario: 3 Strawberry, 2 Lemon, and 1 Mint
We want exact frequencies: $k_1 = 3$, $k_2 = 2$, and $k_3 = 1$. Notice that $3 + 2 + 1 = 6$, which perfectly matches $n$. We apply the Multinomial formula:
$$P(3, 2, 1) = \frac{6!}{3! \cdot 2! \cdot 1!} (0.40)^3 (0.35)^2 (0.25)^1$$
$$P(3, 2, 1) = \frac{720}{6 \cdot 2 \cdot 1} (0.064) (0.1225) (0.25)$$
$$P(3, 2, 1) = 60 \times 0.00196 = 0.1176$$