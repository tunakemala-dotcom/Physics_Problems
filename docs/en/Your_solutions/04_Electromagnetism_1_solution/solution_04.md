# Task 04 – Force Comparison

## Problem Statement

Calculate the magnitude of the electric force and the gravitational force between an electron and a proton in a hydrogen atom (average distance $r \approx 5.3 \times 10^{-11} \text{ m}$). What is the ratio $F_e/F_g$?

## Theory

The electric force is given by Coulomb's Law, and the gravitational force is given by Newton's Law of Universal Gravitation.

$$
F_e = k \frac{|q_1 q_2|}{r^2}
$$

$$
F_g = G \frac{m_1 m_2}{r^2}
$$

## Step-by-Step Solution

Identify the constants:
* Coulomb constant $k = 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$
* Gravitational constant $G = 6.67 \times 10^{-11} \text{ N}\cdot\text{m}^2/\text{kg}^2$
* Elementary charge $e = 1.60 \times 10^{-19} \text{ C}$
* Mass of electron $m_e = 9.11 \times 10^{-31} \text{ kg}$
* Mass of proton $m_p = 1.67 \times 10^{-27} \text{ kg}$
* Distance $r = 5.3 \times 10^{-11} \text{ m}$

### Electric Force

$$
F_e = \frac{(8.99 \times 10^9)(1.60 \times 10^{-19})^2}{(5.3 \times 10^{-11})^2}
$$

$$
F_e \approx \frac{(8.99 \times 10^9)(2.56 \times 10^{-38})}{2.809 \times 10^{-21}} \approx 8.2 \times 10^{-8} \text{ N}
$$

### Gravitational Force

$$
F_g = \frac{(6.67 \times 10^{-11})(9.11 \times 10^{-31})(1.67 \times 10^{-27})}{(5.3 \times 10^{-11})^2}
$$

$$
F_g \approx \frac{1.01 \times 10^{-67}}{2.809 \times 10^{-21}} \approx 3.6 \times 10^{-47} \text{ N}
$$

### Ratio $F_e/F_g$

Because both formulas share the $r^2$ denominator, the distance cancels out algebraically if computed directly:

$$
\frac{F_e}{F_g} = \frac{k e^2}{G m_e m_p}
$$

$$
\frac{F_e}{F_g} = \frac{8.2 \times 10^{-8}}{3.6 \times 10^{-47}} \approx 2.3 \times 10^{39}
$$

## Final Result

* Electric force: $F_e \approx 8.2 \times 10^{-8} \text{ N}$
* Gravitational force: $F_g \approx 3.6 \times 10^{-47} \text{ N}$
* Ratio: $F_e / F_g \approx 2.3 \times 10^{39}$

## Interpretation

The electric force is approximately 39 orders of magnitude stronger than the gravitational force at the atomic scale. This demonstrates why gravity is entirely negligible in the study of atomic and molecular physics.
