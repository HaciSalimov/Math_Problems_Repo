# Solution for Task 7: Signal Transmission and Interference

## Problem Statement
On a communication line, signals are transmitted as code combinations: $111$ or $000$.
- A priori probabilities: $P(S_{111}) = 0.65$ and $P(S_{000}) = 0.35$.
- Probability of an error for a single symbol (1 received as 0, or 0 received as 1): $p_e = 0.2$.
- Probability of correct transmission for a single symbol: $p_c = 1 - 0.2 = 0.8$.
- Symbols are subject to interference independently.

We need to calculate the probability of receiving the specific signals:
1. $111$
2. $000$
3. $010$

---

## Solution & Reasoning

To find the probability of receiving any specific signal $R$, we must consider both possible original signals ($S_{111}$ and $S_{000}$) using the **Law of Total Probability**:
$$P(R) = P(R | S_{111}) \cdot P(S_{111}) + P(R | S_{000}) \cdot P(S_{000})$$

Because each bit is transmitted independently, the conditional probability of receiving a 3-bit sequence is the product of the probabilities of receiving each individual bit.

### 1. Probability of receiving $111$ ($P(R_{111})$)
- If $111$ was sent, all 3 bits must be received correctly: 
  $$P(R_{111} | S_{111}) = 0.8 \times 0.8 \times 0.8 = (0.8)^3 = 0.512$$
- If $000$ was sent, all 3 bits must be received with an error: 
  $$P(R_{111} | S_{000}) = 0.2 \times 0.2 \times 0.2 = (0.2)^3 = 0.008$$
  
Now, apply Total Probability:
$$P(R_{111}) = (0.512 \cdot 0.65) + (0.008 \cdot 0.35) = 0.3328 + 0.0028 = 0.3356$$

### 2. Probability of receiving $000$ ($P(R_{000})$)
- If $111$ was sent, all 3 bits must be received with an error:
  $$P(R_{000} | S_{111}) = (0.2)^3 = 0.008$$
- If $000$ was sent, all 3 bits must be received correctly:
  $$P(R_{000} | S_{000}) = (0.8)^3 = 0.512$$

Now, apply Total Probability:
$$P(R_{000}) = (0.008 \cdot 0.65) + (0.512 \cdot 0.35) = 0.0052 + 0.1792 = 0.1844$$

### 3. Probability of receiving $010$ ($P(R_{010})$)
- If $111$ was sent, the 1st and 3rd bits have errors (received as 0), but the 2nd bit is correct (received as 1):
  $$P(R_{010} | S_{111}) = 0.2 \times 0.8 \times 0.2 = 0.032$$
- If $000$ was sent, the 1st and 3rd bits are correct (received as 0), but the 2nd bit has an error (received as 1):
  $$P(R_{010} | S_{000}) = 0.8 \times 0.2 \times 0.8 = 0.128$$

Now, apply Total Probability:
$$P(R_{010}) = (0.032 \cdot 0.65) + (0.128 \cdot 0.35) = 0.0208 + 0.0448 = 0.0656$$

---
**Commentary / Understanding Check:**
* **Independence of Events:** A critical assumption here is that noise affects each bit independently. This allows us to multiply the probabilities of individual bits to find the probability of a sequence.
* **Total Probability in Telecommunications:** This problem illustrates a fundamental concept in information theory. A received message can be the result of a correctly transmitted message OR a heavily corrupted different message. We must account for all possible origins of the received signal.