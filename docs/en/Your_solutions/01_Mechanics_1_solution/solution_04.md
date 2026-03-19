# Task 04 – Vector Calculus

## Problem Statement

The position of an object is given by $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$. Find the object's velocity and acceleration vectors as a function of time.

## Theory

The velocity vector is the first time derivative of the position vector. The acceleration vector is the first time derivative of the velocity vector, which is equivalent to the second time derivative of the position vector.

$$
\vec{v}(t) = \frac{d\vec{r}(t)}{dt}
$$

$$
\vec{a}(t) = \frac{d\vec{v}(t)}{dt} = \frac{d^2\vec{r}(t)}{dt^2}
$$

## Step-by-Step Solution

### Velocity Vector

Differentiate each component of the position vector $\vec{r}(t)$ with respect to time $t$:

$$
v_x(t) = \frac{d}{dt}(3t^2) = 6t
$$

$$
v_y(t) = \frac{d}{dt}(5t - 8t^2) = 5 - 16t
$$

Combine the components into the velocity vector:

$$
\vec{v}(t) = (6t)\hat{i} + (5 - 16t)\hat{j}
$$

### Acceleration Vector

Differentiate each component of the velocity vector $\vec{v}(t)$ with respect to time $t$:

$$
a_x(t) = \frac{d}{dt}(6t) = 6
$$

$$
a_y(t) = \frac{d}{dt}(5 - 16t) = -16
$$

Combine the components into the acceleration vector:

$$
\vec{a}(t) = (6)\hat{i} + (-16)\hat{j}
$$

## Final Result

Velocity: $\vec{v}(t) = 6t \hat{i} + (5 - 16t) \hat{j}$

Acceleration: $\vec{a}(t) = 6 \hat{i} - 16 \hat{j}$

## Interpretation

The acceleration vector is constant in both magnitude and direction, as it has no time dependence. This means the object is undergoing uniformly accelerated motion in a two-dimensional plane.
