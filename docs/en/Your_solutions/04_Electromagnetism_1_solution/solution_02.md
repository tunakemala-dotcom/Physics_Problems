# Task 02 – Electric Potential

## Problem Statement

Point charges of $+1\text{C}$, $-2\text{C}$, $+3\text{C}$, and $-4\text{C}$ are placed at the corners of a square with sides of $1.0 \text{ m}$ (in order). Calculate the electric potential at the center of the square.

## Theory

The electric potential $V$ at a point due to a system of discrete point charges is the algebraic sum of the potentials due to individual charges. Potential is a scalar quantity, so vector addition is not required.

$$
V = \sum_{i=1}^{n} k \frac{q_i}{r_i}
$$

## Step-by-Step Solution

Identify the known variables. The side length of the square is $L = 1.0 \text{ m}$. 
The distance $r$ from any corner to the center of the square is half the length of the diagonal.

$$
r = \frac{L\sqrt{2}}{2} = \frac{1.0\sqrt{2}}{2} = \frac{1}{\sqrt{2}} \approx 0.707 \text{ m}
$$

Coulomb's constant is $k \approx 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$.

Write the superposition equation for the four charges:

$$
V_{center} = k \left( \frac{q_1}{r} + \frac{q_2}{r} + \frac{q_3}{r} + \frac{q_4}{r} \right)
$$

Factor out the common distance $r$:

$$
V_{center} = \frac{k}{r} (q_1 + q_2 + q_3 + q_4)
$$

Substitute the given charge values:

$$
\sum q = (+1) + (-2) + (+3) + (-4) = -2 \text{ C}
$$

Calculate the final potential:

$$
V_{center} = \frac{8.99 \times 10^9}{1/\sqrt{2}} (-2)
$$

$$
V_{center} = -2\sqrt{2} (8.99 \times 10^9)
$$

$$
V_{center} \approx -2(1.414)(8.99 \times 10^9) \approx -2.54 \times 10^{10} \text{ V}
$$

## Final Result

The electric potential at the center of the square is approximately $-2.54 \times 10^{10} \text{ V}$.

## Interpretation

The net negative potential at the center indicates that a positive test charge brought from infinity to this point would release potential energy (work is done by the electric field), primarily driven by the dominating influence of the $-4\text{C}$ and $-2\text{C}$ charges.
