# Solution for Task 8: Beta Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** A continuous experiment mapping proportions, probabilities, or percentages confined strictly to the interval $[0,1]$.
* **Sample Space ($\Omega$):** The continuous mathematical interval $[0,1]$.
* **Random Variable $X(\omega)$:** The specific proportion value, $X(\omega) = \omega$.
* **Support of $X$:** $[0,1]$.

## 1. PDF and Parameters
The PDF is defined by two shape parameters, $\alpha$ (Alpha) and $\beta$ (Beta), which act as "pseudo-counts" of successes and failures.

## 3, 4 & 5. Shape Dynamics
Unlike most distributions, the Beta distribution can take wildly different shapes based on its parameters:
* **Symmetric:** When $\alpha = \beta > 1$, it forms a beautiful bell curve perfectly centered at 0.5. (If $\alpha = \beta = 1$, it becomes a flat Uniform distribution).
* **Skewed Right:** When $\alpha < \beta$, the peak leans heavily to the left (closer to 0).
* **Skewed Left:** When $\alpha > \beta$, the peak leans heavily to the right (closer to 1).
* **U-Shaped:** When $\alpha < 1$ and $\beta < 1$, the density is concentrated strictly near the endpoints 0 and 1, dipping in the middle.

## 7. Continuous Probabilities
For any continuous distribution like the Beta, the probability of the variable taking one infinitely precise point is zero ($P(X = a) = 0$). Instead, probabilities are calculated as the physical area (the mathematical integral) under the PDF curve between two boundaries: $P(a \le X \le b)$.

## 8. Practical Applications
The primary tool in **Bayesian Statistics** (used as a prior distribution to model beliefs about probabilities) and **Project Management (PERT)** to model expected task completion times.