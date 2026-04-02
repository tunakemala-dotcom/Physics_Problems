# Task 12 – Work and energy with a constant force

## Problem Statement

A constant force acts on a body of mass $m = 2 \text{ kg}$: $\vec{F} = [6, 2] \text{ N}$.
Initial velocity $\vec{v}(0) = (1, -1) \text{ m/s}$, initial position $\vec{r}(0)=(0,0) \text{ m}$.
Find $\vec{a}(t)$, $\vec{v}(t)$, $\vec{r}(t)$, draw/describe the trajectory, calculate work done at $t=3 \text{ s}$, and verify the work-energy theorem.

## Theory

For a constant force, motion is uniformly accelerated.

$$
\vec{a} = \frac{\vec{F}}{m}
$$

The work-energy theorem states that the work done on an object equals its change in kinetic energy:

$$
W = \Delta KE = \frac{1}{2}m|\vec{v}_f|^2 - \frac{1}{2}m|\vec{v}_i|^2
$$

Work can also be directly calculated as $W = \vec{F} \cdot \Delta\vec{r}$.

## Step-by-Step Solution

### Kinematic Vectors

Acceleration:

$$
\vec{a}(t) = \frac{\vec{F}}{m} = \left( \frac{6}{2}, \frac{2}{2} \right) = (3, 1) \text{ m/s}^2
$$

Velocity (integrate $\vec{a}$):

$$
\vec{v}(t) = \int (3, 1) dt = (3t + C_x, t + C_y)
$$

Apply $\vec{v}(0) = (1, -1)$:

$$
\vec{v}(t) = (3t + 1, t - 1) \text{ m/s}
$$

Position (integrate $\vec{v}$):

$$
\vec{r}(t) = \int (3t + 1, t - 1) dt = (1.5t^2 + t + K_x, 0.5t^2 - t + K_y)
$$

Apply $\vec{r}(0) = (0, 0)$:

$$
\vec{r}(t) = (1.5t^2 + t, 0.5t^2 - t) \text{ m}
$$

### Trajectory

To find the Cartesian equation, isolate $t^2$ from the y-coordinate:

$$
y = 0.5t^2 - t \implies 3y = 1.5t^2 - 3t
$$

Subtract this from the x-coordinate:

$$
x - 3y = (1.5t^2 + t) - (1.5t^2 - 3t) = 4t \implies t = \frac{x - 3y}{4}
$$

Substitute back into $y(t)$ to obtain a parabolic equation $y = f(x)$. The trajectory is an oblique parabola in the xy-plane.

### Work Done at $t = 3 \text{ s}$

Evaluate the displacement vector at $t = 3$:

$$
\Delta\vec{r} = \vec{r}(3) - \vec{r}(0) = (1.5(3)^2 + 3, 0.5(3)^2 - 3) = (13.5 + 3, 4.5 - 3) = (16.5, 1.5) \text{ m}
$$

Calculate work via dot product:

$$
W = \vec{F} \cdot \Delta\vec{r} = (6)(16.5) + (2)(1.5) = 99 + 3 = 102 \text{ J}
$$

### Consistency with Work-Energy Theorem

Calculate initial kinetic energy ($t = 0$):

$$
|\vec{v}(0)|^2 = 1^2 + (-1)^2 = 2
$$

$$
KE_i = \frac{1}{2}m |\vec{v}(0)|^2 = \frac{1}{2}(2)(2) = 2 \text{ J}
$$

Calculate final kinetic energy ($t = 3$):

$$
\vec{v}(3) = (3(3) + 1, 3 - 1) = (10, 2)
$$

$$
|\vec{v}(3)|^2 = 10^2 + 2^2 = 104
$$

$$
KE_f = \frac{1}{2}m |\vec{v}(3)|^2 = \frac{1}{2}(2)(104) = 104 \text{ J}
$$

Calculate change in kinetic energy:

$$
\Delta KE = KE_f - KE_i = 104 - 2 = 102 \text{ J}
$$

## Final Result

* $\vec{a}(t) = (3, 1)$
* $\vec{v}(t) = (3t + 1, t - 1)$
* $\vec{r}(t) = (1.5t^2 + t, 0.5t^2 - t)$
* Work done: $W = 102 \text{ J}$
* Work-Energy theorem is perfectly consistent ($\Delta KE = 102 \text{ J} = W$).

## Interpretation

The two independent methods of finding work—evaluating the spatial path integral (dot product for a constant force) and comparing velocity magnitudes (kinetic energy)—yield the exact same value. The parabolic trajectory arises from uniform acceleration applied diagonally to the initial velocity.
