# Solution for Task 3: Binomial Distribution $Bin(n,p)$

## 0. The Random Experiment & Sample Space
* **Experiment:** Performing $n$ strictly independent Bernoulli trials, where each trial has exactly two outcomes: Success (with probability $p$) or Failure (with probability $1-p$).
* **Sample Space ($\Omega$):** The set of all possible sequences of Successes (S) and Failures (F) of length $n$. For example, if $n=3$, $\Omega = \{SSS, SSF, SFS, SFF, FSS, FSF, FFS, FFF\}$.
* **Elementary Outcome ($\omega$):** One specific string of length $n$, e.g., $\omega = SFS$.
* **Random Variable $X(\omega)$:** The total count of Successes in the entire sequence.
* **Support of $X$:** $\{0, 1, 2, \dots, n\}$.

## 1 & 2. Probability Mass Function (PMF) and Support
The PMF must account for the number of ways to arrange $k$ successes in $n$ trials (the binomial coefficient), multiplied by the probability of one such specific arrangement:
$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

## 3 & 4. Graphical Representation (Shape Changes)

**Case A: $n=6, p = 0.5$ (Symmetric)**
When the probability of success is exactly half, the PMF is perfectly symmetric around its mean ($n/2$).
```text
P(X=x)
 0.3 |       *
 0.2 |     * | *
 0.1 |   * | | | *
 0.0 +-*-----------*- x
       0 1 2 3 4 5 6
```

**Case B: $n=6, p = 0.2$ (Skewed Right)**
When success is rare, the bulk of the probability mass shifts to the lower values, creating a long right tail.
```text
P(X=x)
 0.4 |   *
 0.3 | * |
 0.1 | | |   *
 0.0 +-|-------*-*-*- x
       0 1 2 3 4 5 6
```

## 5. Parameter Analysis
* **When $p$ increases:** The entire distribution slides to the right. The CDF curve remains flat longer and rises sharply near $n$.
* **When $n$ increases:** The variance grows, meaning the PMF curve spreads out. According to the Central Limit Theorem, as $n$ grows very large, the Binomial PMF visually approaches the smooth, symmetric bell curve of the Normal Distribution.

## 6 & 7. Computing Probabilities (Example: $n=10, p=0.5$)
* **Direct PMF:** $P(X = 5) = \binom{10}{5} (0.5)^5 (0.5)^5 = \frac{252}{1024} \approx 0.246$.
* **Using CDF:** To find $P(X \ge 2)$, summing from 2 to 10 is tedious. Using the complement rule with the CDF is highly efficient: $1 - F(1) = 1 - (P(X=0) + P(X=1))$.

## 8. Practical Applications
The Binomial model is the absolute standard for **Quality Control** (e.g., counting the number of defective parts in a batch of $n$ inspected items) and **Clinical Trials** (counting how many patients out of $n$ show recovery after a specific treatment).