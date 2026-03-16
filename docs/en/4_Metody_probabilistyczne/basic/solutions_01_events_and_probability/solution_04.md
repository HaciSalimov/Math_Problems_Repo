# Solution for Task 4: Weekly Weather Observation

## 1. Setup & Baseline
The weather can be modeled in one of three distinct states: Sunny ($S$), Cloudy ($C$), or Rainy ($R$). We observe these states over a continuous sequence of days.

---

## 2. Sample Space Construction

### Scenario 1: One Day ($\Omega_1$)
The space consists of the three base states.
$$\Omega_1 = \{S, C, R\} \implies |\Omega_1| = 3$$

### Scenario 2: Two Consecutive Days ($\Omega_2$)
The space expands to ordered pairs of weather states.
$$\Omega_2 = \{(w_1, w_2) \mid w_i \in \{S, C, R\}\} \implies |\Omega_2| = 3^2 = 9$$

### Scenario 3: Seven Consecutive Days ($\Omega_7$)
The combinations grow exponentially for a full week.
$$\Omega_7 = \{(w_1, w_2, \dots, w_7) \mid w_i \in \{S, C, R\}\} \implies |\Omega_7| = 3^7 = 2187$$

---
> **Commentary / Key Takeaway:** > Even though this models meteorology, mathematically it is identical to variations with repetition (like rolling a 3-sided die). Every elementary outcome is an ordered 7-tuple representing a single, unbreakable 7-day weather trajectory.