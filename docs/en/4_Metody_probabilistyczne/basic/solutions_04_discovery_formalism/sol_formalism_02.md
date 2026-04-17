# Solution for Problem 2: Die x Die

## Introduction & Sample Space Analysis
We are rolling two six-sided dice, creating a 6x6 sample space of 36 elementary outcomes. Each outcome is an ordered pair (row, column).

## Part A — Marking Events

### 1. the sum is equal to 8
**Reasoning:** We find all pairs where row + column = 8. These are (2,6), (3,5), (4,4), (5,3), and (6,2).
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . X
3     . . . . X .
4     . . . X . .
5     . . X . . .
6     . X . . . .
```

### 2. the first die is greater than the second
**Reasoning:** We look for outcomes where row > column. This forms the lower triangular region of the matrix.
```text
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X X . . .
5     X X X X . .
6     X X X X X .
```

### 3. both dice show even numbers
**Reasoning:** Row must be 2, 4, or 6 AND column must be 2, 4, or 6. This creates a grid pattern.
```text
      1 2 3 4 5 6
1     . . . . . .
2     . X . X . X
3     . . . . . .
4     . X . X . X
5     . . . . . .
6     . X . X . X
```

### 4. at least one die shows 6
**Reasoning:** We mark the entire 6th row and 6th column.
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     X X X X X X
```

### 5. exactly one die shows 1
**Reasoning:** We mark the 1st row and 1st column, but strictly EXCLUDE (1,1) because that is two dice showing 1.
```text
      1 2 3 4 5 6
1     . X X X X X
2     X . . . . .
3     X . . . . .
4     X . . . . .
5     X . . . . .
6     X . . . . .
```

## Part B — Interpretation

### Case 1
**Interpretation:** The block covers outcomes where both dice show 3, 4, 5, or 6. The statement is: **"Both dice show a number strictly greater than 2."**

### Case 2
**Interpretation:** The marked cells form the main diagonal where row equals column. The statement is: **"Both dice show the exact same number."**