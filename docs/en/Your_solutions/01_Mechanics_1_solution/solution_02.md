# Task 02 – Range Optimization

## Problem Statement

For projectile motion, show analytically that the maximum range for a given initial velocity $v_0$ is achieved at a launch angle of $45^\circ$.

## Theory

The horizontal range $R$ of a projectile fired over level ground with initial velocity $v_0$ at an angle $\theta$ is given by the function:

$$
R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}
$$

To find the angle that maximizes this range, the first derivative of $R$ with respect to $\theta$ must be evaluated and set to zero.

## Step-by-Step Solution

Differentiate the range function with respect to the launch angle $\theta$:

$$
\frac{dR}{d\theta} = \frac{d}{d\theta} \left( \frac{v_0^2 \sin(2\theta)}{g} \right)
$$

Since $v_0$ and $g$ are constants, they factor out of the derivative:

$$
\frac{dR}{d\theta} = \frac{v_0^2}{g} \frac{d}{d\theta} (\sin(2\theta))
$$

Apply the chain rule:

$$
\frac{dR}{d\theta} = \frac{v_0^2}{g} (2 \cos(2\theta))
$$

To find the critical points, set the derivative equal to zero:

$$
\frac{2v_0^2}{g} \cos(2\theta) = 0
$$

Because $2v_0^2 / g \neq 0$, the equation simplifies to:

$$
\cos(2\theta) = 0
$$

Within the physically meaningful domain of launch angles $[0^\circ, 90^\circ]$, the cosine function is zero when its argument is $90^\circ$ (or $\pi/2$ radians):

$$
2\theta = 90^\circ
$$

$$
\theta = 45^\circ
$$

To confirm this is a maximum, check the second derivative:

$$
\frac{d^2R}{d\theta^2} = \frac{v_0^2}{g} (-4 \sin(2\theta))
$$

Evaluating at $\theta = 45^\circ$:

$$
\frac{d^2R}{d\theta^2} \bigg|_{\theta=45^\circ} = \frac{-4v_0^2}{g} \sin(90^\circ) = \frac{-4v_0^2}{g} < 0
$$

## Final Result

The maximum range is achieved at $\theta = 45^\circ$.

## Interpretation

The negative second derivative confirms that $\theta = 45^\circ$ yields a local maximum. This angle provides the optimal balance between keeping the projectile in the air long enough (which requires a large vertical velocity component) and having it travel forward fast enough (which requires a large horizontal velocity component).
