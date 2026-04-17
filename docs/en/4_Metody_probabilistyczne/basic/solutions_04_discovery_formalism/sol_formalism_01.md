# Solution for Problem 1: Coin x Coin

## Introduction & Sample Space Analysis
In this experiment, we are tossing two coins. The fundamental concept here is to map logical statements about the physical coins into mathematical subsets within our sample space. The sample space consists of 4 elementary outcomes, defined by ordered pairs: (H,H), (H,T), (T,H), (T,T).

## Part A — Marking Events

### 1. exactly one head
**Reasoning:** The event requires strictly one Head and one Tail across the two tosses. This excludes (H,H) and (T,T).
```text
      H   T
H     .   X
T     X   .
```

### 2. both tosses are the same
**Reasoning:** The event requires the first and second outcomes to be identical. This forms the main diagonal.
```text
      H   T
H     X   .
T     .   X
```

### 3. at least one head
**Reasoning:** This includes everything except the outcome with zero heads, which is (T,T).
```text
      H   T
H     X   X
T     X   .
```

### 4. the first toss is tails
**Reasoning:** We are only constrained by the first toss. We select the entire row where the first toss is T.
```text
      H   T
H     .   .
T     X   X
```

### 5. the second toss is heads
**Reasoning:** The constraint is strictly on the second toss. We select the entire column where the second toss is H.
```text
      H   T
H     X   .
T     X   .
```

## Part B — Interpretation

### Case 1
**Interpretation:** The entire first row is marked X. This corresponds to situations where the first toss resulted in Heads, regardless of the second toss. The statement is: **"The first toss is heads."**

### Case 2
**Interpretation:** The marked cells correspond to (H,T) and (T,H). The outcomes where both coins show the same face are excluded. The statement is: **"Exactly one head"** or **"The tosses yield different results."**