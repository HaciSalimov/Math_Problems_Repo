# Solution for Task 5: Poisson Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** Observing and counting the number of discrete, random events that occur within a strictly fixed interval of time or region of space.
* **Sample Space ($\Omega$):** The set of all non-negative integers. $\Omega = \{0, 1, 2, 3, \dots\}$.
* **Random Variable $X(\omega)$:** The exact number of events observed in that specific interval.
* **Support of $X$:** $\{0, 1, 2, 3, \dots\}$ extending to infinity.

## 1. PMF and Parameter
* **PMF:** $$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$
* **Parameter $\lambda$ (Lambda):** Represents the expected (average) rate of occurrences within the interval.

## 3 & 4. Graphical Representation (Shape Changes)

**Case A: $\lambda = 1$ (Highly Skewed)**
```text
P(X=x)
 0.36 | * *
 0.18 | | |   *
 0.06 | | |   |   *
 0.00 +-|---|---|---|--- x
        0   1   2   3
```

**Case B: $\lambda = 5$ (Approaching Symmetry)**
```text
P(X=x)
 0.17 |           * *
 0.14 |         * | | *
 0.08 |       * | | | | *
 0.03 |     * | | | | | | *
 0.00 +-|---|---|---|---|---|--- x
        2   3   4   5   6   7
```

## 5. Shape Dynamics
Unlike the Geometric distribution which always peaks at 1, the Poisson peak moves. As $\lambda$ increases, the PMF curve shifts to the right and becomes wider. For large values of $\lambda$ (e.g., $\lambda > 10$), the Poisson distribution becomes highly symmetric, again approximating the Normal distribution curve.

## 6 & 7. Computations
* **$P(X \le k)$:** Computed using the CDF by summing the PMF values from $0$ up to $k$.
* **$P(X \ge k)$:** Because the support goes to infinity, we cannot sum upwards. We must use the complement rule: $1 - P(X \le k-1)$, leveraging the CDF.

## 8. Practical Applications
The Poisson model is the gold standard for modeling "arrival" processes. Examples include **Network Traffic Analysis** (counting HTTP requests hitting a server per minute), **Call Centers** (number of calls received per hour), and **Astronomy** (counting meteorites hitting a specific region per year).