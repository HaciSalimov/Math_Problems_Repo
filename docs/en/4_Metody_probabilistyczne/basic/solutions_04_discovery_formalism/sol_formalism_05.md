# Solution for Problem 5: Frequencies to Probability

## Part A — Observed Frequencies
Calculated using f(X) = n(X) / 1000:
1. A = {2,4,6}: n(A) = 154 + 167 + 170 = 491. f(A) = 0.491.
2. B = {1,2,3}: n(B) = 168 + 154 + 181 = 503. f(B) = 0.503.
3. C = {5,6}: n(C) = 160 + 170 = 330. f(C) = 0.330.
4. D = {1,3,5}: n(D) = 168 + 181 + 160 = 509. f(D) = 0.509.
5. E = {1,2,3,4}: n(E) = 168 + 154 + 181 + 167 = 670. f(E) = 0.670.

## Part B — Relationships
1. f({2,4,6}) = f({2}) + f({4}) + f({6}) holds because the outcomes are mutually exclusive (disjoint). We can simply add their frequencies.
2. f({1,2,3,4}) = f({1,2}) + f({3,4}) holds because the sets {1,2} and {3,4} are disjoint.
3. f({1,3,5}) + f({2,4,6}) = 1 holds because these two disjoint sets cover the entire sample space (complementarity).
4. f({5,6}) = 1 - f({1,2,3,4}) holds because {5,6} is the exact complement of {1,2,3,4}.

## Part C — Addition Failure
M = {1,2,3}, N = {3,4,5}.
f(M) = 0.503, f(N) = 0.508.
f(M U N) = f({1,2,3,4,5}) = 0.830.
f(M) + f(N) = 1.011.
**Explanation:** f(M U N) is not equal to f(M) + f(N) because the elementary outcome {3} exists in both sets. It is counted twice in the simple addition.

## Part D — Covering the Space
1. The sum of all single frequencies is exactly 1.
2. This is because adding all individual counts gives 1000, and 1000/1000 = 1.
3. f({1,2}) + f({3,4}) + f({5,6}) = 0.322 + 0.348 + 0.330 = 1.
4. Because these three subsets are disjoint and partition the sample space completely.
5. **General Statement:** If a sample space is partitioned into any number of mutually exclusive events, the sum of their frequencies is always 1.

## Part E & F — Mathematical Probability
To transition from empirical frequencies to theoretical probability, the mathematical function P must obey:
1. Outputs between 0 and 1 (frequencies are parts of a whole).
2. P(impossible) = 0 (an event that never happens has 0 count).
3. P(Sample Space) = 1 (the sum of all possibilities is 100%).
4. Additivity for disjoint events (just like we saw in Part B).
5. Complement rule adds to 1.