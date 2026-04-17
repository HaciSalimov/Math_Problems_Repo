# Solution for Problem 4: Complex Statements

## Part A — Basic Statements
**A: Sum is 7.** Points: (1,6), (2,5), (3,4), (4,3), (5,2), (6,1).
**B: First > Second.** The lower triangle.
**C: At least one 6.** Row 6 and Col 6.

## Part B — Compound Statements

### 1. A OR C (Sum is 7 or at least one 6)
**Reasoning:** Union of sets A and C.
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X X
3     . . . X . X
4     . . X . . X
5     . X . . . X
6     X X X X X X
```

### 2. A AND C (Sum is 7 and at least one 6)
**Reasoning:** Intersection. Only (1,6) and (6,1) satisfy both.
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X . . . . .
```

### 3. B AND C (First > Second and at least one 6)
**Reasoning:** Intersection. Row 6, except (6,6).
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     X X X X X .
```

### 4. A BUT NOT B (Sum is 7, but First <= Second)
**Reasoning:** Set A minus Set B. Points: (1,6), (2,5), (3,4).
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . X .
3     . . . X . .
4     . . . . . .
5     . . . . . .
6     . . . . . .
```

### 5. A AND NOT C (Sum is 7 and no 6)
**Reasoning:** Set A minus Set C. Points: (2,5), (3,4), (4,3), (5,2).
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . X .
3     . . . X . .
4     . . X . . .
5     . X . . . .
6     . . . . . .
```

### 6. C BUT NOT A (At least one 6, but Sum != 7)
**Reasoning:** Set C minus Set A.
```text
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     . X X X X X
```

### 7. NOT A AND B (Sum != 7 and First > Second)
**Reasoning:** Set B minus Set A.
```text
      1 2 3 4 5 6
1     . . . . . .
2     X . . . . .
3     X X . . . .
4     X X X . . .
5     X . X X . .
6     . X X X X .
```

### 8. NOT B AND C (First <= Second and at least one 6)
**Reasoning:** Set C minus Set B. The 6th column.
```text
      1 2 3 4 5 6
1     . . . . . X
2     . . . . . X
3     . . . . . X
4     . . . . . X
5     . . . . . X
6     . . . . . X
```

### 9. NOT (A OR C)
**Reasoning:** The complement of statement 1. Neither sum is 7 nor is there a 6.
```text
      1 2 3 4 5 6
1     X X X X X .
2     X X X X . .
3     X X X . X .
4     X X . X X .
5     X . X X X .
6     . . . . . .
```

### 10. NOT (A AND C)
**Reasoning:** The complement of statement 2. Everything except (1,6) and (6,1).
```text
      1 2 3 4 5 6
1     X X X X X .
2     X X X X X X
3     X X X X X X
4     X X X X X X
5     X X X X X X
6     . X X X X X
```