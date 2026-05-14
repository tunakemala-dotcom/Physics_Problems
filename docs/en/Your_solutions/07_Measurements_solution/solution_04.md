# Task 04 – Relative Uncertainty

## Problem Statement

A car's speedometer has a $5\%$ uncertainty. If it reads $60\text{ km/h}$, what is the range of the car's actual speed?

## Theory

Percentage uncertainty represents the relative error multiplied by $100$. The absolute uncertainty is found by taking that percentage of the nominal measured value.

$$
\Delta v = v \times \left( \frac{\% \text{ uncertainty}}{100} \right)
$$

The range is defined as $[v - \Delta v, v + \Delta v]$.

## Step-by-Step Solution

Calculate the absolute uncertainty:

$$
\Delta v = 60 \times 0.05 = 3\text{ km/h}
$$

Determine the lower bound of the range:

$$
v_{min} = 60 - 3 = 57\text{ km/h}
$$

Determine the upper bound of the range:

$$
v_{max} = 60 + 3 = 63\text{ km/h}
$$

## Final Result

The range of the car's actual speed is $57\text{ km/h}$ to $63\text{ km/h}$.

## Interpretation

A $5\%$ error margin means the true speed could deviate by up to $3\text{ km/h}$ in either direction from the indicated value at this specific speed. The absolute error will grow larger at higher speeds.
