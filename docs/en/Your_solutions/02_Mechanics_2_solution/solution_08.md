# Task 08 – Work of a variable force

## Problem Statement

Given a one-dimensional force $F(x) = -kx$:
1. Write down the equation of motion and solve it.
2. Calculate the work done during displacement from $0$ to $x_0$.
3. Interpret the result as potential energy and verify $F = -dU/dx$.
4. Draw the graph of $F(x)$ and $U(x)$.

## Theory

A force proportional to the negative displacement represents Hooke's Law (a linear restoring force), leading to simple harmonic motion. The work done by a conservative force is the negative of the change in potential energy:

$$
W = \int F(x) dx = -\Delta U
$$

## Step-by-Step Solution

### 1. Equation of Motion

From Newton's Second Law ($F = ma$):

$$
m \frac{d^2 x}{dt^2} = -kx
$$

Rearranging yields a second-order linear homogeneous differential equation:

$$
\frac{d^2 x}{dt^2} + \frac{k}{m} x = 0
$$

Letting $\omega^2 = k/m$, the general solution is:

$$
x(t) = A \cos(\omega t + \phi)
$$

where $A$ and $\phi$ are constants determined by initial conditions.

### 2. Work Done

The work done by the force from $x=0$ to $x=x_0$ is:

$$
W = \int_0^{x_0} F(x) dx = \int_0^{x_0} (-kx) dx
$$

$$
W = \left[ -\frac{1}{2} k x^2 \right]_0^{x_0} = -\frac{1}{2} k x_0^2
$$

### 3. Potential Energy and Verification

The change in potential energy is defined as $\Delta U = -W$. Setting the reference point $U(0) = 0$:

$$
U(x_0) - U(0) = - \left(-\frac{1}{2} k x_0^2\right)
$$

$$
U(x_0) = \frac{1}{2} k x_0^2
$$

Generalizing for any $x$:

$$
U(x) = \frac{1}{2} k x^2
$$

Verify the relationship $F = -dU/dx$:

$$
-\frac{dU}{dx} = -\frac{d}{dx} \left( \frac{1}{2} k x^2 \right) = -k x = F(x)
$$

This perfectly matches the given force.

### 4. Graphs

The graph of $F(x) = -kx$ is a straight line passing through the origin with a negative slope $-k$.
The graph of $U(x) = \frac{1}{2}kx^2$ is an upward-opening parabola with its vertex at the origin.

```text
    F(x)                          U(x)
      |                             |    .   |   .
      |      .                      |   .    |    .
      |    .                        |  .     |     .
______|__.______ x            ______|_.______|____._ x
    . |                             |
  .   |                             |
.     |                             |
