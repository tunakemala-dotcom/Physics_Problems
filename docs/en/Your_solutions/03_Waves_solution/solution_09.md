# Task 09 – Damped Oscillator

## Problem Statement

For the equation $m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0$, provide the general solution, classification of damping states, and an interactive HTML animation solving it via RK4.

## Theory

This is a second-order linear homogeneous differential equation. The roots of the characteristic equation dictate the physical behavior of the oscillator, dependent on the damping ratio $\zeta = \frac{b}{2\sqrt{mk}}$ or damping coefficient $\gamma = \frac{b}{m}$ relative to the natural frequency $\omega_0^2 = \frac{k}{m}$.

## Step-by-Step Solution

### 1. General Solution & 2. Classification

Define $\gamma = \frac{b}{2m}$ and $\omega_0 = \sqrt{\frac{k}{m}}$. 

The characteristic roots are $r = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}$.

* **Underdamped ($b < 2\sqrt{mk}$):** Roots are complex. The system oscillates with decaying amplitude.
    $$
    x(t) = A e^{-\gamma t} \cos(\omega_d t + \phi), \quad \text{where } \omega_d = \sqrt{\omega_0^2 - \gamma^2}
    $$
* **Critically Damped ($b = 2\sqrt{mk}$):** Roots are real and repeated. System returns to equilibrium without oscillating in the shortest time.
    $$
    x(t) = (A + Bt) e^{-\gamma t}
    $$
* **Overdamped ($b > 2\sqrt{mk}$):** Roots are real and distinct. System returns to equilibrium slowly without oscillating.
    $$
    x(t) = A e^{r_1 t} + B e^{r_2 t}
    $$

### 3-6. Numerical Solution and Interactive Animation (HTML)

Save the following code as an `.html` file to view the simulation. It uses standard JavaScript Canvas to render the RK4 numerical integration.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Damped Oscillator</title>
    <style>
        body { font-family: sans-serif; display: flex; flex-direction: column; align-items: center; }
        canvas { border: 1px solid #ccc; margin: 10px; }
        .controls { padding: 10px; background: #f0f0f0; border-radius: 5px; }
    </style>
</head>
<body>

<div class="controls">
    <label>Damping b: <span id="b_val">1.0</span></label><br>
    <input type="range" id="b_slider" min="0" max="10" step="0.1" value="1.0" style="width:300px;">
    <p>State: <strong id="state_label">Underdamped</strong></p>
</div>

<canvas id="timeGraph" width="600" height="200"></canvas>
<canvas id="phaseGraph" width="300" height="300"></canvas>

<script>
    const m = 1.0, k = 10.0;
    const dt = 0.05;
    
    function solveRK4(b) {
        let x = 1.0, v = 0.0; // Initial conditions
        const history = [];
        for(let t = 0; t <= 15; t += dt) {
            history.push({t, x, v});
            const a = (x, v) => -(b/m)*v - (k/m)*x;
            
            let k1v = a(x, v), k1x = v;
            let k2v = a(x + 0.5*dt*k1x, v + 0.5*dt*k1v), k2x = v + 0.5*dt*k1v;
            let k3v = a(x + 0.5*dt*k2x, v + 0.5*dt*k2v), k3x = v + 0.5*dt*k2v;
            let k4v = a(x + dt*k3x, v + dt*k3v), k4x = v + dt*k3v;
            
            x += (dt/6) * (k1x + 2*k2x + 2*k3x + k4x);
            v += (dt/6) * (k1v + 2*k2v + 2*k3v + k4v);
        }
        return history;
    }

    function draw() {
        const b = parseFloat(document.getElementById('b_slider').value);
        document.getElementById('b_val').innerText = b;
        
        const crit = 2 * Math.sqrt(m * k);
        let state = "Underdamped";
        if (Math.abs(b - crit) < 0.1) state = "Critically Damped";
        else if (b > crit) state = "Overdamped";
        document.getElementById('state_label').innerText = state;

        const data = solveRK4(b);
        
        // Draw Time Graph x(t)
        const ctxT = document.getElementById('timeGraph').getContext('2d');
        ctxT.clearRect(0,0,600,200);
        ctxT.beginPath();
        data.forEach(pt => ctxT.lineTo(pt.t * 40, 100 - pt.x * 80));
        ctxT.stroke();

        // Draw Phase Portrait v(x)
        const ctxP = document.getElementById('phaseGraph').getContext('2d');
        ctxP.clearRect(0,0,300,300);
        ctxP.beginPath();
        data.forEach(pt => ctxP.lineTo(150 + pt.x * 120, 150 - pt.v * 30));
        ctxP.stroke();
    }

    document.getElementById('b_slider').addEventListener('input', draw);
    draw();
</script>
</body>
</html>
