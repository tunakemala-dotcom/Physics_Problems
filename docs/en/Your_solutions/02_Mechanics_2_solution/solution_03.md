# Task 03 – Conservation of Energy

## Problem Statement

A pendulum with a length of 1.0 meter is released from an initial angle of $15^\circ$. What is the speed of the pendulum bob at the bottom of its swing?

## Theory

The system is conservative, so mechanical energy is conserved. The potential energy at the highest point is completely converted into kinetic energy at the lowest point. 

$$
\Delta E_k + \Delta E_p = 0
$$

The change in height $h$ from the lowest point (the equilibrium position) to an angle $\theta$ is derived from geometry:

$$
h = L - L\cos(\theta) = L(1 - \cos(\theta))
$$

## Step-by-Step Solution

Set the potential energy at the bottom of the swing to zero ($E_{p,f} = 0$). 
The initial velocity is zero, so $E_{k,i} = 0$.

Equate the initial potential energy to the final kinetic energy:

$$
mgh = \frac{1}{2}mv^2
$$

The mass $m$ cancels out:

$$
gh = \frac{1}{2}v^2
$$

Solve for the velocity $v$:

$$
v = \sqrt{2gh}
$$

Substitute the expression for height $h = L(1 - \cos(\theta))$:

$$
v = \sqrt{2gL(1 - \cos(\theta))}
$$

Insert the numerical values ($L = 1.0 \text{ m}$, $\theta = 15^\circ$, $g \approx 9.81 \text{ m/s}^2$):

$$
v = \sqrt{2(9.81)(1.0)(1 - \cos(15^\circ))}
$$

$$
v = \sqrt{19.62(1 - 0.9659)}
$$

$$
v = \sqrt{19.62(0.0341)} \approx \sqrt{0.669} \approx 0.818 \text{ m/s}
$$

## Final Result

The speed of the pendulum bob at the bottom of its swing is approximately $0.818 \text{ m/s}$.

## Interpretation

Because gravity is a conservative force, the path taken by the bob does not affect the final speed. The speed at the lowest point is identical to that of an object dropped straight down from the same vertical height $h$.
