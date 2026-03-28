# List 4 — Discovering Formalism

## Instructions

All answers for problems 1-3 **must be presented using clear ASCII diagrams**, consistent with the format used in the problems.

* use the notation:

  * `X` — the outcome belongs to the event
  * `.` — the outcome does not belong to the event
* the table structure must be preserved (no axis swapping, no shortcuts)
* answers must be complete and readable

**Any other form of answer (lists, purely verbal descriptions, etc.) will not be accepted.**

---

# Problem 1 — Coin × Coin

Consider an experiment consisting of two coin tosses.

Representation:

```
      H   T
H     .   .
T     .   .
```

Each cell corresponds to one possible outcome.

---

## Part A — marking events

For each statement, mark all outcomes for which the statement is true:

1. exactly one head
2. both tosses are the same
3. at least one head
4. the first toss is tails
5. the second toss is heads

---

## Part B — interpretation

Describe the event represented by each case below:

### Case 1

```
      H   T
H     X   X
T     .   .
```

---

### Case 2

```
      H   T
H     .   X
T     X   .
```

---

# Problem 2 — Die × Die

Consider an experiment consisting of two dice rolls.

Representation:

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

---

## Part A — marking events

Mark all outcomes satisfying the statement:

1. the sum is equal to 8
2. the first die is greater than the second
3. both dice show even numbers
4. at least one die shows 6
5. exactly one die shows 1

---

## Part B — interpretation

Describe the event represented by each case below:

### Case 1

```
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . X X X X
4     . . X X X X
5     . . X X X X
6     . . X X X X
```

---

### Case 2

```
      1 2 3 4 5 6
1     X . . . . .
2     . X . . . .
3     . . X . . .
4     . . . X . .
5     . . . . X .
6     . . . . . X
```

---

# Problem 3 — Weather (7 days × 3 states)

Consider a week where each day can be:

* S — sunny
* C — cloudy
* R — rainy

Representation:

```
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   .   .
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

---

## Part A — marking events

Mark all outcomes satisfying the statement:

1. Monday is sunny
2. the weekend (Saturday and Sunday) is rainy
3. it rains on Wednesday or Friday
4. there is no rainy day during the week
5. Thursday is not sunny

---

## Part B — interpretation

Describe the event represented by each case below:

### Case 1

```
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   X   X
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

---

### Case 2

```
      Mon Tue Wed Thu Fri Sat Sun
S     X   X   X   X   X   X   X
C     X   X   X   X   X   X   X
R     .   .   .   .   .   .   .
```


## Problem 4 — Building complex statements from simple ones

Consider an experiment consisting of **two die rolls**.

Representation:

```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

Each cell corresponds to one outcome ((i,j)), where:

* (i) is the result of the first die,
* (j) is the result of the second die.

Use the notation:

* `X` — the outcome belongs to the event
* `.` — the outcome does not belong to the event

**All answers must be presented graphically.**
A plain list of ordered pairs is **not accepted**.

The minimum accepted format is a clear **ASCII table** obtained by marking the sample space.
If someone wants, they may also prepare an **HTML visualization**, but ASCII is the required minimum.

 
## Part A — basic statements

Mark the events corresponding to the following statements:

* (A): the sum of the two results is equal to 7
* (B): the first die shows a greater number than the second
* (C): at least one die shows 6


## Part B — compound statements

Using the events (A), (B), and (C), mark the events corresponding to the following statements:

1. the sum is 7 **or** at least one die shows 6
2. the sum is 7 **and** at least one die shows 6
3. the first die is greater than the second **and** at least one die shows 6
4. the sum is 7, **but** the first die is not greater than the second
5. the sum is 7, **and** no die shows 6
6. at least one die shows 6, **but** the sum is not 7
7. the sum is not 7 **and** the first die is greater than the second
8. the first die is not greater than the second **and** at least one die shows 6
9. it is not true that the sum is 7 **or** at least one die shows 6
10. it is not true that the sum is 7 **and** at least one die shows 6


## Problem 5 — From recorded frequencies to probability

A student rolled a six-sided die **1000 times** and recorded the results.

The numbers of occurrences of the elementary outcomes were:

$$
n({1})=168,\qquad
n({2})=154,\qquad
n({3})=181,
$$

$$
n({4})=167,\qquad
n({5})=160,\qquad
n({6})=170.
$$

Thus the sample space of a single experiment is

$$
\Omega={1,2,3,4,5,6}.
$$

Every event is a subset of (\Omega).

For any event (A\subseteq\Omega), define its **observed frequency** by

$$
f(A)=\frac{n(A)}{1000},
$$

where (n(A)) is the number of throws in which the event (A) occurred.

### Part A — From elementary outcomes to events

Using the recorded data, compute the observed frequencies of the following events:

1. (A={2,4,6})
2. (B={1,2,3})
3. (C={5,6})
4. (D={1,3,5})
5. (E={1,2,3,4})

In each case, first compute (n(A)), (n(B)), etc., and then compute (f(A)), (f(B)), etc.

### Part B — How frequencies combine

Using the same data, verify the following relationships:

1. (f({2,4,6})=f({2})+f({4})+f({6}))
2. (f({1,2,3,4})=f({1,2})+f({3,4}))
3. (f({1,3,5})+f({2,4,6})=1)
4. (f({5,6})=1-f({1,2,3,4}))

Explain in each case why the equality holds.

### Part C — When simple addition works and when it fails

1. Check that

$$
f({1,2}\cup{5,6})=f({1,2})+f({5,6}).
$$

2. Now consider the events

$$
M={1,2,3},\qquad N={3,4,5}.
$$

Compute

$$
f(M),\qquad f(N),\qquad f(M\cup N),\qquad f(M)+f(N).
$$

3. Explain why in this case

$$
f(M\cup N)\neq f(M)+f(N).
$$

4. Identify which elementary outcomes are counted twice in the sum (f(M)+f(N)).

### Part D — Covering the whole sample space

Consider the six one-element events

$$
{1},{2},{3},{4},{5},{6}.
$$

1. Add their observed frequencies.
2. Explain why the result must be equal to 1.
3. Split (\Omega) into the three disjoint events

$$
{1,2},\qquad {3,4},\qquad {5,6}
$$

and compute the sum of their observed frequencies.
4. Explain why this sum is also equal to 1.
5. Formulate a general statement about any decomposition of (\Omega) into disjoint events.

### Part E — From observed frequency to probability

In the previous parts, you worked with observed frequencies obtained from **1000 real throws**.

Now suppose that instead of working only with this one recorded experiment, we want to introduce a mathematical object that assigns a number to every event (A\subseteq\Omega), describing how often we expect this event to occur in repeated trials.

Based on the previous parts, write down what properties such an assignment should have.

In particular, explain why it should satisfy:

1. it assigns numbers between 0 and 1,
2. it assigns 0 to the impossible event,
3. it assigns 1 to the whole sample space,
4. for disjoint events, the value on the union is the sum of the values,
5. for complementary events, the two values add up to 1.

### Part F — Conclusion

Explain in your own words how the following three levels are connected:

1. elementary outcomes and events,
2. observed frequencies from a real experiment,
3. probability as a mathematical abstraction built from those observations.


## Problem 6 — Final discussion: the axiomatic point of view

Using everything developed in the previous problems, write a short discussion of the axiomatic formulation of probability. State and comment on the Kolmogorov axioms, explain which of their features were already suggested by our earlier work with events and observed frequencies, and indicate clearly what goes beyond those earlier finite considerations.

In particular, discuss why non-negativity, normalization, and finite additivity for disjoint events appear naturally in the framework we have built, and why countable additivity is a more subtle principle that is not directly obtained from finite experiments or finite sample spaces.
