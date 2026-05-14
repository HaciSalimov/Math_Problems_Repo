# Solution for Task 7: Negative Binomial Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** Performing repeated, independent Bernoulli trials sequentially until exactly the $r$-th success is achieved.
* **Sample Space ($\Omega$):** All possible sequences of trials ending with a Success and containing exactly $r$ Successes in total.
* **Random Variable $X(\omega)$:** The total number of trials required to observe the $r$-th success.
* **Support of $X$:** $\{r, r+1, r+2, \dots\}$. It is infinite, but strictly starts at $r$ because you cannot achieve $r$ successes in fewer than $r$ trials.

## 1. PMF Formula
The last trial must be a success. The remaining $r-1$ successes can be arranged anywhere in the preceding $k-1$ trials:
$$P(X = k) = \binom{k-1}{r-1} p^r (1-p)^{k-r}$$

## 3 & 4. Graphical Representation

**Case A: $r=2, p=0.5$ (Waiting for 2nd success)**
```text
P(X=x)
 0.25 |   * *
 0.18 |   | |   *
 0.12 |   | |   |   *
 0.07 |   | |   |   |   *
 0.00 +-|---|---|---|---|--- x
        2   3   4   5   6
```

**Case B: $r=4, p=0.5$ (Waiting for 4th success)**
```text
P(X=x)
 0.15 |         * * *
 0.12 |       * | | | *
 0.06 |     * | | | | |
 0.00 +-|---|---|---|---|--- x
        4   5   6   7   8
```

## 5. Parameter Changes
* **When $r$ increases:** The entire distribution shifts to the right (you naturally have to wait longer trials to accumulate more total successes).
* **When $p$ increases:** The distribution shifts to the left and becomes narrower, because high success rates mean you will hit the target $r$ much faster.

## 7. Generalization of the Geometric Distribution
The Negative Binomial distribution is the direct mathematical generalization of the Geometric distribution. If we plug in $r=1$ (waiting for the very first success), the combinatorial term $\binom{k-1}{0}$ becomes 1, and the formula perfectly collapses into the Geometric PMF: $(1-p)^{k-1}p$.

## 8. Practical Applications
Highly relevant in **Epidemiology** (modeling the spread of infectious diseases) and **Reliability Engineering** (evaluating systems that only fail after $r$ redundant components break).