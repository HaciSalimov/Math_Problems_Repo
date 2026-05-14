## Task 1 — Discrete Distribution Given by a PMF Table

**Original Task:** Consider a discrete random variable $X$ with the following PMF:
| $x$ | -2 | 0 | 1 | 3 | 5 |
| --- | --- | --- | --- | --- | --- |
| $P(X=x)$ | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

### Solution

**0. Probability Space & Random Variable:**
* **Sample Space ($\Omega$):** An urn with 100 balls where 10 are labeled '-2', 25 labeled '0', 30 labeled '1', 20 labeled '3', and 15 labeled '5'.
* **Random Variable $X$:** The number on the drawn ball.
* **Support:** $\{-2, 0, 1, 3, 5\}$.

**1. Verification:**
Sum = 0.10 + 0.25 + 0.30 + 0.20 + 0.15 = 1.00. Valid.

**2. PMF Graph:**
```text
P(X=x)
 0.30 |          *
 0.25 |      * |
 0.20 |      |   |       *
 0.15 |      |   |       |       *
 0.10 |  * |   |       |       |
 0.00 +--|---|---|-------|-------|-- x
        -2   0   1       3       5
```

**3 & 4. CDF Construction & Graph:**
* $F(x) = 0$ for $x < -2$
* $F(x) = 0.10$ for $-2 \le x < 0$
* $F(x) = 0.35$ for $0 \le x < 1$
* $F(x) = 0.65$ for $1 \le x < 3$
* $F(x) = 0.85$ for $3 \le x < 5$
* $F(x) = 1.00$ for $x \ge 5$

```text
F(x)
 1.00 |                          o========>
 0.85 |                  o=======*
 0.65 |          o=======*
 0.35 |      o===*
 0.10 |  o===*
 0.00 ===*---|---|-------|-------|-------- x
            -2   0       1       3       5
```

**5. Jumps:** The jump size at $x$ is exactly $P(X=x)$.

---