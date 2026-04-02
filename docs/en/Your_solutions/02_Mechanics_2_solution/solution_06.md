# Task 06 – Energy Dissipation

## Problem Statement

A tennis ball is dropped from a height of $2.0 \text{ m}$. After each bounce, it loses 30% of its mechanical energy. To what height does it rise after the second bounce?

## Theory

If an object loses a fixed percentage of its energy, the remaining energy forms a geometric sequence. 
Losing 30% means that 70% of the mechanical energy remains after each bounce. 
At maximum height $h_n$ after the $n$-th bounce, the mechanical energy is purely gravitational potential energy:

$$
E_n = mgh_n
$$

## Step-by-Step Solution

Let the initial mechanical energy be $E_0 = mgh_0$, where $h_0 = 2.0 \text{ m}$.

After the first bounce, the remaining energy is:

$$
E_1 = 0.70 E_0
$$

After the second bounce, the remaining energy is:

$$
E_2 = 0.70 E_1 = 0.70 (0.70 E_0) = 0.49 E_0
$$

Express $E_2$ in terms of potential energy:

$$
mgh_2 = 0.49 (mgh_0)
$$

The mass $m$ and gravitational acceleration $g$ cancel out:

$$
h_2 = 0.49 h_0
$$

Substitute the initial height:

$$
h_2 = 0.49 (2.0) = 0.98 \text{ m}
$$

## Final Result

The ball rises to a height of $0.98 \text{ m}$ after the second bounce.

## Interpretation

The coefficient of restitution governs the energy loss during collisions with the ground. Because the loss is a percentage, the bounce height decays exponentially. Even though only 30% of energy is lost per bounce, over half the total energy (51%) is dissipated by the time the ball reaches its second peak.
