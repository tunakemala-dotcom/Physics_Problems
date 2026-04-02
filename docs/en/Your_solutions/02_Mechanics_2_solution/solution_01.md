# Task 01 – Gravitational Dependence

## Problem Statement

A simple pendulum has a period of 4 seconds on Earth. What would its period be on the Moon, where the gravitational acceleration is about 1/6th of Earth's? What is the required length of a simple pendulum to have a period of exactly 1 second on Earth?

## Theory

The period $T$ of a simple pendulum undergoing small oscillations is independent of the mass and depends only on its length $L$ and the local acceleration due to gravity $g$:

$$
T = 2\pi\sqrt{\frac{L}{g}}
$$

## Step-by-Step Solution

### Period on the Moon

Let $T_E = 4 \text{ s}$ be the period on Earth with gravity $g_E$. Let $T_M$ be the period on the Moon with gravity $g_M = g_E / 6$. 

The equations for the periods are:

$$
\begin{align}
T_E &= 2\pi\sqrt{\frac{L}{g_E}} \\
T_M &= 2\pi\sqrt{\frac{L}{g_M}}
\end{align}
$$

Substitute $g_M$:

$$
T_M = 2\pi\sqrt{\frac{L}{g_E / 6}} = 2\pi\sqrt{6\frac{L}{g_E}} = \sqrt{6} \left( 2\pi\sqrt{\frac{L}{g_E}} \right)
$$

$$
T_M = \sqrt{6} T_E
$$

Calculate the value:

$$
T_M = 4\sqrt{6} \approx 4(2.449) \approx 9.80 \text{ s}
$$

### Length for a 1-second period on Earth

Rearrange the period formula to solve for $L$:

$$
T = 2\pi\sqrt{\frac{L}{g}}
$$

$$
T^2 = 4\pi^2 \frac{L}{g}
$$

$$
L = \frac{g T^2}{4\pi^2}
$$

Substitute $T = 1 \text{ s}$ and standard Earth gravity $g \approx 9.81 \text{ m/s}^2$:

$$
L = \frac{9.81 (1)^2}{4\pi^2} \approx \frac{9.81}{39.478} \approx 0.248 \text{ m}
$$

## Final Result

* Period on the Moon: $9.80 \text{ s}$
* Length for $T=1 \text{ s}$ on Earth: $0.248 \text{ m}$ (or $24.8 \text{ cm}$)

## Interpretation

Decreasing the restoring force (gravity) makes the pendulum swing more slowly, thus increasing the period. A pendulum on the Moon takes roughly 2.45 times longer to complete one oscillation than an identical pendulum on Earth.
