This final problem is a fantastic way to conclude your presentation because it takes all the concepts we've discussed—the Wave Equation, Superposition Principle, Wavelength, and Frequency—and combines them into a dynamic, visual simulation.

## 10. Interactive Wave Interference Simulation

### 1. The Concept and Formula Breakdown
The problem gives us a powerful equation to model how a point source generates waves. Let's break down exactly what each term means for your classmates:

$$
u(\vec{r},t) = \underbrace{ \left( \frac{A}{|\vec{r}-\vec{r_0}|^\alpha} \right) }_{\text{Term 1: Decaying Amplitude}} \cdot \underbrace{ \sin(k |\vec{r} - \vec{r_0}| - \omega t) }_{\text{Term 2: The Oscillating Wave}}
$$

* **$\vec{r_0}$:** The location of the dot (the source).
* **$\vec{r}$:** The position in space we are calculating (any pixel on the screen).
* **$|\vec{r}-\vec{r_0}|$:** The *distance* from the source to that point in space. Let's call this distance $d$.

* **Term 1 (Amplitude Decay):** This is the key insight. The "volume" of the wave doesn't stay constant ($A$). It decreases as the wave travels further away ($A / d^\alpha$).
    * The parameter $\alpha$ (Alpha) controls how *fast* the wave fades.
    * If $\alpha=0$, there is *no decay*—the wave has the same amplitude everywhere (physically unrealistic, but helpful for seeing clear interference patterns).
    * If $\alpha=1$, the amplitude drops linearly ($1/d$). This is a simplified 2D model (like ripples expanding on water).
    * If $\alpha=2$, the amplitude drops off rapidly ($1/d^2$), like light intensity or gravitational pull.

* **Term 2 (The Wave):** This is the classic traveling sine wave, $(kd - \omega t)$, just expressed using the distance $d$.



---

### 2. Implementation: Numerical Solution and Superposition
To make this work in real-time on a screen, we must handle two main challenges:

**A. Numerical Solution via Pixel Shading**
The computer doesn't solve a differential equation. Instead, we use a technique used in computer graphics. For every single pixel (coordinate $\vec{r}$) on our canvas, we must plug its coordinates into the master equation, calculate its "height" ($u$) at the current time ($t$), and assign it a color (e.g., $u=1$ is red, $u=-1$ is blue, $u=0$ is white). This must be done at 60 frames per second to show smooth motion.

**B. The Superposition Principle (The "Add It Up" Step)**
This simulation is the ultimate demonstration of Superposition. If you place 5 dots, the computer has to run a loop:
1.  **Look at Pixel (1,1).**
2.  Calculate the wave from Dot 1 at that location.
3.  Calculate the wave from Dot 2...
4.  **Add them together** ($u_{total} = u_1 + u_2 + u_3 + u_4 + u_5$).
5.  Set the pixel color based on $u_{total}$.

Where crests meet crests, we get super-high interference (constructive). Where a crest meets a trough, they cancel to zero (destructive).

---

### 3. Interactive Animation (HTML/JavaScript)
Here is the code. Copy this into an `.html` file. During your presentation, you will be able to click on the black canvas to add sources, and use the slider to change $\alpha$ in real-time.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Wave Source Interference</title>
    <style>
        body { font-family: sans-serif; display: flex; flex-direction: column; align-items: center; background: #222; color: #eee; }
        .controls { background: #333; padding: 20px; border-radius: 8px; margin: 10px; text-align: center; width: 80%; }
        canvas { border: 2px solid #555; background: black; cursor: crosshair; }
        .slider-label { font-weight: bold; margin-right: 10px; }
    </style>
</head>
<body>
    <h2>Wave Source Interference Simulation</h2>
    
    <div class="controls">
        <label class="slider-label">Alpha (Decay Rate, \(\alpha\)): </label>
        <input type="range" id="alphaSlider" min="0" max="2" step="0.1" value="0.5" style="width: 300px;">
        <span id="alphaVal">0.5</span>
        <button onclick="clearSources()" style="margin-left: 20px; padding: 5px 15px;">Clear Sources</button>
        <p><em>Click on the canvas to add wave sources. Clear them to start over.</em></p>
    </div>

    <canvas id="waveCanvas" width="800" height="600"></canvas>

<script>
    const canvas = document.getElementById('waveCanvas');
    const ctx = canvas.getContext('2d');
    const alphaSlider = document.getElementById('alphaSlider');
    const alphaVal = document.getElementById('alphaVal');

    // Parameters
    let A = 40.0;    // Main Amplitude
    let k = 0.06;    // Wave number (Controls wavelength, λ = 2π/k ≈ 100 pixels)
    let omega = 0.05;// Angular frequency (Controls speed)
    let sources = [];// Array to store source positions [{x, y}]
    let time = 0;
    let alpha = 0.5;

    // Handle User Input (Adding Sources)
    canvas.addEventListener('mousedown', function(event) {
        const rect = canvas.getBoundingClientRect();
        const x = event.clientX - rect.left;
        const y = event.clientY - rect.top;
        sources.push({ x, y });
    });

    // Handle Slider Input
    alphaSlider.oninput = function() {
        alpha = parseFloat(this.value);
        alphaVal.innerText = alpha;
    }

    function clearSources() { sources = []; }

    function drawWaves() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        time += 1.0; // Advance simulation time

        // Get pixel data
        const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
        const data = imageData.data;

        // Step 3 & 4: Numerical Loop and Superposition
        // Iterate through EVERY pixel
        for (let y = 0; y < canvas.height; y++) {
            for (let x = 0; x < canvas.width; x++) {
                let u_total = 0; // Total amplitude at this point (r)

                // Sum up contributions from all sources (Superposition)
                for (let i = 0; i < sources.length; i++) {
                    const r0 = sources[i];
                    const dx = x - r0.x;
                    const dy = y - r0.y;
                    const dist = Math.sqrt(dx * dx + dy * dy);

                    // Skip the calculation exactly at the source (dist = 0) to avoid division by zero
                    if (dist < 1) continue; 

                    // --- The Master Equation Implementation ---
                    // u = ( A / dist^alpha ) * sin( k * dist - omega * time )
                    let u = (A / Math.pow(dist, alpha)) * Math.sin(k * dist - omega * time);
                    u_total += u; 
                }

                // --- Color Mapping (Visualization) ---
                const index = (y * canvas.width + x) * 4;
                
                // Color mapping: 
                // positive u -> red channel, negative u -> blue channel
                let colorInt = Math.abs(u_total) * 15; // Brightness scaling

                data[index + 0] = u_total > 0 ? colorInt : 0;   // Red channel (R)
                data[index + 1] = 0;                           // Green channel (G)
                data[index + 2] = u_total < 0 ? colorInt : 0;   // Blue channel (B)
                data[index + 3] = 255;                          // Alpha (Opacity) - Full
            }
        }

        ctx.putImageData(imageData, 0, 0);

        // Optional: Draw the source dots themselves
        for (let s of sources) {
            ctx.beginPath();
            ctx.arc(s.x, s.y, 4, 0, 2 * Math.PI);
            ctx.fillStyle = 'white';
            ctx.fill();
        }

        requestAnimationFrame(drawWaves); // Loop the animation
    }

    // Start the animation
    drawWaves();
</script>
</body>
</html>
```

---

### Summary for Presentation
* **Visualization (Mapping):** Explain that the red spots are positive amplitudes (crests) and the blue spots are negative amplitudes (troughs). Black/dark areas are zero amplitude, showing destructive interference.
* **The Decay ($\alpha$):** Ask the class to observe the sources. Increase $\alpha$ to 1.5 or 2.0. The waves will fade quickly, and the interference patterns will only exist very close to the dots. Set $\alpha$ to 0.0, and the patterns will be incredibly complex and fill the whole screen.

> **Pro-Tip for Class:** Point out that this concept of "Add it all up" (Superposition) is the fundamental idea behind many crucial modern technologies. When you have multiple antennas on your Wi-Fi router (MIMO) or multiple speakers in a stadium, engineers use these exact formulas to ensure the waves add constructively in the areas they want coverage and don't cancel each other out!

