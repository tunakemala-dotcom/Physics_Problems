# Task 11 – Dynamics with a time-dependent force

## Problem Statement

A particle of mass $m=3 \text{ kg}$ moves in a time-dependent force field: $\vec{F} = (15t, 3t-12, -6t^2) \text{ N}$.
Given initial conditions $\vec{r}_0=(5,2,-3) \text{ m}$ and $\vec{v}_0=(2,0,1) \text{ m/s}$, find the position and velocity dependence on time.

## Theory

Using Newton's Second Law, the acceleration vector is $\vec{a}(t) = \vec{F}(t) / m$.
Velocity is the time integral of acceleration, and position is the time integral of velocity. Initial conditions are used to solve for integration constants.

## Step-by-Step Solution

### Acceleration

Divide the force vector by the mass $m=3$:

$$
\vec{a}(t) = \left( \frac{15t}{3}, \frac{3t-12}{3}, \frac{-6t^2}{3} \right)
$$

$$
\vec{a}(t) = (5t, t - 4, -2t^2)
$$

### Velocity

Integrate $\vec{a}(t)$ to find $\vec{v}(t)$:

$$
\vec{v}(t) = \int (5t, t - 4, -2t^2) dt
$$

$$
\vec{v}(t) = \left( \frac{5}{2}t^2 + C_x, \frac{1}{2}t^2 - 4t + C_y, -\frac{2}{3}t^3 + C_z \right)
$$

Use the initial condition $\vec{v}(0) = (2, 0, 1)$ to find the constants:

$$
C_x = 2, \quad C_y = 0, \quad C_z = 1
$$

Thus, the velocity vector is:

$$
\vec{v}(t) = \left( 2.5t^2 + 2, 0.5t^2 - 4t, -\frac{2}{3}t^3 + 1 \right)
$$

### Position

Integrate $\vec{v}(t)$ to find $\vec{r}(t)$:

$$
\vec{r}(t) = \int \left( 2.5t^2 + 2, 0.5t^2 - 4t, -\frac{2}{3}t^3 + 1 \right) dt
$$

$$
\vec{r}(t) = \left( \frac{2.5}{3}t^3 + 2t + K_x, \frac{0.5}{3}t^3 - 2t^2 + K_y, -\frac{2}{12}t^4 + t + K_z \right)
$$

Simplify fractions:

$$
\vec{r}(t) = \left( \frac{5}{6}t^3 + 2t + K_x, \frac{1}{6}t^3 - 2t^2 + K_y, -\frac{1}{6}t^4 + t + K_z \right)
$$

Use the initial condition $\vec{r}(0) = (5, 2, -3)$ to find the constants:

$$
K_x = 5, \quad K_y = 2, \quad K_z = -3
$$

Thus, the position vector is:

$$
\vec{r}(t) = \left( \frac{5}{6}t^3 + 2t + 5, \frac{1}{6}t^3 - 2t^2 + 2, -\frac{1}{6}t^4 + t - 3 \right)
$$

## Final Result

* Velocity: $\vec{v}(t) = (2.5t^2 + 2, 0.5t^2 - 4t, -\frac{2}{3}t^3 + 1)$
* Position: $\vec{r}(t) = (\frac{5}{6}t^3 + 2t + 5, \frac{1}{6}t^3 - 2t^2 + 2, -\frac{1}{6}t^4 + t - 3)$

## Interpretation

The polynomial force produces higher-order polynomial trajectories in all three dimensions. The initial velocity and position define the origin of integration, preventing the constants from vanishing and preserving the object's history of motion before $t=0$.
