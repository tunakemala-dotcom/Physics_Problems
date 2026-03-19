# Task 08 – Circular Motion

## Problem Statement

Calculate the centripetal acceleration of a person standing on the Earth's equator. The Earth's radius is approximately $6378 \text{ km}$.

## Theory

An object undergoing uniform circular motion with radius $r$ and angular velocity $\omega$ experiences a centripetal acceleration directed towards the center of the circle.

$$
a_c = \omega^2 r = \frac{v^2}{r}
$$

The angular velocity $\omega$ relates to the period $T$ of rotation by:

$$
\omega = \frac{2\pi}{T}
$$

## Step-by-Step Solution

Identify the knowns:
* $r = 6378 \text{ km} = 6378000 \text{ m}$
* The period of Earth's rotation relative to the stars (sidereal day) is $T \approx 23 \text{ hours}, 56 \text{ minutes}, 4 \text{ seconds} = 86164 \text{ s}$. For a simple approximation, $T \approx 24 \text{ h} = 86400 \text{ s}$ can also be used, but the sidereal day is more precise. We will use $86164 \text{ s}$.

Calculate the angular velocity:

$$
\omega = \frac{2\pi}{86164} \approx 7.292 \times 10^{-5} \text{ rad/s}
$$

Calculate the centripetal acceleration:

$$
a_c = (7.292 \times 10^{-5})^2 (6378000)
$$

$$
a_c \approx (5.317 \times 10^{-9}) (6378000) \approx 0.0339 \text{ m/s}^2
$$

## Final Result

The centripetal acceleration at the equator is approximately $0.0339 \text{ m/s}^2$.

## Interpretation

This acceleration is small compared to the acceleration due to gravity ($g \approx 9.8 \text{ m/s}^2$). However, it is responsible for the slight bulging of the Earth at the equator and causes the effective gravitational acceleration measured at the equator to be slightly less than at the poles.
