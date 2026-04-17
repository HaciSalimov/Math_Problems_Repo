# Solution for Problem 6: The Axiomatic Point of View

## Discussion on Kolmogorov Axioms
The transition from recording 1000 dice rolls to the formal axioms of probability is the shift from empirical observation to mathematical deduction.

### 1. Intuition from Frequencies
Our work in Problem 5 directly inspired the first two axioms:
* **Non-negativity:** Since frequency is a count divided by total trials, it cannot be negative. Thus, P(A) >= 0.
* **Normalization:** Since all events happen within the sample space, the sum of all parts must equal the whole. Thus, P(Sample Space) = 1.

### 2. Finite vs. Countable Additivity
In our concrete experiment, we saw **finite additivity**: if two events are disjoint, the frequency of their union is the sum of their frequencies. However, Kolmogorov's third axiom demands **countable additivity** (sigma-additivity) for an infinite sequence of disjoint events. 

This cannot be proven by rolling a die 1000 times. It is a purely abstract, theoretical requirement that allows mathematicians to calculate limits and work with continuous probability spaces (like measuring time or length), moving beyond simple discrete counting.