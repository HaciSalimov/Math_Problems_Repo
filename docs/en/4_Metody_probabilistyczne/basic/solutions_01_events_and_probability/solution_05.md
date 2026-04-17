# Solution for Task 5: Buffon's Needle Sample Space

## 1. Setup & Baseline
A needle of length $L$ is thrown onto parallel lines spaced $d$ apart. The outcome is determined entirely by two continuous variables:
* $x$: The perpendicular distance from the needle's center to the nearest line.
* $\theta$: The acute angle between the needle and the parallel lines.

---

## 2. Defining the Sample Space ($\Omega$)

### Bounding the Distance ($x$)
Because $x$ is the distance to the *closest* line, its maximum possible value is exactly halfway between the lines ($d/2$).
$$0 \le x \le \frac{d}{2}$$

### Bounding the Angle ($\theta$)
Due to rotational symmetry, the distinct orientation angles range from $0$ to $\pi/2$.
$$0 \le \theta \le \frac{\pi}{2}$$

### The Final Set Definition
Combining these continuous boundaries gives us our final geometric space:
$$\Omega = \left\{ (x, \theta) \mid 0 \le x \le \frac{d}{2}, \, 0 \le \theta \le \frac{\pi}{2} \right\}$$

---
> **Commentary / Key Takeaway:** > This is a major paradigm shift. Unlike coins or dice, distance and angle are measured in real numbers ($\mathbb{R}$). Therefore, the sample space is **continuous**, not discrete. It represents a 2D rectangular geometric area containing infinitely many possible outcomes.