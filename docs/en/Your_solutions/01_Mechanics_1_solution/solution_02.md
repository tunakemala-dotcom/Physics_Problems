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
FILE: task_03.md

Markdown
# Task 03 – Path Intersection

## Problem Statement

Alice is moving along a path described by $A(t) = (2+t, 8-3t)$ and Bob is moving along a path $B(t) = (2t-1, 2t+2)$. Determine if their paths intersect. If yes, determine when and where they will collide. If not, determine the minimum distance between them and when it occurs.

## Theory

Path intersection means the objects visit the same spatial coordinates, though potentially at different times $t_A$ and $t_B$. 

Collision means the objects visit the same spatial coordinates at the exact same time $t$. 

The distance between two points at time $t$ is calculated using the Euclidean distance formula:

$$
D(t) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2}
$$

## Step-by-Step Solution

### Checking for Collision

Set $A(t) = B(t)$ for the same time $t$:

$$
2 + t = 2t - 1 \implies t = 3
$$

Check the y-coordinates at $t = 3$:

$$
y_A(3) = 8 - 3(3) = -1
$$

$$
y_B(3) = 2(3) + 2 = 8
$$

Since $-1 \neq 8$, they do not collide.

### Checking for Path Intersection

Set the coordinates equal using different time variables, $t_A$ and $t_B$:

$$
\begin{align}
2 + t_A &= 2t_B - 1 \\
8 - 3t_A &= 2t_B + 2
\end{align}
$$

From the first equation, express $t_A$:

$$
t_A = 2t_B - 3
$$

Substitute into the second equation:

$$
8 - 3(2t_B - 3) = 2t_B + 2
$$

$$
8 - 6t_B + 9 = 2t_B + 2
$$

$$
17 - 6t_B = 2t_B + 2
$$

$$
15 = 8t_B \implies t_B = \frac{15}{8}
$$

Find $t_A$:

$$
t_A = 2\left(\frac{15}{8}\right) - 3 = \frac{15}{4} - \frac{12}{4} = \frac{3}{4}
$$

The paths intersect at the point:

$$
B(15/8) = \left(2\left(\frac{15}{8}\right) - 1, 2\left(\frac{15}{8}\right) + 2\right) = \left(\frac{11}{4}, \frac{23}{4}\right)
$$

### Minimum Distance

Define the squared distance function $f(t) = D(t)^2$:

$$
f(t) = (2t - 1 - (2 + t))^2 + (2t + 2 - (8 - 3t))^2
$$

$$
f(t) = (t - 3)^2 + (5t - 6)^2
$$

Expand the terms:

$$
f(t) = (t^2 - 6t + 9) + (25t^2 - 60t + 36)
$$

$$
f(t) = 26t^2 - 66t + 45
$$

To find the minimum, set the derivative to zero:

$$
f'(t) = 52t - 66 = 0
$$

$$
t = \frac{66}{52} = \frac{33}{26}
$$

Calculate the minimum distance $D(33/26)$:

$$
D_{min} = \sqrt{26\left(\frac{33}{26}\right)^2 - 66\left(\frac{33}{26}\right) + 45} = \sqrt{\frac{1089}{26} - \frac{2178}{26} + \frac{1170}{26}} = \sqrt{\frac{81}{26}} \approx 1.76
$$

## Final Result

* Collision: No.
* Intersection: Yes, at point $(11/4, 23/4)$.
* Minimum distance: $\sqrt{81/26} \approx 1.76$ units at time $t = 33/26 \approx 1.27 \text{ s}$.

## Interpretation

Even though their geometric paths cross, the two moving bodies arrive at the intersectio
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
