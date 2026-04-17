# Solution for Task 6: Binomial Model Calculations

## 1. Setup & Baseline
We are inspecting $n = 10$ parts. The probability of any single part being defective is $p = 0.04$. Consequently, the probability of a part being functional is $1 - p = 0.96$. Let $X$ be the number of defective parts.
$$X \sim \text{Bin}(n=10, p=0.04)$$

---

## 2. Probability Calculations

### Scenario A: Exactly 2 parts are defective
We apply the standard Binomial probability mass function:
$$P(X = 2) = \binom{10}{2} (0.04)^2 (0.96)^8$$
$$P(X = 2) = 45 \times 0.0016 \times 0.7214 \approx 0.0519$$

### Scenario B: At least one part is defective
Calculating probabilities for $X = 1, 2, \dots, 10$ is inefficient. Instead, we use the **Complement Rule** ($1 - P(\text{zero defective parts})$).
$$P(X \ge 1) = 1 - P(X = 0)$$
$$P(X \ge 1) = 1 - \left[ \binom{10}{0} (0.04)^0 (0.96)^{10} \right]$$
$$P(X \ge 1) = 1 - (0.96)^{10} \approx 1 - 0.6648 = 0.3352$$