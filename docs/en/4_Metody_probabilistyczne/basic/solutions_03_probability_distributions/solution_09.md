# Solution for Task 9: Poisson Model Calculations

## 1. Setup & Baseline
A customer service center receives requests at an average rate of $\lambda = 5$ per hour. Let $X$ be the exact number of requests received in a one-hour interval.
$$X \sim \text{Poisson}(\lambda=5)$$

---

## 2. Probability Calculations

### Scenario A: Exactly 3 requests in one hour
We plug $\lambda = 5$ and $k = 3$ directly into the Poisson formula.
$$P(X = 3) = \frac{e^{-5} \cdot 5^3}{3!}$$
$$P(X = 3) = \frac{e^{-5} \cdot 125}{6} \approx 0.1404$$

### Scenario B: At least one request in one hour
Calculating $P(X \ge 1)$ requires an infinite sum. We instead use the **Complement Rule** ($1 - P(X = 0)$).
$$P(X \ge 1) = 1 - P(X = 0)$$
$$P(X \ge 1) = 1 - \frac{e^{-5} \cdot 5^0}{0!}$$
$$P(X \ge 1) = 1 - e^{-5} \approx 1 - 0.0067 = 0.9933$$