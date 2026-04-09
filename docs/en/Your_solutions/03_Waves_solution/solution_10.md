# Task 10 – Animation: Wave Sources

## Problem Statement

Write an HTML animation to place dots as wave sources described by $u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_0}|^\alpha} \sin(k |\vec{r} - \vec{r_0}| - \omega t)$, allowing adjustment of $\alpha \in [0, 2]$.

## Step-by-Step Solution

Save the following code as an `.html` file. It uses an HTML5 Canvas and pixel manipulation to compute the scalar field $u(\vec{r}, t)$ at each pixel. You can click to add sources.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Wave Sources</title>
</head>
<body>
    <label>Alpha (Attenuation): <input type="range" id="alpha" min="0" max="2" step="0.1" value="0.5"></label>
    <button onclick="sources = []">Clear Sources</button><br>
    <canvas id="canvas" width="400" height="400" style="border:1px solid black; cursor: crosshair;"></canvas>

<script>
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    const imgData = ctx.createImageData(canvas.width, canvas.height);
    
    let sources = [];
    let t = 0;
    const A = 20, k = 0.2, w = 0.5;

    canvas.addEventListener('click', (e) => {
        const rect = canvas.getBoundingClientRect();
        sources.push({ x: e.clientX - rect.left, y: e.clientY - rect.top });
    });

    function draw() {
        const alpha = parseFloat(document.getElementById('alpha').value);
        for (let y = 0; y < canvas.height; y+=2) {
            for (let x = 0; x < canvas.width; x+=2) {
                let u = 0;
                for (let s of sources) {
                    const r = Math.max(1, Math.sqrt((x - s.x)**2 + (y - s.y)**2));
                    u += (A / Math.pow(r, alpha)) * Math.sin(k * r - w * t);
                }
                const color = Math.floor(128 + u * 10);
                
                for(let dy=0; dy<2; dy++) {
                    for(let dx=0; dx<2; dx++) {
                        const idx = ((y+dy) * canvas.width + (x+dx)) * 4;
                        imgData.data[idx] = color;
                        imgData.data[idx+1] = color;
                        imgData.data[idx+2] = color;
                        imgData.data[idx+3] = 255;
                    }
                }
            }
        }
        ctx.putImageData(imgData, 0, 0);
        sources.forEach(s => {
            ctx.fillStyle = 'red';
            ctx.beginPath();
            ctx.arc(s.x, s.y, 4, 0, 2*Math.PI);
            ctx.fill();
        });
        t += 0.5;
        requestAnimationFrame(draw);
    }
    draw();
</script>
</body>
</html>
