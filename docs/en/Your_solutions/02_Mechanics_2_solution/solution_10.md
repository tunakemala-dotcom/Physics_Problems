# Task 10 – Force field and power

## Problem Statement

In a force field, a particle with mass $m=0.5 \text{ kg}$ has equations of motion:
$x = 5t^2 - t, \quad y = 2t^3, \quad z = -3t + 2$.
Find the time dependence of velocity, momentum, acceleration, force, and power.

## Theory

Kinematic vectors are obtained by successive time derivatives of the position vector $\vec{r}(t)$. 

* $\vec{v}(t) = d\vec{r}/dt$
* $\vec{a}(t) = d\vec{v}/dt$
* $\vec{p}(t) = m\vec{v}(t)$
* $\vec{F}(t) = m\vec{a}(t)$
* Power $P(t) = \vec{F}(t) \cdot \vec{v}(t)$

## Step-by-Step Solution

Given the position vector:

$$
\vec{r}(t) = (5t^2 - t, 2t^3, -3t + 2)
$$

### Velocity

Differentiate $\vec{r}(t)$ with respect to time:

$$
\vec{v}(t) = \left( \frac{d}{dt}(5t^2 - t), \frac{d}{dt}(2t^3), \frac{d}{dt}(-3t + 2) \right)
$$

$$
\vec{v}(t) = (10t - 1, 6t^2, -3)
$$

### Momentum

Multiply velocity by mass $m = 0.5$:

$$
\vec{p}(t) = 0.5(10t - 1, 6t^2, -3)
$$

$$
\vec{p}(t) = (5t - 0.5, 3t^2, -1.5)
$$

### Acceleration

Differentiate $\vec{v}(t)$ with respect to time:

$$
\vec{a}(t) = \left( \frac{d}{dt}(10t - 1), \frac{d}{dt}(6t^2), \frac{d}{dt}(-3) \right)
$$

$$
\vec{a}(t) = (10, 12t, 0)
$$

### Force

Apply Newton's Second Law ($\vec{F} = m\vec{a}$) using $m = 0.5$:

$$
\vec{F}(t) = 0.5(10, 12t, 0)
$$

$$
\vec{F}(t) = (5, 6t, 0)
$$

### Power

Calculate the dot product of Force and Velocity vectors:

$$
P(t) = \vec{F}(t) \cdot \vec{v}(t) = F_x v_x + F_y v_y + F_z v_z
$$

$$
P(t) = (5)(10t - 1) + (6t)(6t^2) + (0)(-3)
$$

$$
P(t) = 50t - 5 + 36t^3
$$

## Final Result

* Velocity: $\vec{v}(t) = (10t - 1, 6t^2, -3) \text{ m/s}$
* Momentum: $\vec{p}(t) = (5t - 0.5, 3t^2, -1.5) \text{ kg}\cdot\text{m/s}$
* Acceleration: $\vec{a}(t) = (10, 12t, 0) \text{ m/s}^2$
* Force: $\vec{F}(t) = (5, 6t, 0) \text{ N}$
* Power: $P(t) = 36t^3 + 50t - 5 \text{ W}$

## Interpretation

The force field acts entirely in the xy-plane because the z-acceleration is zero. Consequently, power is only transferred to/from the particle via the x and y components. The power transferred grows cubically with time due to the constantly increasing y-component of the force.
