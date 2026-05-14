## Task 2 — Discrete Distribution Given by a CDF Table

**Original Task:** CDF values:
| $x$ | -1 | 0 | 2 | 4 | 6 |
| --- | --- | --- | --- | --- | --- |
| $F(x)$ | 0.15 | 0.35 | 0.60 | 0.85 | 1.00 |

### Solution

**1. Reconstructing PMF:**
* $P(X=-1) = 0.15$
* $P(X=0) = 0.35 - 0.15 = 0.20$
* $P(X=2) = 0.60 - 0.35 = 0.25$
* $P(X=4) = 0.85 - 0.60 = 0.25$
* $P(X=6) = 1.00 - 0.85 = 0.15$

**2 & 3. Graphical Representation:**
```text
P(X=x) (PMF)
 0.25 |          * *
 0.20 |      * |       |
 0.15 |  * |   |       |       *
 0.00 +--|---|---|-------|-------|-- x
        -1   0   2       4       6
```

**6. Probabilities from CDF:**
* $P(X \le 2) = F(2) = 0.60$
* $P(X < 2) = F(0) = 0.35$
* $P(X = 2) = 0.60 - 0.35 = 0.25$

---