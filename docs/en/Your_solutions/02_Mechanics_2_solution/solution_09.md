# Task 09 – Vertical throw with drag

## Problem Statement

Equation of motion: $m\frac{dv}{dt} = -mg - kv$, with initial conditions $v(0)=v_0$, $x(0)=10$.
Solve analytically, determine maximum height, compare with the no-drag case, and provide a numerical simulation script.

## Theory

The term $-kv$ represents linear air resistance (Stokes' drag), acting in opposition to velocity. We solve the first-order differential equation for velocity using separation of variables, then integrate velocity to find position.

## Step-by-Step Solution

### 1. Analytical Solution for Velocity

Isolate the variables $v$ and $t$:

$$
\frac{dv}{dt} = -g - \frac{k}{m}v = -\frac{k}{m} \left(v + \frac{mg}{k}\right)
$$

$$
\frac{dv}{v + \frac{mg}{k}} = -\frac{k}{m} dt
$$

Integrate both sides:

$$
\int_{v_0}^{v(t)} \frac{1}{u + \frac{mg}{k}} du = \int_0^t -\frac{k}{m} d\tau
$$

$$
\ln \left( \frac{v(t) + \frac{mg}{k}}{v_0 + \frac{mg}{k}} \right) = -\frac{k}{m} t
$$

Exponentiate and solve for $v(t)$:

$$
v(t) = \left(v_0 + \frac{mg}{k}\right) e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

### 2. Analytical Solution for Position

Integrate $v(t)$ to find $x(t)$:

$$
x(t) = \int \left[ \left(v_0 + \frac{mg}{k}\right) e^{-\frac{k}{m}t} - \frac{mg}{k} \right] dt
$$

$$
x(t) = -\frac{m}{k}\left(v_0 + \frac{mg}{k}\right) e^{-\frac{k}{m}t} - \frac{mg}{k}t + C
$$

Apply initial condition $x(0) = 10$:

$$
10 = -\frac{m}{k}\left(v_0 + \frac{mg}{k}\right) (1) - 0 + C
$$

$$
C = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)
$$

Substitute $C$ back into $x(t)$:

$$
x(t) = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right) \left(1 - e^{-\frac{k}{m}t}\right) - \frac{mg}{k}t
$$

### 3. Maximum Height

At maximum height, $v(t) = 0$:

$$
0 = \left(v_0 + \frac{mg}{k}\right) e^{-\frac{k}{m}t_{max}} - \frac{mg}{k}
$$

$$
e^{\frac{k}{m}t_{max}} = \frac{v_0 + \frac{mg}{k}}{\frac{mg}{k}} = 1 + \frac{kv_0}{mg}
$$

$$
t_{max} = \frac{m}{k} \ln \left( 1 + \frac{kv_0}{mg} \right)
$$

Substitute $t_{max}$ into the $x(t)$ equation. Noting that $e^{-\frac{k}{m}t_{max}} = \left(1 + \frac{kv_0}{mg}\right)^{-1}$:

$$
x_{max} = 10 + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right) \left( 1 - \frac{1}{1 + \frac{kv_0}{mg}} \right) - \frac{mg}{k} \frac{m}{k} \ln \left( 1 + \frac{kv_0}{mg} \right)
$$

Simplifies to:

$$
x_{max} = 10 + \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln \left( 1 + \frac{k v_0}{mg} \right)
$$

### 4. Comparison without Drag

Without drag ($k \to 0$), the kinematic formula yields:

$$
x_{max, \text{no drag}} = 10 + \frac{v_0^2}{2g}
$$

Because air resistance constantly removes mechanical energy from the system, $x_{max} < x_{max, \text{no drag}}$.

### 5. Python Numerical Simulation

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import odeint

def model(state, t, m, k, g):
    x, v = state
    dxdt = v
    dvdt = -g - (k/m)*v
    return [dxdt, dvdt]

m, k, g = 1.0, 0.5, 9.81
v0 = 20.0
state0 = [10.0, v0]
t = np.linspace(0, 4, 100)

solution = odeint(model, state0, t, args=(m, k, g))
x_num = solution[:, 0]

plt.plot(t, x_num, label='With Drag')
plt.plot(t, 10 + v0*t - 0.5*g*t**2, '--', label='Without Drag')
plt.xlabel('Time (s)')
plt.ylabel('Height (m)')
plt.title('Vertical Throw with Drag')
plt.legend()
plt.grid()
plt.show()
