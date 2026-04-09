# Task 06 – Wave Equation

## Problem Statement

A wave is described by the equation $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$, where $x$ and $y$ are in meters and $t$ is in seconds. Determine the wave's amplitude $A$, wavelength $\lambda$, frequency $f$, and wave speed $v$.

## Theory

The standard mathematical form of a 1D harmonic traveling wave is:

$$
y(x,t) = A \sin(kx - \omega t + \phi)
$$

By direct comparison with the standard form, the wave parameters can be extracted:
* Amplitude: $A$
* Wave number: $k = \frac{2\pi}{\lambda}$
* Angular frequency: $\omega = 2\pi f$
* Wave speed: $v = \frac{\omega}{k} = \lambda f$

## Step-by-Step Solution

Compare $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$ to $y(x,t) = A \sin(kx - \omega t)$:

### a) Amplitude

Directly from the coefficient:

$$
A = 0.05 \text{ m}
$$

### b) Wavelength

From the spatial term, $k = 2\pi \text{ rad/m}$.

$$
k = \frac{2\pi}{\lambda} \implies 2\pi = \frac{2\pi}{\lambda}
$$

$$
\lambda = 1 \text{ m}
$$

### c) Frequency

From the temporal term, $\omega = 50\pi \text{ rad/s}$.

$$
\omega = 2\pi f \implies 50\pi = 2\pi f
$$

$$
f = 25 \text{ Hz}
$$

### d) Wave Speed

Calculate using frequency and wavelength:

$$
v = \lambda f = (1)(25) = 25 \text{ m/s}
$$

Alternatively, use $\omega$ and $k$:

$$
v = \frac{\omega}{k} = \frac{50\pi}{2\pi} = 25 \text{ m/s}
$$

## Final Result

* Amplitude $A = 0.05 \text{ m}$
* Wavelength $\lambda = 1 \text{ m}$
* Frequency $f = 25 \text{ Hz}$
* Wave speed $v = 25 \text{ m/s}$

## Interpretation

The negative sign between the spatial and temporal terms in the argument $(kx - \omega t)$ indicates that this transverse wave is traveling in the positive $x$-direction at $25 \text{ m/s}$.
