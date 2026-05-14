# Task 09 – Pendulum Measurements

## Problem Statement

Create an HTML pendulum simulator with a stopwatch. Assuming exact string length, perform 10 measurements for 10 complete oscillations. Calculate the mean period, standard deviation, and determine $g$ with its uncertainty.

## Theory

The period of a simple pendulum for small angles is:

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

Solving for the acceleration due to gravity $g$:

$$
g = \frac{4\pi^2 L}{T^2}
$$

The relative uncertainty in $g$ (assuming $L$ is exact) is:

$$
\frac{\Delta g}{g} = 2 \frac{\Delta T}{T}
$$

## Step-by-Step Solution

### 1. HTML Simulator Code

Save this as `pendulum.html`.

```html
<!DOCTYPE html>
<html>
<head><title>Pendulum Simulator</title></head>
<body>
    <h3>Simple Pendulum (L = 1.0 m)</h3>
    <canvas id="canvas" width="300" height="300" style="border:1px solid black;"></canvas><br>
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
            ctx.clearRect(0, 0, 300, 300);
            
            // L = 1.0 m, g = 9.81 m/s^2 -> omega = sqrt(9.81) ~ 3.132 rad/s
            let theta = 0.2 * Math.cos(3.132 * t); 
            let x = 150 + 200 * Math.sin(theta);
            let y = 0 + 200 * Math.cos(theta);
            
            ctx.beginPath();
            ctx.moveTo(150, 0);
            ctx.lineTo(x, y); // String
            ctx.stroke();
            
            ctx.beginPath();
            ctx.arc(x, y, 10, 0, 2*Math.PI); // Bob
            ctx.fillStyle = 'red';
            ctx.fill();
            
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
