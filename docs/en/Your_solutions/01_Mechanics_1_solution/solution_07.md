# Task 07 – Elimination of time and interpretation of acceleration

## Problem Statement

The path equation is given in parametric form: $x(t)=2t^2, \quad y(t)=3t^3$. 
Eliminate the parameter $t$. Draw the trajectory. Calculate $\vec{v}(t)$, $|\vec{v}(t)|$, $\vec{a}(t)$ and $|\vec{a}(t)|$. Is the acceleration constant?

## Theory

To find the Cartesian equation of the trajectory, the time parameter $t$ must be isolated in one equation and substituted into the other. Kinematic vectors are found via successive differentiation.

## Step-by-Step Solution

### Eliminate Parameter $t$

From the $x(t)$ equation (assuming $t \ge 0$ for a single-valued branch):

$$
t = \sqrt{\frac{x}{2}}
$$

Substitute into the $y(t)$ equation:

$$
y(x) = 3 \left(\sqrt{\frac{x}{2}}\right)^3 = 3 \left(\frac{x}{2}\right)^{3/2} = \frac{3}{2\sqrt{2}} x^{3/2}
$$

This represents a semi-cubical parabola. 

### Kinematic Vectors

Differentiate the position vector $\vec{r}(t) = (2t^2, 3t^3)$ to find velocity:

$$
\vec{v}(t) = \left( \frac{d}{dt}(2t^2), \frac{d}{dt}(3t^3) \right) = (4t, 9t^2)
$$

Calculate the magnitude of velocity (speed):

$$
|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}
$$

Differentiate velocity to find acceleration:

$$
\vec{a}(t) = \left( \frac{d}{dt}(4t), \frac{d}{dt}(9t^2) \right) = (4, 18t)
$$

Calculate the magnitude of acceleration:

$$
|\vec{a}(t)| = \sqrt{4^2 + (18t)^2} = \sqrt{16 + 324t^2} = 2\sqrt{4 + 81t^2}
$$

### Is Acceleration Constant?

The acceleration vector is $\vec{a}(t) = (4, 18t)$. Since the $y$-component depends on time $t$, the vector changes over time.

## Final Result

* Path equation: $y(x) = \frac{3}{2\sqrt{2}} x^{3/2}$
* $\vec{v}(t) = (4t, 9t^2)$
* $|\vec{v}(t)| = t\sqrt{16 + 81t^2}$
* $\vec{a}(t) = (4, 18t)$
* $|\vec{a}(t)| = 2\sqrt{4 + 81t^2}$
* The acceleration is not constant.

## Interpretation

The object is accelerating uniformly in the x-direction but experiences linearly increasing acceleration in the y-direction. This results in the object tracing a curve that bends increasingly sharply upwards.
