# Task 01 – Propagation of Error I

## Problem Statement

The radius of a sphere is measured to be $r = (6.20 \pm 0.05)\text{ cm}$. Calculate the volume of the sphere and its associated uncertainty.

## Theory

The volume of a sphere is given by:

$$
V = \frac{4}{3} \pi r^3
$$

For a function of a single variable $V(r)$, the absolute uncertainty $\Delta V$ is calculated using the derivative method (error propagation):

$$
\Delta V = \left| \frac{dV}{dr} \right| \Delta r
$$

Alternatively, using relative uncertainties for a power law $V \propto r^3$, the relative uncertainty is multiplied by the exponent:

$$
\frac{\Delta V}{V} = 3 \frac{\Delta r}{r}
$$

## Step-by-Step Solution

Calculate the nominal volume using the measured radius $r = 6.20 \text{ cm}$:

$$
V = \frac{4}{3} \pi (6.20)^3 \approx \frac{4}{3} \pi (238.328) \approx 998.3 \text{ cm}^3
$$

Calculate the relative uncertainty in the radius:

$$
\frac{\Delta r}{r} = \frac{0.05}{6.20} \approx 0.00806
$$

Calculate the absolute uncertainty in the volume:

$$
\Delta V = 3 \left( \frac{\Delta r}{r} \right) V
$$

$$
\Delta V = 3 (0.00806) (998.3) \approx 24.1 \text{ cm}^3
$$

Round the uncertainty to one significant figure (standard practice for simple error analysis), which is $20 \text{ cm}^3$, or keep two for intermediate precision. Let us state it as $24 \text{ cm}^3$ and round the volume to match the decimal place. 

## Final Result

The volume of the sphere is $V = (998 \pm 24)\text{ cm}^3$.

## Interpretation

The cubic relationship significantly magnifies the relative error. A small $0.8\%$ uncertainty in the radius measurement translates into a nearly $2.4\%$ uncertainty in the final calculated volume.
