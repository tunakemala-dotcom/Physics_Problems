# Task 10 – Kinematics

## Problem Statement

Point M moves according to the equation $\vec{r}(t) = (a \cos(\omega t), b \sin(\omega t), bt)$, where $a, b, \omega$ are positive constants.
Find the equation of the point's trajectory, compute the path length from $t=0$ to $t=t_0$, and provide Python code to draw the trajectory. 

## Theory

The trajectory equation in space is found by establishing relationships between the coordinates $(x,y,z)$. 
The path length $S$ is the integral of the speed:

$$
S = \int_0^{t_0} |\vec{v}(t)| dt = \int_0^{t_0} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 + \left(\frac{dz}{dt}\right)^2} dt
$$

## Step-by-Step Solution

### a) Equation of Trajectory

The coordinates are:

$$
\begin{align}
x &= a \cos(\omega t) \\
y &= b \sin(\omega t) \\
z &= bt
\end{align}
$$

Using the identity $\cos^2(\theta) + \sin^2(\theta) = 1$:

$$
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 = \cos^2(\omega t) + \sin^2(\omega t) = 1
$$

This represents an elliptical cylinder. The motion is bounded to the surface of this cylinder while progressing linearly in the $z$-direction over time. The trajectory is an elliptical helix.

### b) Path Length

Find the velocity components by differentiating $\vec{r}(t)$:

$$
\vec{v}(t) = (-a\omega \sin(\omega t), b\omega \cos(\omega t), b)
$$

Calculate the speed:

$$
|\vec{v}(t)| = \sqrt{(-a\omega \sin(\omega t))^2 + (b\omega \cos(\omega t))^2 + b^2}
$$

$$
|\vec{v}(t)| = \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2}
$$

The path length integral is:

$$
S = \int_0^{t_0} \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2} dt
$$

If $a = b$ (circular helix), the integral simplifies to $S = t_0 \sqrt{a^2\omega^2 + b^2}$. For arbitrary $a \neq b$, this yields an incomplete elliptic integral of the second kind.

### c) Python Code for Trajectory

The following script uses `matplotlib` to plot the 3D trajectory.

```python
import numpy as np
import matplotlib.pyplot as plt

def plot_trajectory(a, b, omega, t_max):
    t = np.linspace(0, t_max, 500)
    x = a * np.cos(omega * t)
    y = b * np.sin(omega * t)
    z = b * t

    fig = plt.figure(figsize=(8, 8))
    ax = fig.add_subplot(111, projection='3d')
    ax.plot(x, y, z, label='Trajectory', color='blue')
    
    ax.set_xlabel('X')
    ax.set_ylabel('Y')
    ax.set_zlabel('Z')
    ax.set_title('Elliptical Helix')
    plt.legend()
    plt.show()

# Example usage:
plot_trajectory(a=3, b=2, omega=1, t_max=15)
