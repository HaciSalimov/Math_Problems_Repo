# Solution for Task 9: Gamma Distribution

## 0. The Random Experiment & Sample Space
* **Experiment:** Measuring the continuous waiting time required until exactly $\alpha$ events occur in a Poisson process.
* **Sample Space ($\Omega$):** The continuous real number line from zero to infinity, $[0, \infty)$.
* **Support of $X$:** $[0, \infty)$. Waiting time cannot be negative.

## 1. PDF and Parameters
Defined by a Shape parameter ($\alpha$) and a Rate parameter ($\lambda$ or $\beta$).

## 5. Shape Dynamics
* **When $\alpha = 1$:** The Gamma distribution perfectly matches the Exponential distribution (waiting for the first event). The PDF drops sharply from the y-axis.
* **When $\alpha > 1$:** The peak moves away from zero. As $\alpha$ grows large, the distribution starts to look symmetric, approximating a Normal distribution curve.

## 6. The Chi-Square Connection
The Chi-Square distribution, which is fundamental to inferential statistics, is not a separate entity. It is mathematically a strict, special case of the Gamma family. Specifically, a Chi-Square distribution with $n$ degrees of freedom is exactly a Gamma distribution where the shape parameter $\alpha = n/2$ and the rate parameter $\beta = 1/2$.

## 8. Practical Applications
Crucial in **Actuarial Science / Insurance** (modeling the size of aggregate insurance claims) and **Hypothesis Testing** (via its Chi-Square variant for goodness-of-fit tests).