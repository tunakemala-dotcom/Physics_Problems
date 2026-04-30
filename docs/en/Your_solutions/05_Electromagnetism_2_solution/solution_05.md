# Task 05 – Energy Stored by charge in a capacitor

## Problem Statement

We have a parallel-plate capacitor with $S = 0.02 \text{ m}^2$, $d = 5 \text{ mm}$, and voltage $U = 500 \text{ V}$. Calculate the capacitance $C$, the stored energy, the electric field intensity $E$, and the force of attraction $F$ between the plates.

## Theory

The core formulas governing an ideal parallel-plate capacitor in a vacuum/air are:

$$
C = \frac{\epsilon_0 S}{d}
$$

$$
\text{Energy} = \frac{1}{2} C V^2
$$

$$
E = \frac{V}{d}
$$

$$
F = \frac{1}{2} \epsilon_0 E^2 S
$$

*(Note: To avoid symbol confusion, the voltage $U=500\text{V}$ is denoted as $V$ in the derivations below).*

## Step-by-Step Solution

Given $S = 0.02 \text{ m}^2$, $d = 0.005 \text{ m}$, $V = 500 \text{ V}$, and $\epsilon_0 = 8.854 \times 10^{-12} \text{ F/m}$.

### Capacitance $C$

$$
C = \frac{8.854 \times 10^{-12} \times 0.02}{0.005} = \frac{1.7708 \times 10^{-13}}{0.005} = 3.5416 \times 10^{-11} \text{ F}
$$

### Stored Energy

$$
\text{Energy} = \frac{1}{2} C V^2 = \frac{1}{2} (3.5416 \times 10^{-11}) (500)^2
$$

$$
\text{Energy} = \frac{1}{2} (3.5416 \times 10^{-11}) (250000) \approx 4.427 \times 10^{-6} \text{ J}
$$

### Electric Field Intensity $E$

$$
E = \frac{V}{d} = \frac{500}{0.005} = 100,000 \text{ V/m}
$$

### Force of Attraction $F$

The plates attract each other due to opposite charges. 

$$
F = \frac{1}{2} (8.854 \times 10^{-12}) (100000)^2 (0.02)
$$

$$
F = (4.427 \times 10^{-12}) (10^{10}) (0.02)
$$

$$
F = 0.04427 \times 0.02 \approx 8.85 \times 10^{-4} \text{ N}
$$

## Final Result

* Capacitance: $C \approx 35.4 \text{ pF}$
* Stored energy: $4.43 \text{ }\mu\text{J}$
* Electric field: $E = 1.0 \times 10^5 \text{ V/m}$
* Attraction force: $F \approx 8.85 \times 10^{-4} \text{ N}$

## Interpretation

Despite a relatively high voltage of $500 \text{ V}$, the macroscopic separation ($5 \text{ mm}$) and small area result in a very low capacitance and minimal stored energy. The attractive force between the rigid plates is likewise extremely small.
