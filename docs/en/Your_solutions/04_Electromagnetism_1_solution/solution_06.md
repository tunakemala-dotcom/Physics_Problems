# Task 06 – Field at a point from a system of charges

## Problem Statement

Two point charges are given: $+q$ at $(-a, 0)$ and $+2q$ at $(a, 0)$.
1. Determine the field vector $\vec{E}(0, y)$, $\vec{E}(x, 0)$ and generally $\vec{E}(x, y)$.
2. Determine the condition for which $E_x = 0$, $E_y = 0$, and $\vec{E} = 0$.
3. Calculate the field for $a = 0.2\text{m}$, $y = 0.3\text{m}$, $q = 2\mu\text{C}$ on the y-axis.
4. Investigate the limit $y \gg a$.

## Theory

The electric field vector from a point charge $q_i$ at position vector $\vec{r}_i$ evaluated at observation point $\vec{r}$ is:

$$
\vec{E}_i(\vec{r}) = k q_i \frac{\vec{r} - \vec{r}_i}{|\vec{r} - \vec{r}_i|^3}
$$

Total field is the superposition $\vec{E} = \vec{E}_1 + \vec{E}_2$.

## Step-by-Step Solution

### 1. General and Axis Field Vectors

Let $\vec{r}_1 = (-a, 0)$ with charge $q$, and $\vec{r}_2 = (a, 0)$ with charge $2q$.

General field $\vec{E}(x,y)$:

$$
\vec{E}(x,y) = kq \frac{(x+a)\hat{i} + y\hat{j}}{((x+a)^2 + y^2)^{3/2}} + 2kq \frac{(x-a)\hat{i} + y\hat{j}}{((x-a)^2 + y^2)^{3/2}}
$$

Field on the y-axis $\vec{E}(0,y)$ by setting $x=0$:

$$
\vec{E}(0,y) = kq \frac{a\hat{i} + y\hat{j}}{(a^2 + y^2)^{3/2}} + 2kq \frac{-a\hat{i} + y\hat{j}}{(a^2 + y^2)^{3/2}} = \frac{kq}{(a^2+y^2)^{3/2}} (-a\hat{i} + 3y\hat{j})
$$

Field on the x-axis $\vec{E}(x,0)$ by setting $y=0$:

$$
\vec{E}(x,0) = \left[ kq \frac{x+a}{|x+a|^3} + 2kq \frac{x-a}{|x-a|^3} \right] \hat{i}
$$

### 2. Zero Field Conditions

* $E_y = 0$: Requires $y=0$. The electric field only has no vertical component on the x-axis.
* $E_x = 0$: On the y-axis, the x-components don't fully cancel (due to $2q$ vs $q$). On the x-axis, $E_x = 0$ implies $\vec{E} = 0$.
* $\vec{E} = 0$: Must occur on the x-axis between the charges ($-a < x < a$), where vectors oppose.

$$
k \frac{q}{(x+a)^2} = k \frac{2q}{(a-x)^2}
$$

$$
\frac{1}{x+a} = \frac{\sqrt{2}}{a-x}
$$

$$
a - x = \sqrt{2}x + \sqrt{2}a
$$

$$
x(1+\sqrt{2}) = a(1-\sqrt{2}) \implies x = a \frac{1-\sqrt{2}}{1+\sqrt{2}} = -a(3 - 2\sqrt{2}) \approx -0.17a
$$

### 3. Numerical Calculation

Evaluate $\vec{E}(0,y)$ for $a=0.2$, $y=0.3$, $q=2 \times 10^{-6}$:

Denominator: $(0.2^2 + 0.3^2)^{3/2} = (0.04 + 0.09)^{3/2} = (0.13)^{3/2} \approx 0.04687$

$$
\vec{E}(0,0.3) = \frac{(9\times 10^9)(2\times 10^{-6})}{0.04687} (-0.2\hat{i} + 3(0.3)\hat{j})
$$

$$
\vec{E}(0,0.3) \approx 383995 (-0.2\hat{i} + 0.9\hat{j}) = (-76.8\hat{i} + 345.6\hat{j}) \text{ kV/m}
$$

### 4. Limit $y \gg a$

If $y \gg a$, then $(a^2 + y^2)^{3/2} \approx y^3$.

Substitute into the $\vec{E}(0,y)$ equation:

$$
\vec{E}(0,y) \approx \frac{kq}{y^3} (-a\hat{i} + 3y\hat{j})
$$

As $y$ dominates, the $-a\hat{i}/y^3$ term vanishes faster than the $3y\hat{j}/y^3$ term.

$$
\vec{E}(0,y) \approx \frac{k(3q)}{y^2} \hat{j}
$$

## Final Result

1. Derived in step 1.
2. $\vec{E} = 0$ at $x = -a(3-2\sqrt{2})$.
3. $\vec{E}(0, 0.3) \approx -76.8 \text{ kV/m} \, \hat{i} + 345.6 \text{ kV/m} \, \hat{j}$.
4. In the far-field limit, $\vec{E} \approx \frac{k(3q)}{y^2} \hat{j}$ (acts as a point charge of $3q$).

## Interpretation

Close to the charges, the spatial separation matters, and the $+2q$ charge pushes the equilibrium point leftward. From far away, the distribution details blur, and the system behaves exactly like a single monopole carrying the total net charge $+3q$.
