# Solution for Task 2: Hypergeometric Model (Sampling from a Batch)

## 1. Description of the Random Experiment
We have a finite population of 20 components (5 defective, 15 functional). We draw a sample of 4 components strictly **without replacement**. Because the population physically shrinks, the draws are dependent events.

---

## 2. The Sample Space ($\Omega$) & Random Variable Values
Let $X$ be the random variable representing the number of defective components in our drawn sample of 4.
Since there are 5 defective components in total, we could theoretically draw anywhere from 0 up to 4 defectives.
$$\Omega_X = \{0, 1, 2, 3, 4\}$$

---

## 3. Probability Distribution
The probability of getting exactly $k$ defective components is calculated using combinations (favorable ways over total ways):
$$P(X = k) = \frac{\binom{5}{k} \binom{15}{4-k}}{\binom{20}{4}}$$

---

## 4. Definition of a "Success"
In this hypergeometric model, a **success is defined as drawing a defective component**. We are counting how many of these "successes" end up in our sample of 4.