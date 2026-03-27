# Solution for Task 1: Binomial Model (Quality Control)

## 1. Description of the Random Experiment
We are inspecting exactly 3 consecutive screws from a factory. Each screw operates as an independent Bernoulli trial with only two possible outcomes: **Good** ($G$) or **Defective** ($D$). 

---

## 2. The Sample Space ($\Omega$)
If we list all possible sequences of 3 screws, we get $2^3 = 8$ elementary outcomes:
$$\Omega = \{(G,G,G), (G,G,D), (G,D,G), (D,G,G), (G,D,D), (D,G,D), (D,D,G), (D,D,D)\}$$
However, in a Binomial distribution, we define the sample space strictly by the random variable $X$, representing the **number of defective screws**:
$$\Omega_X = \{0, 1, 2, 3\}$$

---

## 3. Probability Distribution
Let $p$ be the probability of a defective screw. The probability of exactly $k$ defectives out of 3 is given by the Binomial formula:
$$P(X = k) = \binom{3}{k} p^k (1-p)^{3-k} \quad \text{for } k \in \{0, 1, 2, 3\}$$

---

## 4. Definition of a "Success"
In probability theory, "success" is simply the event we are mathematically counting. In this quality control model, a **success is finding a defective screw**.