# Solution for Task 8: Geometric Model Calculations

## 1. Setup & Baseline
The probability of a compilation error is $p = 0.1$. The probability of a successful, error-free compilation is $1 - p = 0.9$. Let $X$ be the number of compilations needed to hit the **first error**.
$$X \sim \text{Geo}(p=0.1)$$

---

## 2. Probability Calculations

### Scenario A: The first error appears exactly on the 4th compilation
This means the first 3 compilations must be strictly error-free, followed by an error on the 4th.
$$P(X = 4) = (0.9)^3 \times (0.1)$$
$$P(X = 4) = 0.729 \times 0.1 = 0.0729$$

### Scenario B: The first error appears NO LATER than the 3rd compilation
This is the cumulative probability $P(X \le 3)$. We can calculate this by adding the probabilities of the error occurring on the 1st, 2nd, or 3rd try.
$$P(X \le 3) = P(X=1) + P(X=2) + P(X=3)$$
Alternatively, using the cumulative distribution function (CDF) for the geometric distribution ($1 - (1-p)^k$):
$$P(X \le 3) = 1 - (0.9)^3 = 1 - 0.729 = 0.271$$