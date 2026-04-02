# Task 02 – Harmonic Motion

## Problem Statement

A 10 kg mass is attached to a spring and oscillates according to the equation $x(t) = 0.2 \cos(10\pi t)$ (in meters). What is the spring constant $k$? What is the total mechanical energy of the system?

## Theory

For simple harmonic motion, the position as a function of time is given by:

$$
x(t) = A \cos(\omega t + \phi)
$$

where $A$ is the amplitude and $\omega$ is the angular frequency. The angular frequency is related to the mass $m$ and spring constant $k$ by:

$$
\omega = \sqrt{\frac{k}{m}}
$$

The total mechanical energy $E$ of a simple harmonic oscillator is constant and is equal to its maximum potential energy:

$$
E = \frac{1}{2} k A^2
$$

## Step-by-Step Solution

### Spring Constant $k$

By comparing the given equation $x(t) = 0.2 \cos(10\pi t)$ to the standard form, we identify:

* Amplitude $A = 0.2 \text{ m}$
* Angular frequency $\omega = 10\pi \text{ rad/s}$

Rearrange the angular frequency formula to solve for $k$:

$$
k = m \omega^2
$$

Substitute the known values ($m = 10 \text{ kg}$):

$$
k = 10 (10\pi)^2 = 10 (100\pi^2) = 1000\pi^2 \text{ N/m}
$$

Using $\pi^2 \approx 9.8696$:

$$
k \approx 9869.6 \text{ N/m}
$$

### Total Mechanical Energy

Substitute $k$ and $A$ into the energy equation:

$$
E = \frac{1}{2} (1000\pi^2) (0.2)^2
$$

$$
E = 500\pi^2 (0.04) = 20\pi^2 \text{ J}
$$

Using $\pi^2 \approx 9.8696$:

$$
E \approx 197.4 \text{ J}
$$

## Final Result

* Spring constant: $k = 1000\pi^2 \text{ N/m} \approx 9869.6 \text{ N/m}$
* Total mechanical energy: $E = 20\pi^2 \text{ J} \approx 197.4 \text{ J}$

## Interpretation

The very high angular frequency ($10\pi \text{ rad/s}$ or $5 \text{ Hz}$) for a massive $10 \text{ kg}$ object implies a very stiff spring. The total energy remains constant throughout the motion, shifting continuously between kinetic and elastic potential energy.
