# Solution for Problem 3: Weather

## Introduction
The columns represent Days of the week and the rows represent Weather states.

## Part A — Marking Events

### 1. Monday is sunny
**Reasoning:** We mark the intersection of row S and column Mon.
```text
      Mon Tue Wed Thu Fri Sat Sun
S     X   .   .   .   .   .   .
C     .   .   .   .   .   .   .
R     .   .   .   .   .   .   .
```

### 2. the weekend (Saturday and Sunday) is rainy
**Reasoning:** We assign the Rainy state (R) to both Sat and Sun.
```text
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   .   .
C     .   .   .   .   .   .   .
R     .   .   .   .   .   X   X
```

### 3. it rains on Wednesday or Friday
**Reasoning:** We mark row R under Wed and Fri.
```text
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   .   .
C     .   .   .   .   .   .   .
R     .   .   X   .   X   .   .
```

### 4. there is no rainy day during the week
**Reasoning:** Row R is left blank. Every day must be either S or C.
```text
      Mon Tue Wed Thu Fri Sat Sun
S     X   X   X   X   X   X   X
C     X   X   X   X   X   X   X
R     .   .   .   .   .   .   .
```

### 5. Thursday is not sunny
**Reasoning:** Thursday can be C or R, but not S.
```text
      Mon Tue Wed Thu Fri Sat Sun
S     .   .   .   .   .   .   .
C     .   .   .   X   .   .   .
R     .   .   .   X   .   .   .
```

## Part B — Interpretation

### Case 1
**Interpretation:** Only Sat and Sun are marked, and only under Sunny. Statement: **"The weekend is sunny."**

### Case 2
**Interpretation:** S and C are marked for all days; R is completely empty. Statement: **"There is no rain throughout the entire week."**