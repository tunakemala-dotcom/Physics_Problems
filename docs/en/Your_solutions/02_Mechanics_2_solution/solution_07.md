# Task 07 – Dynamics with Friction

## Problem Statement

A 5 kg block is placed on a 10 kg block. A horizontal force of 45 N is applied to the 10 kg block, and the 5 kg block is tied to the wall. The coefficient of kinetic friction between all moving surfaces is 0.2. Find the acceleration of the 10 kg block.

## Theory

We must analyze the forces acting on the 10 kg block. It experiences friction from two distinct surfaces:
1. The top surface, dragging against the stationary 5 kg block.
2. The bottom surface, dragging against the floor.

Kinetic friction is calculated as:

$$
f_k = \mu_k N
$$

Newton's Second Law for the 10 kg block in the horizontal direction:

$$
\sum F_x = F_{applied} - f_{top} - f_{bottom} = m_2 a
$$

## Step-by-Step Solution

### Step 1: Identify Normal Forces

Let $m_1 = 5 \text{ kg}$ and $m_2 = 10 \text{ kg}$.

The normal force between the 5 kg block and the 10 kg block balances the weight of the 5 kg block:

$$
N_1 = m_1 g = 5(9.81) = 49.05 \text{ N}
$$

The normal force between the 10 kg block and the floor balances the combined weight of both blocks:

$$
N_2 = (m_1 + m_2)g = 15(9.81) = 147.15 \text{ N}
$$

### Step 2: Calculate Friction Forces

Friction from the 5 kg block on the top surface of the 10 kg block:

$$
f_1 = \mu_k N_1 = 0.2(49.05) = 9.81 \text{ N}
$$

Friction from the floor on the bottom surface of the 10 kg block:

$$
f_2 = \mu_k N_2 = 0.2(147.15) = 29.43 \text{ N}
$$

### Step 3: Determine Acceleration

Apply Newton's Second Law to the 10 kg block. The applied force is $F = 45 \text{ N}$. Both friction forces oppose the motion.

$$
F - f_1 - f_2 = m_2 a
$$

$$
45 - 9.81 - 29.43 = 10 a
$$

$$
5.76 = 10 a
$$

$$
a = 0.576 \text{ m/s}^2
$$

## Final Result

The acceleration of the 10 kg block is $0.576 \text{ m/s}^2$.

## Interpretation

The 10 kg block is effectively sandwiched between two frictional boundaries. The stationary top block acts as a constant drag force in addition to the floor's friction. Because the net force (5.76 N) is positive, the 45 N applied force is sufficient to overcome static friction and accelerate the mass.
