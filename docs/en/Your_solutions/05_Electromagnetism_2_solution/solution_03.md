# Task 03 – Biot-Savart Law

## Problem Statement

A small segment of a line wire of length $0.1 \text{ m}$ carries a current of $3 \text{ A}$. The segment is located at a distance of $0.2 \text{ m}$ from a point P. Calculate the magnetic field at point P due to this current segment (assume the segment is perpendicular to the line connecting it to point P).

## Theory

The Biot-Savart Law gives the magnetic field contribution $dB$ from a small current element $dl$:

$$
dB = \frac{\mu_0 I dl \sin(\theta)}{4\pi r^2}
$$

For a short, finite segment approximated as a differential element, we can evaluate the magnitude using this formula directly.

## Step-by-Step Solution

Identify the given values:
* Current $I = 3 \text{ A}$
* Segment length $dl = 0.1 \text{ m}$
* Distance $r = 0.2 \text{ m}$
* Angle $\theta = 90^\circ$ (perpendicular)

Substitute the values into the Biot-Savart equation:

$$
B \approx \frac{(4\pi \times 10^{-7})(3)(0.1)\sin(90^\circ)}{4\pi(0.2)^2}
$$

Cancel the $4\pi$ terms and evaluate:

$$
B \approx \frac{10^{-7} (0.3)(1)}{0.04}
$$

$$
B \approx \frac{3 \times 10^{-8}}{0.04} = 7.5 \times 10^{-7} \text{ T}
$$

## Final Result

The magnetic field at point P is approximately $7.5 \times 10^{-7} \text{ T}$.

## Interpretation

This calculation assumes the segment is small enough relative to the distance $r$ that the field contribution can be treated as a single point source. The perpendicular orientation ensures the sine term is maximized, yielding the strongest possible field for this distance.
