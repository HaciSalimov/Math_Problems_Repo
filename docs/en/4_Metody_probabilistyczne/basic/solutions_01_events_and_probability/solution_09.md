# Solution for Task 9: Probabilities in Weekly Weather

## 1. Setup & Baseline
Using Task 4's sample space (7 days, $\{S,C,R\}$). 
* Each day is strictly independent.
* The probability for each individual state is $1/3$.
* Therefore, the probability of any specific 7-day sequence is $(1/3)^7$.

---

## 2. Probability Calculations

### Event A: Entire weekend is sunny
Saturday is $S$ ($1/3$) AND Sunday is $S$ ($1/3$). The weather on the other 5 days does not matter.
$$P(A) = \frac{1}{3} \cdot \frac{1}{3} = \frac{1}{9}$$

### Event B: Wed, Thu, Fri are rainy
Three specific, designated days are restricted to $R$ ($1/3$ each).
$$P(B) = \left(\frac{1}{3}\right)^3 = \frac{1}{27}$$

### Event C: At least one day is sunny
We apply the **complement rule**: $1 - P(\text{zero sunny days})$. The probability of any day being non-sunny is $2/3$.
$$P(C) = 1 - \left(\frac{2}{3}\right)^7 = 1 - \frac{128}{2187} = \frac{2059}{2187}$$

### Event D: No rainy day
Every single day must be either $S$ or $C$. The probability of this happening on any given day is $2/3$.
$$P(D) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187}$$

### Event E: Exactly two sunny days
This requires the **Binomial Distribution**. We must choose 2 days out of 7 to be sunny $\binom{7}{2}$. Those 2 days have a probability of $(1/3)^2$, and the remaining 5 days have a probability of $(2/3)^5$. 
$$P(E) = \binom{7}{2} \left(\frac{1}{3}\right)^2 \left(\frac{2}{3}\right)^5 = 21 \cdot \frac{1}{9} \cdot \frac{32}{243} = \frac{224}{729}$$

### Custom Event F: Weather stays exactly the same
The weather is identical for the entire week. There are only 3 such valid sequences: (all S), (all C), or (all R).
$$P(F) = 3 \cdot \left(\frac{1}{3}\right)^7 = \frac{3}{2187} = \frac{1}{729}$$

---
> **Commentary / Key Takeaway:** > Event $E$ is a classic application of Bernoulli trials. We cannot simply multiply fractions; we must account for all $\binom{7}{2} = 21$ different ways those two sunny days could be distributed throughout the week's timeline.