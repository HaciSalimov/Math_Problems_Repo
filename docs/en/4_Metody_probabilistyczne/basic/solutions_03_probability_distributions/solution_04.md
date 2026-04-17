# Solution for Task 4: Poisson Model (Arrival of Events)

## 1. Description of the Random Experiment
We are monitoring a web service over a continuous interval of time (one hour) to count how many discrete error reports arrive. The average rate is constant at 3 reports per hour.

---

## 2. The Sample Space ($\Omega$)
Let $X$ be the total number of error reports received in one hour. We could receive zero reports, or theoretically an infinite number of reports.
$$\Omega_X = \{0, 1, 2, 3, \dots\}$$

---

## 3. Probability Distribution Formula
The Poisson probability mass function is used to find the chance of exactly $k$ arrivals, using the exponential constant $e$:
$$P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}$$
*(For this specific web service, $\lambda = 3$)*.

---

## 4. Interpretation of the Parameter $\lambda$
The parameter **$\lambda$ (lambda)** represents the **average (expected) rate of occurrences** within the specified continuous interval. Here, $\lambda = 3$ means we mathematically expect 3 error reports to arrive every hour.