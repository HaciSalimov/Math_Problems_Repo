# Solution for Task 3: Geometric Model (Waiting for the First Event)

## 1. Description of the Random Experiment
We observe consecutively printed pages one by one. Each page has a printing error with an independent probability $p$. The experiment instantly stops the moment we find the **very first error**.

---

## 2. The Sample Space ($\Omega$)
Let $X$ be the number of pages inspected until the first error occurs. Since the error could theoretically appear on the first page, or never appear, the sample space goes to infinity.
$$\Omega_X = \{1, 2, 3, 4, \dots\}$$

---

## 3. Probability Distribution
For the first error to occur on the $k$-th page, the first $(k-1)$ pages must be completely error-free (probability $1-p$), followed by exactly one error (probability $p$):
$$P(X = k) = (1-p)^{k-1} p$$

---

## 4. Definition of a "Success"
In the context of the Geometric distribution, a **success is encountering a page that contains a printing error**. The model measures the waiting time (number of trials) required to achieve this first success.