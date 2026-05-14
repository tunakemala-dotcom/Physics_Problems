# Task 03 – Propagation of Error III

## Problem Statement

The resistance $R$ is calculated using Ohm's Law, $R = V/I$. If the voltage is measured as $V = (10.0 \pm 0.2)\text{ V}$ and the current as $I = (2.00 \pm 0.05)\text{ A}$, what is the calculated resistance and its uncertainty?

## Theory

For a quotient of two measured variables ($R = V/I$), the relative uncertainty of the result is the sum of the relative uncertainties of the numerator and the denominator (worst-case error).

$$
\frac{\Delta R}{R} = \frac{\Delta V}{V} + \frac{\Delta I}{I}
$$

## Step-by-Step Solution

Calculate the nominal resistance:

$$
R = \frac{10.0}{2.00} = 5.00 \ \Omega
$$

Calculate the relative uncertainties:

$$
\frac{\Delta V}{V} = \frac{0.2}{10.0} = 0.02
$$

$$
\frac{\Delta I}{I} = \frac{0.05}{2.00} = 0.025
$$

Sum the relative uncertainties:

$$
\frac{\Delta R}{R} = 0.02 + 0.025 = 0.045
$$

Calculate the absolute uncertainty:

$$
\Delta R = R \times 0.045 = 5.00 \times 0.045 = 0.225 \ \Omega
$$

Rounding to one significant figure for the uncertainty yields $\Delta R \approx 0.2 \ \Omega$.

## Final Result

The calculated resistance is $R = (5.0 \pm 0.2)\ \Omega$.

## Interpretation

The fractional error in the current ($2.5\%$) is slightly larger than the fractional error in the voltage ($2.0\%$). Combined, they yield a maximum percentage uncertainty of $4.5\%$ for the resistance.
