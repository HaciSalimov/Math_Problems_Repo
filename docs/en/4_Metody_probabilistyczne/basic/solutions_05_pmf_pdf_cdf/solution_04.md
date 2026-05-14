# Solution for Task 4: Geometric Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** Performing repeated, independent Bernoulli trials sequentially until the *very first* success is achieved, at which point the experiment terminates.
* **Sample Space ($\Omega$):** The set of all possible sequences of Failures (F) terminating in exactly one Success (S). $\Omega = \{S, FS, FFS, FFFS, \dots\}$.
* **Elementary Outcome ($\omega$):** A specific string ending in S, e.g., $\omega = FFS$ (success on the 3rd trial).
* **Random Variable $X(\omega)$:** The number of the trial on which the first success occurs.
* **Support of $X$:** $\{1, 2, 3, 4, \dots\}$. **Why infinite?** Because theoretically, one could flip a coin forever and continue getting Failures. There is no hard upper bound.

## 1. PMF and CDF Formulas
* **PMF:** $P(X = k) = (1-p)^{k-1}p$. (Meaning: $k-1$ failures strictly followed by 1 success).
* **CDF:** $F(k) = 1 - (1-p)^k$.

## 3 & 4. Graphical Representation

**Case A: $p = 0.5$ (Fast Decay)**
```text
P(X=x)
 0.50 | *
 0.25 | |   *
 0.12 | |   |   *
 0.06 | |   |   |   *
 0.00 +-]---|---|---|--- x
        1   2   3   4
```

**Case B: $p = 0.1$ (Slow Decay)**
```text
P(X=x)
 0.10 | * * *
 0.05 | | | |   * *
 0.00 +-]-|-|---|---|--- x
        1 2 3   4   5
```

## 5. Shape Changes
The Geometric PMF is unique because its mode (highest peak) is *always* at $k=1$, regardless of $p$. When $p$ is large, the graph drops exceptionally fast. When $p$ is small, the probability decays very slowly, creating a thick, long right tail.

## 6 & 7. Waiting Time & Tail Probabilities
* **Tail Probability:** $P(X > k) = 1 - P(X \le k) = 1 - F(k) = (1-p)^k$.
* **Interpretation:** This elegant result $(1-p)^k$ is exactly the probability of experiencing $k$ consecutive failures. It represents the probability that our "waiting time" will exceed $k$ trials.

## 8. Practical Applications
Extensively used in **Reliability Engineering** (e.g., how many cycles a machine part can endure before its first failure) and **Inventory Management** (waiting time until the first customer demands a specific rare product).