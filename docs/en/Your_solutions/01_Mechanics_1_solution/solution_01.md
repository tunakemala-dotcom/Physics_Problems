# Task 01 – Projectile Motion

## Problem Statement

A projectile is fired from the ground with an initial velocity of $100 \text{ m/s}$ at an angle of $37^\circ$ above the horizontal. Assume no air resistance. Derive the differential equations of motion, and determine the time of flight, the maximum height, and the range.

## Theory

Projectile motion in two dimensions is governed by Newton's Second Law. In the absence of air resistance, the only force acting on the object is gravity, which points downwards.

The acceleration vector is constant:

$$
\vec{a} = (0, -g)
$$

The equations of kinematics for constant acceleration are obtained by integrating the acceleration with respect to time.

## Step-by-Step Solution

### Differential Equations of Motion

From Newton's Second Law:

$$
\frac{d^2 x}{dt^2} = 0
$$

$$
\frac{d^2 y}{dt^2} = -g
$$

Integrating once with respect to time yields the velocity components. The initial velocity components are $v_{0x} = v_0 \cos(\theta)$ and $v_{0y} = v_0 \sin(\theta)$.

$$
\frac{dx}{dt} = v_0 \cos(\theta)
$$

$$
\frac{dy}{dt} = v_0 \sin(\theta) - gt
$$

Integrating a second time yields the position functions, assuming the initial position is $(0,0)$:

$$
\begin{align}
x(t) &= v_0 \cos(\theta) t \\
y(t) &= v_0 \sin(\theta) t - \frac{1}{2}gt^2
\end{align}
$$

### Time of Flight

The projectile lands when $y(t) = 0$ for $t > 0$:

$$
v_0 \sin(\theta) t - \frac{1}{2}gt^2 = 0
$$

Solving for $t$:

$$
t = \frac{2v_0 \sin(\theta)}{g}
$$

Using $v_0 = 100 \text{ m/s}$, $\theta = 37^\circ$, and $g = 9.81 \text{ m/s}^2$:

$$
t = \frac{2(100) \sin(37^\circ)}{9.81} \approx \frac{200(0.6018)}{9.81} \approx 12.27 \text{ s}
$$

### Maximum Height

The maximum height is reached when the vertical velocity is zero:

$$
v_y(t) = v_0 \sin(\theta) - gt_{top} = 0
$$

$$
t_{top} = \frac{v_0 \sin(\theta)}{g}
$$

Substituting $t_{top}$ into the $y(t)$ equation:

$$
h_{max} = y(t_{top}) = \frac{(v_0 \sin(\theta))^2}{2g}
$$

Calculating the value:

$$
h_{max} = \frac{(100 \sin(37^\circ))^2}{2(9.81)} \approx \frac{(60.18)^2}{19.62} \approx 184.6 \text{ m}
$$

### Range

The range is the horizontal distance traveled during the time of flight $t = 2v_0 \sin(\theta)/g$:

$$
R = x(t_{flight}) = v_0 \cos(\theta) \left( \frac{2v_0 \sin(\theta)}{g} \right)
$$

Using the trigonometric identity $2 \sin(\theta)\cos(\theta) = \sin(2\theta)$:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

Calculating the value:

$$
R = \frac{(100)^2 \sin(74^\circ)}{9.81} \approx \frac{10000(0.9613)}{9.81} \approx 979.9 \text{ m}
$$

## Final Result

* Time of flight: $12.27 \text{ s}$
* Maximum height: $184.6 \text{ m}$
* Range: $979.9 \text{ m}$

## Interpretation

The decoupling of horizontal and vertical motions allows them to be analyzed independently. The horizontal motion is uniform, while the vertical motion is uniformly accelerated due to gravity. The time of flight is entirely dictated by the vertical component of the initial velocity.
