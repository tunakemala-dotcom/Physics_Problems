# Section 0: Mathematical Foundations – Solutions

## Task 1 – Vector Algebra

### Problem Statement

Given two vectors in 3D space: $\vec{a} = [2, 1, -3]$ and $\vec{b} = [4, -2, 1]$. Calculate the magnitude of each, their dot product, cross product, and the angle between them.

### Theory

The magnitude of a vector is the square root of the sum of its squared components. The dot product represents the projection of one vector onto another. The cross product yields a vector orthogonal to both. The angle $\theta$ can be found using the dot product relation.

### Step-by-Step Solution

Magnitudes:

$$
|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2} = \sqrt{4 + 1 + 9} = \sqrt{14}
$$

$$
|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2} = \sqrt{16 + 4 + 1} = \sqrt{21}
$$

Dot Product:

$$
\vec{a} \cdot \vec{b} = (2)(4) + (1)(-2) + (-3)(1) = 8 - 2 - 3 = 3
$$

Cross Product:

$$
\vec{a} \times \vec{b} = \begin{pmatrix} (1)(1) - (-3)(-2) \\ (-3)(4) - (2)(1) \\ (2)(-2) - (1)(4) \end{pmatrix} = \begin{pmatrix} -5 \\ -14 \\ -8 \end{pmatrix}
$$

Angle:

$$
\cos(\theta) = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|} = \frac{3}{\sqrt{14}\sqrt{21}} = \frac{3}{7\sqrt{6}} = \frac{\sqrt{6}}{14}
$$

### Final Result

- Magnitudes: $|\vec{a}| = \sqrt{14}$, $|\vec{b}| = \sqrt{21}$
- Dot product: $3$
- Cross product: $[-5, -14, -8]$
- Angle: $\theta = \arccos(\frac{\sqrt{6}}{14})$

### Interpretation

The positive dot product indicates the angle between the vectors is acute. The cross product vector is perpendicular to the plane formed by $\vec{a}$ and $\vec{b}$.

---

## Task 2 – Systems of Equations

### Problem Statement

Find the values of $x$ and $y$ that satisfy $2x + 3y = 12$ and $x - y = 1$.

### Theory

A system of linear equations can be solved using substitution or elimination to find the intersection point of the two lines.

### Step-by-Step Solution

From the second equation, isolate $x$:

$$
x = y + 1
$$

Substitute this into the first equation:

$$
\begin{align}
2(y + 1) + 3y &= 12 \\
2y + 2 + 3y &= 12 \\
5y &= 10 \\
y &= 2
\end{align}
$$

Substitute $y$ back to find $x$:

$$
x = 2 + 1 = 3
$$

### Final Result

$x = 3$, $y = 2$

### Interpretation

The unique solution represents the coordinate point $(3, 2)$ where the two lines intersect in the Cartesian plane.

---

## Task 3 – Proportionality

### Problem Statement

Determine the factor by which the gravitational force $F = G \frac{m_1 m_2}{r^2}$ changes if $r$ is doubled and both masses are halved.

### Theory

Gravitational force is directly proportional to the product of the masses and inversely proportional to the square of the distance between them.

### Step-by-Step Solution

Let the new variables be $r' = 2r$, $m_1' = \frac{m_1}{2}$, and $m_2' = \frac{m_2}{2}$. Substitute these into the force equation to find the new force $F'$:

$$
\begin{align}
F' &= G \frac{m_1' m_2'}{(r')^2} \\
   &= G \frac{(\frac{m_1}{2})(\frac{m_2}{2})}{(2r)^2} \\
   &= G \frac{\frac{m_1 m_2}{4}}{4r^2} \\
   &= \frac{1}{16} \left( G \frac{m_1 m_2}{r^2} \right)
\end{align}
$$

### Final Result

The force changes by a factor of $\frac{1}{16}$.

### Interpretation

Increasing the distance and decreasing the masses both act to reduce the gravitational force. The squared inverse relationship with distance heavily dominates the reduction.

---

## Task 4 – Rearranging Formulas

### Problem Statement

Rearrange the pendulum period formula $T = 2\pi \sqrt{\frac{L}{g}}$ to solve for $g$.

### Theory

Algebraic isolation requires performing inverse operations: squaring both sides to remove the radical, and cross-multiplying to isolate the variable in the denominator.

### Step-by-Step Solution

Square both sides:

$$
T^2 = 4\pi^2 \frac{L}{g}
$$

Multiply by $g$:

$$
g T^2 = 4\pi^2 L
$$

Divide by $T^2$:

$$
g = \frac{4\pi^2 L}{T^2}
$$

### Final Result

$g = \frac{4\pi^2 L}{T^2}$

### Interpretation

This rearranged formula allows experimental determination of the acceleration due to gravity by measuring the length and oscillation period of a simple pendulum.

---

## Task 5 – Trigonometry

### Problem Statement

A vector $\vec{A}$ has a magnitude of $15$ and makes an angle of $60^\circ$ with the horizontal axis. Calculate its components.

### Theory

A vector in 2D space can be decomposed into orthogonal scalar components using sine and cosine functions.

### Step-by-Step Solution

The horizontal component $A_x$ is:

$$
A_x = 15 \cos(60^\circ) = 15(0.5) = 7.5
$$

The vertical component $A_y$ is:

$$
A_y = 15 \sin(60^\circ) = 15\left(\frac{\sqrt{3}}{2}\right) = 7.5\sqrt{3}
$$

### Final Result

- Horizontal component: $7.5$
- Vertical component: $7.5\sqrt{3}$

### Interpretation

These components represent the projection of the vector along the x and y coordinate axes.

---

## Task 6 – Function Analysis

### Problem Statement

Identify any local maxima or minima for the function $f(x) = 3x^2 - 12x + 7$.

### Theory

Local extrema occur where the first derivative is zero. The second derivative test determines whether the extremum is a minimum (positive second derivative) or a maximum (negative).

### Step-by-Step Solution

Find the first derivative:

$$
f'(x) = 6x - 12
$$

Set to zero to find critical points:

$$
6x - 12 = 0 \implies x = 2
$$

Find the second derivative:

$$
f''(x) = 6
$$

Since $f''(2) > 0$, the point is a local minimum. Calculate the function value:

$$
f(2) = 3(2)^2 - 12(2) + 7 = 12 - 24 + 7 = -5
$$

### Final Result

Local minimum at $(2, -5)$.

### Interpretation

The function represents an upward-opening parabola, meaning it has a single global minimum at its vertex and no maxima.

---

## Task 7 – Logic & Series

### Problem Statement

A bicycle at $10\text{ m}$ moves towards a wall at $1\text{ m/s}$. A fly flies continuously between the bicycle and the wall at $2\text{ m/s}$. What is the total distance the fly travels?

### Theory

Instead of summing an infinite geometric series of the fly's back-and-forth trips, the problem can be simplified by determining the total time of the event.

### Step-by-Step Solution

Calculate the time it takes for the bicycle to reach the wall:

$$
t = \frac{d}{v_{\text{bike}}} = \frac{10}{1} = 10\text{ s}
$$

The fly is in motion for exactly this amount of time at a constant speed:

$$
d_{\text{fly}} = v_{\text{fly}} \times t = 2 \times 10 = 20\text{ m}
$$

### Final Result

Total distance is $20\text{ m}$.

### Interpretation

By shifting perspective from spatial segments to total elapsed time, an otherwise complex infinite series problem becomes a simple kinematic calculation.

---

## Task 8 – Definite Integrals

### Problem Statement

Calculate the area under the curve of $f(x) = \sin(x)$ from $x = 0$ to $x = \pi$.

### Theory

The definite integral of a function provides the net signed area bounded by the curve and the x-axis over a specified interval.

### Step-by-Step Solution

Set up the integral:

$$
A = \int_0^\pi \sin(x) \, dx
$$

Evaluate the antiderivative:

$$
\begin{align}
A &= [-\cos(x)]_0^\pi \\
  &= (-\cos(\pi)) - (-\cos(0)) \\
  &= (-(-1)) - (-1) \\
  &= 1 + 1 \\
  &= 2
\end{align}
$$

### Final Result

Area = $2$

### Interpretation

The positive area corresponds to the entire first half-period of the sine wave, which lies completely above the x-axis.

---

## Task 9 – Optimization Problem

### Problem Statement

Find the dimensions of the rectangle with the maximum area in the first quadrant bounded by $y = 3 - x^2$.

### Theory

Optimization requires formulating an objective function (area) in terms of a single variable, finding its critical points via differentiation, and verifying the maximum.

### Step-by-Step Solution

Let the rectangle's width be $x$ and height be $y$. Since it lies under the curve, $y = 3 - x^2$. The area $A$ is:

$$
A(x) = x(3 - x^2) = 3x - x^3
$$

Differentiate with respect to $x$:

$$
A'(x) = 3 - 3x^2
$$

Set to zero to find the maximum:

$$
3 - 3x^2 = 0 \implies x^2 = 1 \implies x = 1
$$

Calculate the corresponding height:

$$
y = 3 - (1)^2 = 2
$$

### Final Result

Width = $1$, Height = $2$

### Interpretation

These dimensions yield a maximum enclosed rectangular area of 2 square units under the parabolic boundary in the positive quadrant.

---

## Task 10 – Infinite Series

### Problem Statement

Determine the final position of an ant moving $1\text{ m}$ east, $1/2\text{ m}$ north, $1/3\text{ m}$ west, $1/4\text{ m}$ south, $1/5\text{ m}$ east, etc.

### Theory

The motion separates into two independent infinite alternating series for the x (East/West) and y (North/South) coordinates. These are known Taylor series expansions.

### Step-by-Step Solution

The x-coordinate is the sum of odd-denominator terms:

$$
X = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots = \sum_{n=0}^\infty \frac{(-1)^n}{2n+1}
$$

This is the Gregory-Leibniz series for arctangent:

$$
X = \arctan(1) = \frac{\pi}{4}
$$

The y-coordinate is the sum of even-denominator terms:

$$
Y = \frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \dots = \frac{1}{2} \left( 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots \right)
$$

The inner series is the alternating harmonic series:

$$
Y = \frac{1}{2}\ln(2)
$$

### Final Result

Final coordinate position: $(\frac{\pi}{4}, \frac{\ln(2)}{2})$

### Interpretation

The ant spirals inward toward a convergent coordinate point dictated by fundamental mathematical constants, demonstrating the geometric meaning of conditionally convergent series.
