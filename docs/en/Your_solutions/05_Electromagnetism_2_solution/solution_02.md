# Task 02 – Ampere's Law

## Problem Statement

Two long, parallel wires are $10 \text{ cm}$ apart and carry currents of $5 \text{ A}$ in opposite directions. Calculate the magnitude and direction of the magnetic field at a point midway between the wires.

## Theory

The magnetic field produced by a long straight wire at a distance $r$ is derived from Ampere's Law:

$$
B = \frac{\mu_0 I}{2\pi r}
$$

By the right-hand rule, if two parallel wires carry currents in opposite directions, their magnetic fields in the space exactly between them will point in the same direction and constructively interfere.

## Step-by-Step Solution

Identify the constants and given values:
* Permeability of free space $\mu_0 = 4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$
* Current $I_1 = I_2 = 5 \text{ A}$
* Distance between wires $d = 10 \text{ cm} = 0.1 \text{ m}$
* Distance from each wire to the midpoint $r = d/2 = 0.05 \text{ m}$

Calculate the magnetic field magnitude from one wire at the midpoint:

$$
B_1 = \frac{(4\pi \times 10^{-7})(5)}{2\pi(0.05)}
$$

$$
B_1 = \frac{2 \times 10^{-7} \times 5}{0.05} = \frac{10^{-6}}{0.05} = 2 \times 10^{-5} \text{ T}
$$

Because the currents flow in opposite directions, the fields $B_1$ and $B_2$ point in the same direction at the midpoint. Therefore, the net magnetic field is the sum of their magnitudes:

$$
B_{net} = B_1 + B_2 = 2 \times 10^{-5} + 2 \times 10^{-5}
$$

$$
B_{net} = 4 \times 10^{-5} \text{ T}
$$

## Final Result

The magnitude of the magnetic field at the midpoint is $4 \times 10^{-5} \text{ T}$ (or $40 \text{ }\mu\text{T}$). The direction is perpendicular to the plane containing the wires, determined by the right-hand rule.

## Interpretation

When currents flow in anti-parallel directions, the region between the wires experiences a reinforced, enhanced magnetic field. This is the underlying principle used to maximize field strength in certain coil and loop geometries.
