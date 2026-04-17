# Solution for Task 7: Hypergeometric Model Calculations

## 1. Setup & Baseline
We have a total population of $N = 15$ bulbs.
* Number of defective bulbs (Successes available) = $K = 3$.
* Number of working bulbs = $15 - 3 = 12$.
* We draw a sample of $n = 5$ bulbs **without replacement**.
Let $X$ be the number of defective bulbs in our sample.

---

## 2. Probability Calculation

### Scenario: Exactly 2 defective bulbs
To get exactly 2 defective bulbs, we must also draw exactly 3 working bulbs ($5 - 2 = 3$) to complete our sample of 5. We divide the favorable combinations by the total possible combinations.
$$P(X = 2) = \frac{\binom{3}{2} \times \binom{12}{3}}{\binom{15}{5}}$$
$$P(X = 2) = \frac{3 \times 220}{3003} = \frac{660}{3003} \approx 0.2198$$