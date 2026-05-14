# Task 08 – Mass-Spring Measurements

## Problem Statement

Generate an HTML simulator of a mass on a spring with a timing function. Perform 10 measurements for 10 complete oscillations. Calculate the mean period, standard deviation, and the spring constant with its uncertainty (assume mass is exact).

## Theory

The period of a mass-spring system is given by:

$$
T = 2\pi \sqrt{\frac{m}{k}}
$$

Solving for the spring constant $k$:

$$
k = \frac{4\pi^2 m}{T^2}
$$

The relative uncertainty in $k$ due to the uncertainty in $T$ (assuming $m$ is exact) is:

$$
\frac{\Delta k}{k} = 2 \frac{\Delta T}{T}
$$

## Step-by-Step Solution

### 1. HTML Simulator Code

Save the following as `spring.html`. It provides a visual oscillator and a stopwatch.

```html
<!DOCTYPE html>
<html>
<head><title>Spring Simulator</title></head>
<body>
    <h3>Mass-Spring Oscillator (m = 1.0 kg)</h3>
    <canvas id="canvas" width="200" height="300" style="border:1px solid black;"></canvas><br>
    <button onclick="startStopwatch()">Start/Stop</button>
    <button onclick="resetStopwatch()">Reset</button>
    <p>Time: <span id="time">0.00</span> s</p>
    <script>
        let t = 0;
        let timerRunning = false;
        let startTime = 0;
        
        function draw() {
            const canvas = document.getElementById('canvas');
            const ctx = canvas.getContext('2d');
            ctx.clearRect(0, 0, 200, 300);
            
            // k = 10 N/m, m = 1.0 kg -> omega = sqrt(10) ~ 3.16 rad/s
            let y = 150 + 50 * Math.cos(3.16 * t); 
            
            ctx.beginPath();
            ctx.moveTo(100, 0);
            ctx.lineTo(100, y - 20); // Spring
            ctx.stroke();
            
            ctx.fillStyle = 'blue';
            ctx.fillRect(80, y - 20, 40, 40); // Mass
            
            t += 0.016;
            if(timerRunning) {
                document.getElementById('time').innerText = ((Date.now() - startTime)/1000).toFixed(2);
            }
            requestAnimationFrame(draw);
        }
        
        function startStopwatch() {
            if(!timerRunning) startTime = Date.now() - parseFloat(document.getElementById('time').innerText)*1000;
            timerRunning = !timerRunning;
        }
        function resetStopwatch() { timerRunning = false; document.getElementById('time').innerText = "0.00"; }
        
        draw();
    </script>
</body>
</html>
