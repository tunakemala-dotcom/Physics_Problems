# Task 07 – Cyclotron Motion

## Problem Statement

An electron is accelerated from rest through a potential difference of 5000 V. It then enters a region of uniform magnetic field B = 0.1 T, perpendicular to its velocity. What is the radius of the circular path it will follow?

## Theory

When an electron accelerates across a potential difference $V$, its potential energy converts entirely into kinetic energy:

$$
qV = \frac{1}{2} m v^2
$$

When a charged particle enters a uniform perpendicular magnetic field, the Lorentz force acts as a centripetal force, creating a circular trajectory:

$$
qvB = \frac{m v^2}{r}
$$

## Step-by-Step Solution

### Step 1: Find Velocity

Isolate the velocity $v$ from the kinetic energy equation:

$$
v = \sqrt{\frac{2qV}{m}}
$$

### Step 2: Formulate Radius Equation

Rearrange the magnetic force equation to solve for the radius $r$:

$$
r = \frac{mv}{qB}
$$

Substitute the expression for velocity into the radius equation:

$$
r = \frac{m}{qB} \sqrt{\frac{2qV}{m}} = \frac{1}{B} \sqrt{\frac{2mV}{q}}
$$

### Step 3: Calculate Value

Identify constants for the electron:
* Mass $m = 9.11 \times 10^{-31} \text{ kg}$
* Charge $q = 1.60 \times 10^{-19} \text{ C}$
* Field $B = 0.1 \text{ T}$
* Voltage $V = 5000 \text{ V}$

Substitute into the derived formula:

$$
r = \frac{1}{0.1} \sqrt{\frac{2(9.11 \times 10^{-31})(5000)}{1.60 \times 10^{-19}}}
$$

$$
r = 10 \sqrt{\frac{9.11 \times 10^{-27}}{1.60 \times 10^{-19}}}
$$

$$
r = 10 \sqrt{5.69 \times 10^{-8}}
$$

$$
r = 10 (2.386 \times 10^{-4}) \approx 2.386 \times 10^{-3} \text{ m}
$$

## Final Result

The radius of the circular path is approximately $2.39 \text{ mm}$.

## Interpretation

The magnetic field strongly confines the highly energetic electron into a millimeter-scale loop. Because the radius depends on the square root of the accelerating voltage, quadrupling the voltage would only double the orbit size.
