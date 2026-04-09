# Task 08 – Waves

## Problem Statement

Which of the following functions can describe a traveling wave? Check if they satisfy the wave equation:

$$
\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}
$$

a) $y(x,t) = A \cos(kx^2 - \omega t)$
b) $y(x,t) = A(x-vt)^2$
c) $y(x,t) = A \log(x+vt)$

## Theory

Any function of the form $f(x \pm vt)$ is a solution to the linear 1D wave equation and represents a traveling wave of fixed shape. We must compute the second partial derivatives with respect to $x$ and $t$ to verify.

## Step-by-Step Solution

### Case a) $y(x,t) = A \cos(kx^2 - \omega t)$

First partials:

$$
\frac{\partial y}{\partial x} = -A \sin(kx^2 - \omega t) \cdot (2kx)
$$

$$
\frac{\partial y}{\partial t} = -A \sin(kx^2 - \omega t) \cdot (-\omega) = A\omega \sin(kx^2 - \omega t)
$$

Second partials:

$$
\frac{\partial^2 y}{\partial x^2} = -2Ak \sin(kx^2 - \omega t) - 4Ak^2x^2 \cos(kx^2 - \omega t)
$$

$$
\frac{\partial^2 y}{\partial t^2} = -A\omega^2 \cos(kx^2 - \omega t)
$$

The spatial derivative $\frac{\partial^2 y}{\partial x^2}$ contains both sine and cosine terms with non-constant coefficients ($x^2$), while the temporal derivative only contains a cosine term. They cannot be proportional by a constant factor $1/v^2$. 
**Conclusion: Not a traveling wave.**

### Case b) $y(x,t) = A(x-vt)^2$

First partials:

$$
\frac{\partial y}{\partial x} = 2A(x-vt)
$$

$$
\frac{\partial y}{\partial t} = 2A(x-vt)(-v) = -2Av(x-vt)
$$

Second partials:

$$
\frac{\partial^2 y}{\partial x^2} = 2A
$$

$$
\frac{\partial^2 y}{\partial t^2} = -2Av(-v) = 2Av^2
$$

Substitute into the wave equation:

$$
2A = \frac{1}{v^2} (2Av^2) \implies 2A = 2A
$$

**Conclusion: Valid traveling wave.**

### Case c) $y(x,t) = A \log(x+vt)$

First partials:

$$
\frac{\partial y}{\partial x} = \frac{A}{x+vt}
$$

$$
\frac{\partial y}{\partial t} = \frac{Av}{x+vt}
$$

Second partials:

$$
\frac{\partial^2 y}{\partial x^2} = -\frac{A}{(x+vt)^2}
$$

$$
\frac{\partial^2 y}{\partial t^2} = -\frac{Av^2}{(x+vt)^2}
$$

Substitute into the wave equation:

$$
-\frac{A}{(x+vt)^2} = \frac{1}{v^2} \left(-\frac{Av^2}{(x+vt)^2}\right) \implies -\frac{A}{(x+vt)^2} = -\frac{A}{(x+vt)^2}
$$

**Conclusion: Valid traveling wave.**

## Final Result

* Function (a) does **not** describe a traveling wave.
* Function (b) describes a traveling wave.
* Function (c) describes a traveling wave.

## Interpretation

Functions (b) and (c) retain the rigid $u = x \pm vt$ structure, ensuring the spatial profile translates linearly over time without distortion. Function (a) fails because the spatial mapping ($x^2$) causes the wave profile to distort and change shape as time progresses.
