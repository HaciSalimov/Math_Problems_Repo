# Solution for Task 10: Normal Distribution $N(\mu, \sigma^2)$

## 0. The Random Experiment & Sample Space
* **Experiment:** Taking a continuous measurement of natural, physical, or human phenomena (e.g., human heights, errors in scientific measurement).
* **Sample Space ($\Omega$):** The entire real number line, $\mathbb{R}$.
* **Support of $X$:** $(-\infty, +\infty)$.

## 1. PDF and Parameters
The famous "Bell Curve" is controlled entirely by two parameters:
* **$\mu$ (Mean):** The center of the distribution.
* **$\sigma^2$ (Variance):** The spread of the distribution.

## 3 & 5. Shape Dynamics (Location and Spread)
* **Influence of $\mu$ (Location):** Changing the mean rigidly slides the entire bell curve left or right along the x-axis. The shape itself does not change.
* **Influence of $\sigma^2$ (Spread):** Increasing the variance makes the bell curve flatter and wider (data is more dispersed). Decreasing the variance makes the curve taller and narrower (data is highly concentrated around the mean).

## 6. Computations and Standardization
Because integrating the Normal PDF is extremely complex, we use standardization. Any $X$ from $N(\mu, \sigma^2)$ can be converted to the Standard Normal $Z \sim N(0,1)$ using the formula:
$$Z = \frac{X - \mu}{\sigma}$$
Once converted, probabilities $P(a \le X \le b)$ can be easily read from standard CDF tables.

## 7. Point Probabilities
As with all continuous variables, the theoretical probability of measuring a continuous value exactly to infinite decimal precision is zero. Thus, $P(X = a) = 0$.

## 8. Practical Applications
The absolute backbone of statistics due to the Central Limit Theorem. Used extensively in **Financial Returns Modeling**, **Error Analysis in Engineering**, and **Standardized Testing** (like IQ or SAT scoring).