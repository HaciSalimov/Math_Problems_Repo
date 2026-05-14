# Solution for Task 6: Hypergeometric Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** Sampling $n$ items from a finite population of size $N$ strictly *without replacement*, where exactly $K$ items in the population have a distinguished characteristic (e.g., are defective).
* **Sample Space ($\Omega$):** The set of all possible subsets of size $n$ that can be drawn from the population of $N$.
* **Elementary Outcome ($\omega$):** One specific drawn subset of $n$ items.
* **Random Variable $X(\omega)$:** The number of "distinguished" objects present in the drawn sample.
* **Support of $X$:** The integers from $\max(0, n - (N-K))$ up to $\min(n, K)$.

## 1. Probability Mass Function (PMF)
The PMF is derived from pure combinatorics (favorable combinations over total combinations):
$$P(X = k) = \frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}$$

## 3 & 4. Graphical Representation

**Case A: $N=20, K=10, n=5$ (Balanced Population)**
```text
P(X=x)
 0.34 |       * *
 0.13 |     * | | *
 0.01 |   * | | | | *
 0.00 +-|---|---|---|---|--- x
        0   1   2   3   4   5
```

**Case B: $N=20, K=5, n=5$ (Rare Characteristic)**
```text
P(X=x)
 0.44 |     *
 0.29 |     |   *
 0.19 |   * |   |
 0.06 |   | |   |   *
 0.00 +-|---|---|---|---*-*- x
        0   1   2   3   4 5
```

## 5 & 7. Concept and Comparison with Binomial
* **Shape Changes:** As the sample size $n$ increases relative to $N$, the variance shrinks because we are depleting the population, making outcomes more certain.
* **Conceptual Difference:** The Binomial distribution models sampling *with replacement* (trials remain perfectly independent). The Hypergeometric distribution models sampling *without replacement*. Every draw physically removes an item, changing the probabilities for the next draw (trials are dependent). If the population $N$ is massive compared to the sample $n$, the Hypergeometric distribution closely approximates the Binomial.

## 8. Practical Applications
Extensively used in **Ecological Studies** (Capture-Recapture methods to estimate animal populations) and **Destructive Quality Control** (testing items from a limited batch where tested items cannot be returned).