# Task 06 – EM Wave Analysis

## Problem Statement

An electromagnetic wave has its electric field component described by $E_y(x,t) = 100\sin(10^7x - \omega t) \text{ V/m}$. What is the direction of propagation? What is the wavelength $\lambda$? What is the angular frequency $\omega$? What is the equation for the magnetic field component?

## Theory

The standard equation for a plane electromagnetic wave is $E(x,t) = E_0 \sin(kx \pm \omega t)$. 
* The argument $(kx - \omega t)$ indicates propagation in the positive $x$-direction.
* Wave number $k = \frac{2\pi}{\lambda}$.
* Angular frequency $\omega = c k$.
* The magnetic field magnitude is $B_0 = \frac{E_0}{c}$, and its vector must be perpendicular to both $\vec{E}$ and the propagation direction such that $\vec{E} \times \vec{B}$ points along the velocity vector.

## Step-by-Step Solution

### Direction of Propagation

The argument is $(10^7 x - \omega t)$. The negative sign between the spatial and temporal terms means the wave propagates in the **$+x$-direction**.

### Wavelength $\lambda$

Extract the wave number $k = 10^7 \text{ m}^{-1}$.

$$
\lambda = \frac{2\pi}{k} = \frac{2\pi}{10^7} \approx 6.28 \times 10^{-7} \text{ m}
$$

### Angular Frequency $\omega$

Use the speed of light $c \approx 3 \times 10^8 \text{ m/s}$:

$$
\omega = c k = (3 \times 10^8)(10^7) = 3 \times 10^{15} \text{ rad/s}
$$

### Magnetic Field Equation

Calculate the amplitude $B_0$:

$$
B_0 = \frac{E_0}{c} = \frac{100}{3 \times 10^8} \approx 3.33 \times 10^{-7} \text{ T}
$$

The electric field oscillates in the $y$-direction ($\hat{j}$), and propagation is in the $x$-direction ($\hat{i}$). The cross product $\hat{j} \times \hat{k} = \hat{i}$ dictates that the magnetic field must oscillate in the $+z$-direction.

$$
B_z(x,t) = 3.33 \times 10^{-7} \sin(10^7 x - 3 \times 10^{15} t) \text{ T}
$$

## Final Result

* Propagation: Positive $x$-direction
* Wavelength: $\lambda \approx 628 \text{ nm}$
* Angular frequency: $\omega = 3 \times 10^{15} \text{ rad/s}$
* Magnetic field: $B_z(x,t) = 3.33 \times 10^{-7} \sin(10^7 x - \omega t) \text{ T}$

## Interpretation

This wave sits in the visible light spectrum (red/orange). The mutually orthogonal relationship between the electric field, magnetic field, and the direction of travel strictly governs the geometry of all electromagnetic radiation.
