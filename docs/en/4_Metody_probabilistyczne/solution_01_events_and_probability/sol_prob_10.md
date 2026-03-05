# Solution for Task 10: Communication Channel and Interference

## Problem Statement
A communication channel transmits 3 types of 4-letter sequences: $AAAA$, $BBBB$, $CCCC$ with the following a priori probabilities:
- $P(T_{AAAA}) = 0.4$
- $P(T_{BBBB}) = 0.3$
- $P(T_{CCCC}) = 0.3$

Each letter is subject to independent random interference. The probability of correct transmission is $0.8$, and the probability of receiving either of the other two wrong letters is $0.1$ each.

We need to find the overall probability of receiving the specific sequences at the output:
1. $AAAA$
2. $ACAA$

---

## Solution & Reasoning

We must use the **Law of Total Probability**. The received signal ($R$) could have originated from any of the three possible transmitted signals ($T$).
$$P(R) = P(R \mid T_{AAAA})P(T_{AAAA}) + P(R \mid T_{BBBB})P(T_{BBBB}) + P(R \mid T_{CCCC})P(T_{CCCC})$$

Since the letters are interfered independently, the probability of receiving a specific sequence is the product of the probabilities of receiving each individual letter.

### 1. Probability of receiving $AAAA$
Let's calculate the conditional probabilities of receiving $AAAA$ given each possible transmitted sequence:
- If $AAAA$ was sent (4 correct letters): 
  $$P(R_{AAAA} \mid T_{AAAA}) = 0.8 \times 0.8 \times 0.8 \times 0.8 = (0.8)^4 = 0.4096$$
- If $BBBB$ was sent (4 errors, all B's turned to A's): 
  $$P(R_{AAAA} \mid T_{BBBB}) = 0.1 \times 0.1 \times 0.1 \times 0.1 = (0.1)^4 = 0.0001$$
- If $CCCC$ was sent (4 errors, all C's turned to A's): 
  $$P(R_{AAAA} \mid T_{CCCC}) = 0.1 \times 0.1 \times 0.1 \times 0.1 = (0.1)^4 = 0.0001$$

Now apply the Law of Total Probability:
$$P(R_{AAAA}) = (0.4096 \times 0.4) + (0.0001 \times 0.3) + (0.0001 \times 0.3)$$
$$P(R_{AAAA}) = 0.16384 + 0.00003 + 0.00003 = 0.1639$$

### 2. Probability of receiving $ACAA$
Let's calculate the conditional probabilities for receiving $A-C-A-A$:
- If $AAAA$ was sent (3 correct, 1 error where A turned to C):
  $$P(R_{ACAA} \mid T_{AAAA}) = 0.8 \times 0.1 \times 0.8 \times 0.8 = 0.512 \times 0.1 = 0.0512$$
- If $BBBB$ was sent (4 errors, three B's turned to A, one B turned to C):
  $$P(R_{ACAA} \mid T_{BBBB}) = 0.1 \times 0.1 \times 0.1 \times 0.1 = 0.0001$$
- If $CCCC$ was sent (3 errors where C turned to A, 1 correct C):
  $$P(R_{ACAA} \mid T_{CCCC}) = 0.1 \times 0.8 \times 0.1 \times 0.1 = 0.0008$$

Now apply the Law of Total Probability:
$$P(R_{ACAA}) = (0.0512 \times 0.4) + (0.0001 \times 0.3) + (0.0008 \times 0.3)$$
$$P(R_{ACAA}) = 0.02048 + 0.00003 + 0.00024 = 0.02075$$

---
**Commentary / Understanding Check:**
* **Information Theory:** This task represents a real-world telecommunications problem. Even if we receive a highly distorted signal like $ACAA$, we can mathematically evaluate the likelihood of what the original message was. 
* **Power of Independent Events:** Because the interference is independent for each letter, we can simply multiply the probabilities from the given matrix to construct the probability of any sequence.