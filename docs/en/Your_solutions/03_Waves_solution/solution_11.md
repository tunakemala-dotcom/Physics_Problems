# Task 11 – Animation: Two-Slit Interference

## Problem Statement

Write an HTML animation simulating Young's experiment. The displacement is the sum of partial waves from two point sources. The user should be able to change the slit distance $d$ and wavelength $\lambda$.

## Step-by-Step Solution

Save the following code as an `.html` file. It computes the wave superposition at each point on the canvas in real time to produce the characteristic interference fringes.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Young's Two-Slit Interference</title>
</head>
<body>
    <label>Slit Distance (d): <input type="range" id="dist" min="20" max="150" value="60"></label>
    <label>Wavelength (&lambda;): <input type="range" id="lambda" min="10" max="50" value="20"></label><br>
    <canvas id="canvas" width="500" height="300" style="border:1px solid black; background:#000;"></canvas>

<script>
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    const imgData = ctx.createImageData(canvas.width, canvas.height);
    
    let t = 0;

    function draw() {
        const d = parseFloat(document.getElementById('dist').value);
        const lambda = parseFloat(document.getElementById('lambda').value);
        const k = (2 * Math.PI) / lambda;
        const w = 0.5;
        const A = 100;
        
        const s1 = { x: 50, y: 150 - d/2 };
        const s2 = { x: 50, y: 150 + d/2 };

        for (let y = 0; y < canvas.height; y+=2) {
            for (let x = 0; x < canvas.width; x+=2) {
                const r1 = Math.max(1, Math.sqrt((x - s1.x)**2 + (y - s1.y)**2));
                const r2 = Math.max(1, Math.sqrt((x - s2.x)**2 + (y - s2.y)**2));
                
                const u1 = (A / Math.sqrt(r1)) * Math.sin(k * r1 - w * t);
                const u2 = (A / Math.sqrt(r2)) * Math.sin(k * r2 - w * t);
                const u = u1 + u2;
                
                const intensity = Math.floor(128 + u * 15);
                
                for(let dy=0; dy<2; dy++) {
                    for(let dx=0; dx<2; dx++) {
                        const idx = ((y+dy) * canvas.width + (x+dx)) * 4;
                        imgData.data[idx] = 0;
                        imgData.data[idx+1] = intensity; // Greenish wave
                        imgData.data[idx+2] = Math.floor(intensity/2); 
                        imgData.data[idx+3] = 255;
                    }
                }
            }
        }
        ctx.putImageData(imgData, 0, 0);
        
        ctx.fillStyle = 'white';
        ctx.fillRect(s1.x - 2, s1.y - 2, 4, 4);
        ctx.fillRect(s2.x - 2, s2.y - 2, 4, 4);

        t += 0.5;
        requestAnimationFrame(draw);
    }
    draw();
</script>
</body>
</html>
