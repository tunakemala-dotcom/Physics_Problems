# Task 03 – Electrostatic Equilibrium

## Problem Statement

Find the equilibrium position for a charge $q_3 = +1\text{C}$ placed on the line between a charge $q_1 = +4\text{C}$ and a charge $q_2 = +9\text{C}$, which are separated by a distance of $2 \text{ m}$.

## Theory

For a charge to be in electrostatic equilibrium, the net electric force acting on it must be zero. If $q_3$ is placed between two positive charges, both will exert a repulsive force on it. Equilibrium requires these two opposing forces to be equal in magnitude.

$$
|\vec{F}_{13}| = |\vec{F}_{23}|
$$

## Step-by-Step Solution

Let the position of $q_1$ be $x = 0$. 
Let the position of $q_2$ be $x = d = 2 \text{ m}$.
Let the equilibrium position of $q_3$ be $x$. The distance to $q_1$ is $x$, and the distance to $q_2$ is $(2 - x)$.

Set the force magnitudes equal:

$$
k \frac{|q_1 q_3|}{x^2} = k \frac{|q_2 q_3|}{(2 - x)^2}
$$

The constants $k$ and the test charge $q_3$ cancel out from both sides:

$$
\frac{q_1}{x^2} = \frac{q_2}{(2 - x)^2}
$$

Substitute the given charge values ($q_1 = 4$, $q_2 = 9$):

$$
\frac{4}{x^2} = \frac{9}{(2 - x)^2}
$$

Take the positive square root of both sides, as the position $x$ must lie physically between the two charges ($0 < x < 2$):

$$
\frac{2}{x} = \frac{3}{2 - x}
$$

Cross-multiply to solve for $x$:

$$
2(2 - x) = 3x
$$

$$
4 - 2x = 3x
$$

$$
4 = 5x
$$

$$
x = 0.8 \text{ m}
$$

## Final Result

The equilibrium position for $q_3$ is $0.8 \text{ m}$ from the $+4\text{C}$ charge (and $1.2 \text{ m}$ from the $+9\text{C}$ charge).

## Interpretation

The equilibrium point is closer to the smaller charge ($q_1$). Because electric force follows an inverse-square law, being physically closer to the weaker charge compensates for its smaller magnitude, allowing it to exactly balance the repulsive push from the much larger, but more distant, $q_2$ charge.
