# Task 02 – Propagation of Error II

## Problem Statement

The length and width of a rectangular plate are measured to be $L = (15.3 \pm 0.1)\text{ cm}$ and $W = (8.4 \pm 0.1)\text{ cm}$. Calculate the area of the plate and its uncertainty.

## Theory

The area of a rectangle is $A = L \times W$. 
For a product of independent measured quantities, the relative uncertainties add in quadrature (for uncorrelated random errors) or linearly (for maximum possible error/worst-case scenario). The worst-case relative error is:

$$
\frac{\Delta A}{A} = \frac{\Delta L}{L} + \frac{\Delta W}{W}
$$

Standard independent error propagation (in quadrature) is:

$$
\frac{\Delta A}{A} = \sqrt{ \left(\frac{\Delta L}{L}\right)^2 + \left(\frac{\Delta W}{W}\right)^2 }
$$

We will use the worst-case linear method here as it is standard in introductory treatments unless specified otherwise.

## Step-by-Step Solution

Calculate the nominal area:

$$
A = 15.3 \times 8.4 = 128.52 \text{ cm}^2
$$

Calculate the relative uncertainties:

$$
\frac{\Delta L}{L} = \frac{0.1}{15.3} \approx 0.00654
$$

$$
\frac{\Delta W}{W} = \frac{0.1}{8.4} \approx 0.01190
$$

Calculate the total relative uncertainty (linear addition):

$$
\frac{\Delta A}{A} = 0.00654 + 0.01190 = 0.01844
$$

Calculate the absolute uncertainty:

$$
\Delta A = 128.52 \times 0.01844 \approx 2.37 \text{ cm}^2
$$

Rounding to one significant figure for uncertainty yields $\Delta A \approx 2 \text{ cm}^2$. The area should be rounded to the same decimal place.

## Final Result

The area of the plate is $A = (129 \pm 2)\text{ cm}^2$.

## Interpretation

Even though the absolute uncertainty is the same for both length and width ($0.1\text{ cm}$), the width contributes almost twice as much to the relative error of the area because its nominal value is smaller.
