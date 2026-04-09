# Task 03 – Superposition Principle

## Problem Statement

Two waves are described by the equations $y_1(x, t) = A \sin(kx - \omega t)$ and $y_2(x, t) = A \sin(kx + \omega t)$. What is the equation of the resulting standing wave? Identify the positions of the nodes.

## Theory

The principle of superposition states that the resultant displacement is the algebraic sum of individual displacements. 
The sum of two sine functions can be expanded using the trigonometric identity:

$$
\sin(u) + \sin(v) = 2 \sin\left(\frac{u+v}{2}\right) \cos\left(\frac{u-v}{2}\right)
$$

## Step-by-Step Solution

### Standing Wave Equation

Apply the superposition principle:

$$
y(x,t) = y_1(x,t) + y_2(x,t) = A \sin(kx - \omega t) + A \sin(kx + \omega t)
$$

Let $u = kx - \omega t$ and $v = kx + \omega t$.

Compute the terms for the identity:

$$
\frac{u+v}{2} = \frac{kx - \omega t + kx + \omega t}{2} = kx
$$

$$
\frac{u-v}{2} = \frac{kx - \omega t - (kx + \omega t)}{2} = -\omega t
$$

Substitute into the identity:

$$
y(x,t) = 2A \sin(kx) \cos(-\omega t)
$$

Since cosine is an even function ($\cos(-\theta) = \cos(\theta)$):

$$
y(x,t) = 2A \sin(kx) \cos(\omega t)
$$

### Positions of Nodes

Nodes occur where the spatial amplitude is zero for all time $t$:

$$
\sin(kx) = 0
$$

This requires the argument to be an integer multiple of $\pi$:

$$
kx = n\pi \quad \text{for} \quad n = 0, \pm 1, \pm 2, \dots
$$

Substitute the wave number $k = \frac{2\pi}{\lambda}$:

$$
\frac{2\pi}{\lambda} x = n\pi
$$

Solve for $x$:

$$
x = \frac{n\lambda}{2}
$$

## Final Result

* Standing wave equation: $y(x,t) = [2A \sin(kx)] \cos(\omega t)$
* Positions of nodes: $x = n \frac{\lambda}{2}$ for $n \in \mathbb{Z}$

## Interpretation

The superposition of two identical waves traveling in opposite directions forms a standing wave. The medium oscillates in place with a time-varying amplitude defined by $\cos(\omega t)$ and a spatially varying envelope defined by $2A \sin(kx)$. The nodes are perfectly stationary points spaced exactly half a wavelength apart.
