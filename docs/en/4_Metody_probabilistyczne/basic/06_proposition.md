# Task List 06 — Algebra of Events and Conditional Probability

## Problem 1 — Event algebra from a two-way table

A university collected data about students’ study habits.

| Student type               | Submits homework on time | Does not submit on time | Total |
| -------------------------- | -----------------------: | ----------------------: | ----: |
| Attends lectures regularly |                       48 |                      12 |    60 |
| Does not attend regularly  |                       22 |                      18 |    40 |
| Total                      |                       70 |                      30 |   100 |

Let:

$$
A=\text{the student attends lectures regularly},
$$

$$
B=\text{the student submits homework on time}.
$$

Compute:

1. $P(A)$,
2. $P(B)$,
3. $P(A\cap B)$,
4. $P(A\cup B)$,
5. $P(A^c)$,
6. $P(B^c)$,
7. $P(A\setminus B)$,
8. $P(B\setminus A)$,
9. $P(A^c\cap B^c)$,
10. $P(A\mid B)$,
11. $P(B\mid A)$.

Then answer:

12. Are $A$ and $B$ mutually exclusive?
13. Are $A$ and $B$ independent?
14. Interpret $P(A\mid B)$ and $P(B\mid A)$ in words.

---

## Problem 2 — Four regions of a sample space

A company classifies support tickets according to two properties:

* whether the ticket is technical,
* whether the ticket was solved during the first contact.

The data are:

| Ticket type   | Solved during first contact | Not solved during first contact | Total |
| ------------- | --------------------------: | ------------------------------: | ----: |
| Technical     |                          90 |                              60 |   150 |
| Non-technical |                         160 |                              40 |   200 |
| Total         |                         250 |                             100 |   350 |

Let:

$$
T=\text{the ticket is technical},
$$

$$
S=\text{the ticket was solved during the first contact}.
$$

1. Fill in the probabilities of the four disjoint regions:

$$
T\cap S,
$$

$$
T\cap S^c,
$$

$$
T^c\cap S,
$$

$$
T^c\cap S^c.
$$

2. Verify that these four probabilities add up to (1).

3. Use these four regions to compute:

$$
P(T\cup S),
$$

$$
P(T^c\cup S),
$$

$$
P(T\cap S^c),
$$

$$
P(T^c\cap S^c).
$$

4. Compute:

$$
P(S\mid T)
$$

and

$$
P(S\mid T^c).
$$

5. Does being a technical ticket change the probability of being solved during the first contact?

---

## Problem 3 — Conditional probabilities are not symmetric

An online course platform records whether users watched a lecture and whether they passed a quiz.

| User behavior         | Passed quiz | Did not pass quiz | Total |
| --------------------- | ----------: | ----------------: | ----: |
| Watched lecture       |          72 |                18 |    90 |
| Did not watch lecture |          28 |                32 |    60 |
| Total                 |         100 |                50 |   150 |

Let:

$$
W=\text{the user watched the lecture},
$$

$$
Q=\text{the user passed the quiz}.
$$

Compute:

1. $P(W)$,
2. $P(Q)$,
3. $P(W\cap Q)$,
4. $P(Q\mid W)$,
5. $P(W\mid Q)$,
6. $P(Q\mid W^c)$,
7. $P(W\mid Q^c)$.

Then answer:

8. Why are $P(Q\mid W)$ and $P(W\mid Q)$ different questions?
9. Which probability is more useful if we want to know whether watching the lecture helps?
10. Which probability is more useful if we want to describe students who passed the quiz?

---

## Problem 4 — Inclusion–exclusion and double counting

A company surveyed 200 employees about two software tools.

* 130 employees use Tool A,
* 90 employees use Tool B,
* 60 employees use both tools.

Let:

$$
A=\text{the employee uses Tool A},
$$

$$
B=\text{the employee uses Tool B}.
$$

Compute:

1. $P(A)$,
2. $P(B)$,
3. $P(A\cap B)$,
4. $P(A\cup B)$,
5. $P(A\setminus B)$,
6. $P(B\setminus A)$,
7. $P(A^c\cap B^c)$,
8. $P(A\mid B)$,
9. $P(B\mid A)$.

Then explain:

10. Why is

$$
P(A\cup B)\neq P(A)+P(B)?
$$

11. Which group is counted twice in $P(A)+P(B)$?

---

## Problem 5 — Independence from data

A streaming platform records whether users have a premium account and whether they watched a movie during the last weekend.

| Account type | Watched a movie | Did not watch a movie | Total |
| ------------ | --------------: | --------------------: | ----: |
| Premium      |              84 |                    36 |   120 |
| Free         |              56 |                    24 |    80 |
| Total        |             140 |                    60 |   200 |

Let:

$$
P=\text{the user has a premium account},
$$

$$
M=\text{the user watched a movie during the weekend}.
$$

1. Compute $P(P)$.
2. Compute $P(M)$.
3. Compute $P(P\cap M)$.
4. Compute $P(M\mid P)$.
5. Compute $P(M\mid P^c)$.
6. Decide whether $P$ and $M$ are independent.
7. Verify your answer using:

$$
P(P\cap M)=P(P)P(M).
$$

8. Verify your answer using:

$$
P(M\mid P)=P(M).
$$

9. Explain in words what independence means in this situation.

---

## Problem 6 — Dependence from data

A delivery company records whether a parcel is international and whether it is delayed.

| Parcel type   | Delayed | Not delayed | Total |
| ------------- | ------: | ----------: | ----: |
| Domestic      |      24 |         376 |   400 |
| International |      36 |         164 |   200 |
| Total         |      60 |         540 |   600 |

Let:

$$
I=\text{the parcel is international},
$$

$$
D=\text{the parcel is delayed}.
$$

Compute:

1. $P(I)$,
2. $P(D)$,
3. $P(I\cap D)$,
4. $P(D\mid I)$,
5. $P(D\mid I^c)$,
6. $P(I\mid D)$,
7. $P(I\mid D^c)$.

Then answer:

8. Are $I$ and $D$ independent?
9. Does international shipping increase the probability of delay?
10. Explain the difference between $P(D\mid I)$ and $P(I\mid D)$.

---

## Problem 7 — Conditional probability with three categories

A company classifies customers into three activity levels:

* high activity,
* medium activity,
* low activity.

It records whether they renewed their subscription.

| Activity level | Renewed | Did not renew | Total |
| -------------- | ------: | ------------: | ----: |
| High           |      80 |            20 |   100 |
| Medium         |      90 |            60 |   150 |
| Low            |      30 |           120 |   150 |
| Total          |     200 |           200 |   400 |

Let:

$$
H=\text{the customer has high activity},
$$

$$
M=\text{the customer has medium activity},
$$

$$
L=\text{the customer has low activity},
$$

$$
R=\text{the customer renewed the subscription}.
$$

1. Explain why $H$, $M$, and $L$ form a partition of the sample space.
2. Compute:

$$
P(H),\quad P(M),\quad P(L).
$$

3. Compute:

$$
P(R\mid H),\quad P(R\mid M),\quad P(R\mid L).
$$

4. Use the law of total probability to compute $P(R)$.
5. Verify your result directly from the table.
6. Compute:

$$
P(H\mid R),\quad P(M\mid R),\quad P(L\mid R).
$$

7. Interpret the difference between $P(R\mid H)$ and $P(H\mid R)$.

---

## Problem 8 — Bayes’ formula from a table

A fraud detection system classifies transactions as suspicious or not suspicious.

The historical data are:

| Transaction type | Marked suspicious | Not marked suspicious | Total |
| ---------------- | ----------------: | --------------------: | ----: |
| Fraudulent       |                98 |                     2 |   100 |
| Legitimate       |               297 |                  9603 |  9900 |
| Total            |               395 |                  9605 | 10000 |

Let:

$$
F=\text{the transaction is fraudulent},
$$

$$
S=\text{the transaction is marked suspicious}.
$$

Compute:

1. $P(F)$,
2. $P(S\mid F)$,
3. $P(S\mid F^c)$,
4. $P(S)$,
5. $P(F\mid S)$,
6. $P(F^c\mid S)$.

Then answer:

7. Most suspicious transactions are fraudulent or legitimate?
8. Why can this happen even if the system detects fraudulent transactions very well?
9. Explain the role of the base rate $P(F)$.

---

## Problem 9 — Law of total probability without a full table

A company receives orders through three channels:

* website,
* mobile app,
* phone.

The proportions of orders are:

$$
P(W)=0.50,
$$

$$
P(A)=0.35,
$$

$$
P(P)=0.15.
$$

The probability that an order is cancelled depends on the channel:

$$
P(C\mid W)=0.04,
$$

$$
P(C\mid A)=0.06,
$$

$$
P(C\mid P)=0.10.
$$

Here:

$$
C=\text{the order is cancelled}.
$$

1. Explain why $W$, $A$, and $P$ form a partition of the sample space.
2. Compute $P(C)$.
3. Compute the contribution of each channel to the total cancellation probability:

$$
P(C\cap W),
$$

$$
P(C\cap A),
$$

$$
P(C\cap P).
$$

4. Compute:

$$
P(W\mid C),
$$

$$
P(A\mid C),
$$

$$
P(P\mid C).
$$

5. Which channel is most likely among cancelled orders?
6. Is this necessarily the channel with the highest cancellation rate? Explain.

---

## Problem 10 — Comprehensive problem: event algebra, conditioning, independence, and Bayes

A company studies whether users complete an online onboarding process.

Users are divided into two groups:

* users who received a tutorial,
* users who did not receive a tutorial.

The data are:

| Group             | Completed onboarding | Did not complete onboarding | Total |
| ----------------- | -------------------: | --------------------------: | ----: |
| Received tutorial |                  180 |                          70 |   250 |
| No tutorial       |                  120 |                         130 |   250 |
| Total             |                  300 |                         200 |   500 |

Let:

$$
T=\text{the user received the tutorial},
$$

$$
C=\text{the user completed onboarding}.
$$

Compute:

1. $P(T)$,
2. $P(C)$,
3. $P(T\cap C)$,
4. $P(T\cup C)$,
5. $P(T\setminus C)$,
6. $P(C\setminus T)$,
7. $P(T^c\cap C^c)$,
8. $P(C\mid T)$,
9. $P(C\mid T^c)$,
10. $P(T\mid C)$,
11. $P(T\mid C^c)$.

Then answer:

12. Are $T$ and $C$ independent?
13. Does receiving the tutorial appear to change the probability of completing onboarding?
14. What is the difference between:

$$
P(C\mid T)
$$

and

$$
P(T\mid C)?
$$

15. Write a short interpretation of the result in words.
