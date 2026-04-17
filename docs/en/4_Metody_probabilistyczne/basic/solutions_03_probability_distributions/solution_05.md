# Solution for Task 5: Multinomial Model (Categories of Outcomes)

## 1. Description of the Random Experiment
A player rolls a fair six-sided die 5 consecutive times. Instead of tracking individual numbers, the outcomes are grouped into three distinct categories: small (1-2), medium (3-4), and large (5-6). Each roll is an independent trial.

---

## 2. The Sample Space ($\Omega$)
Let $k_1, k_2, k_3$ represent the number of times small, medium, and large numbers appear, respectively. The sample space consists of all possible combinations of these frequencies that sum up to the total number of rolls (5).
$$\Omega = \{(k_1, k_2, k_3) \mid k_1 + k_2 + k_3 = 5 \text{ and } k_i \ge 0\}$$

---

## 3. Multinomial Distribution Formula
Since each category has 2 numbers out of 6, the probability for each category is exactly the same: $p_1 = p_2 = p_3 = \frac{2}{6} = \frac{1}{3}$.
The probability of getting exactly $k_1$ small, $k_2$ medium, and $k_3$ large numbers is:
$$P(k_1, k_2, k_3) = \frac{5!}{k_1! \cdot k_2! \cdot k_3!} \left(\frac{1}{3}\right)^{k_1} \left(\frac{1}{3}\right)^{k_2} \left(\frac{1}{3}\right)^{k_3}$$

---

## 4. Interpretation of the Parameters
* **$n = 5$**: The total number of independent trials (die rolls).
* **$p_1, p_2, p_3$**: The base probabilities of each respective category occurring in a single trial.
* **$k_1, k_2, k_3$**: The specific number of times we want each category to occur in our sequence of 5 rolls.