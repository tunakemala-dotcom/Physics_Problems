# Task 09 – Vector Lorentz Force

## Problem Statement

A proton moves with a velocity $\vec{v} = (2\hat{i} - 4\hat{j} + \hat{k}) \text{ m/s}$ in a region where the magnetic field is $\vec{B} = (\hat{i} + 2\hat{j} - \hat{k}) \text{ T}$. What is the magnitude of the magnetic force this charge experiences?

## Theory

The magnetic force vector is found via the cross product:

$$
\vec{F} = q(\vec{v} \times \vec{B})
$$

The cross product can be computed algebraically or using the matrix determinant method:

$$
\vec{v} \times \vec{B} =
\det
\begin{pmatrix}
\hat{i} & \hat{j} & \hat{k} \\
v_x & v_y & v_z \\
B_x & B_y & B_z
\end{pmatrix}
$$

## Step-by-Step Solution

### Step 1: Calculate the Cross Product

Set up the determinant with the given vectors $\vec{v} = (2, -4, 1)$ and $\vec{B} = (1, 2, -1)$:

$$
\vec{v} \times \vec{B} =
\det
\begin{pmatrix}
\hat{i} & \hat{j} & \hat{k} \\
2 & -4 & 1 \\
1 & 2 & -1
\end{pmatrix}
$$

Expand along the first row:

$$
\vec{v} \times \vec{B} = \hat{i} [(-4)(-1) - (1)(2)] - \hat{j} [(2)(-1) - (1)(1)] + \hat{k} [(2)(2) - (-4)(1)]
$$

$$
\vec{v} \times \vec{B} = \hat{i} (4 - 2) - \hat{j} (-2 - 1) + \hat{k} (4 + 4)
$$

$$
\vec{v} \times \vec{B} = 2\hat{i} + 3\hat{j} + 8\hat{k}
$$

### Step 2: Calculate Force Magnitude

The magnitude of the cross product vector is:

$$
|\vec{v} \times \vec{B}| = \sqrt{2^2 + 3^2 + 8^2} = \sqrt{4 + 9 + 64} = \sqrt{77} \approx 8.775 \text{ m}\cdot\text{T/s}
$$

Multiply by the charge of a proton ($q = e = 1.60 \times 10^{-19} \text{ C}$):

$$
|\vec{F}| = q |\vec{v} \times \vec{B}| = (1.60 \times 10^{-19}) (\sqrt{77})
$$

$$
|\vec{F}| \approx (1.60 \times 10^{-19}) (8.775) \approx 1.40 \times 10^{-18} \text{ N}
$$

## Final Result

The magnitude of the magnetic force on the proton is approximately $1.40 \times 10^{-18} \text{ N}$.

## Interpretation

The resulting force vector $(2\hat{i} + 3\hat{j} + 8\hat{k})$ is strictly orthogonal to both the original velocity vector and the magnetic field vector, ensuring that the magnetic field does no work and only alters the trajectory's direction.
