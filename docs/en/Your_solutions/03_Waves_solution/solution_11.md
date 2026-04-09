This problem takes the superposition principle from the previous questions and applies it to one of the most famous experiments in physics history: Young's Double-Slit Experiment. This experiment was crucial because it proved that light behaves like a wave.

## 11. Interactive Two-Slit Interference (Young's Experiment)

### 1. The Concept and Formula Breakdown
In Young's experiment, a single light source illuminates two narrow, parallel slits. Because they originate from the same source, the waves emerging from the two slits are **coherent** (meaning they have the same frequency and a constant phase relationship).

The formula given describes how these two waves combine at any point $\vec{r}$ in space:

$$
u(\vec{r},t) = \underbrace{ \left( \frac{A}{|\vec{r}-\vec{r_1}|} \right) \sin(k |\vec{r} - \vec{r_1}| - \omega t) }_{\text{Wave from Slit 1}} + \underbrace{ \left( \frac{A}{|\vec{r}-\vec{r_2}|} \right) \sin(k |\vec{r} - \vec{r_2}| - \omega t) }_{\text{Wave from Slit 2}}
$$

Let's break down the key parameters for your presentation:

* **Coherence:** The formulas for Slit 1 and Slit 2 are identical, with the same $A$, $k$, and $\omega$. Only their positions ($\vec{r_1}, \vec{r_2}$) and therefore the distances to the point $\vec{r}$ are different.
* **Wavelength ($\lambda$):** Controlled by the wave number, $k = \frac{2\pi}{\lambda}$. Changing $\lambda$ directly changes how "stretched out" or "compressed" the wave pattern is.
* **Slit Separation ($d$):** The distance $|\vec{r_1} - \vec{r_2}|$. This determines the **path difference** for the two waves. Path difference is everything in interference!



---

### 2. Implementation: The Mechanics of the Pattern
To visualize this in real-time, we will use the same pixel-by-pixel numerical shading technique we used in Question 10. For every pixel $(x,y)$, the code:

1.  Calculates the distance to Slit 1 ($|\vec{r}-\vec{r_1}|$).
2.  Calculates the distance to Slit 2 ($|\vec{r}-\vec{r_2}|$).
3.  Calculates the instantaneous displacement ($u$) from *each* slit.
4.  **Sums them together** (Superposition: $u_{total} = u_1 + u_2$).
5.  Assigns a color based on $u_{total}$ (Crest = Green, Trough = Blue, No Wave = Black).

---

### 3. Interactive Animation (HTML/JavaScript)
Save this code as an `.html` file. During your presentation, you will have two sliders: one for Wavelength ($\lambda$) and one for Slit Distance ($d$). You can watch the interference pattern change instantly.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Young's Double-Slit Interference</title>
    <style>
        body { font-family: sans-serif; display: flex; flex-direction: column; align-items: center; background: #222; color: #eee; margin: 20px; }
        .controls { background: #333; padding: 15px; border-radius: 8px; margin: 10px; width: 90%; max-width: 800px; }
        .control-group { margin-bottom: 10px; display: flex; align-items: center; justify-content: space-between;}
        canvas { border: 2px solid #555; background: black; box-shadow: 0 0 15px rgba(0,255,0,0.2); }
        .label { font-weight: bold; width: 150px; }
        .value { width: 60px; text-align: right; margin-left: 10px;}
    </style>
</head>
<body>
    <h2>Young's Double-Slit Interference Simulator</h2>
    
    <div class="controls">
        <div class="control-group">
            <span class="label">Wavelength (\(\lambda\)): </span>
            <input type="range" id="lambdaSlider" min="20" max="150" step="1" value="70" style="width: 400px;">
            <span class="value" id="lambdaVal">70</span> px
        </div>
        <div class="control-group">
            <span class="label">Slit Distance (\(d\)): </span>
            <input type="range" id="dSlider" min="10" max="250" step="1" value="80" style="width: 400px;">
            <span class="value" id="dVal">80</span> px
        </div>
        <p style="text-align: center; color: #aaa; margin: 5px 0 0 0;"><em>Observing constructive and destructive interference in real-time.</em></p>
    </div>

    <canvas id="waveCanvas" width="800" height="600"></canvas>

<script>
    const canvas = document.getElementById('waveCanvas');
    const ctx = canvas.getContext('2d');
    const lambdaSlider = document.getElementById('lambdaSlider');
    const dSlider = document.getElementById('dSlider');
    const lambdaVal = document.getElementById('lambdaVal');
    const dVal = document.getElementById('dVal');

    // Fixed Parameters
    const A = 60.0;    // Main Amplitude
    const omega = 0.08;// Angular frequency (Controls wave speed/animation rate)
    let time = 0;

    // Interactive Parameters (Initial Values)
    let lambda = 70;   // Wavelength (pixels)
    let k = 2 * Math.PI / lambda; // Wave number
    let d = 80;        // Distance between slits (pixels)

    // Handle Sliders
    lambdaSlider.oninput = function() {
        lambda = parseInt(this.value);
        lambdaVal.innerText = lambda;
        k = 2 * Math.PI / lambda; // Recalculate k
    }
    dSlider.oninput = function() {
        d = parseInt(this.value);
        dVal.innerText = d;
    }

    function drawWaves() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        time += 1.0; // Advance time (animation)

        // Define slit positions (Centered on left edge)
        const slit_x = 10;
        const slit1_y = canvas.height / 2 - d / 2;
        const slit2_y = canvas.height / 2 + d / 2;

        const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
        const data = imageData.data;

        // Iterate through EVERY pixel
        for (let y = 0; y < canvas.height; y++) {
            for (let x = 0; x < canvas.width; x++) {
                
                // --- Step 1 & 2: Calculate Distances (r1 and r2) ---
                const dist1 = Math.sqrt(Math.pow(x - slit_x, 2) + Math.pow(y - slit1_y, 2));
                const dist2 = Math.sqrt(Math.pow(x - slit_x, 2) + Math.pow(y - slit2_y, 2));

                // Skip points right at the slits to avoid division by zero
                if (dist1 < 2 || dist2 < 2) continue; 

                // --- Step 3: Calculate Individual Waves ---
                // u = ( A / r ) * sin( k * r - omega * time )
                // Note: amplitude decay is 1/r
                let u1 = (A / dist1) * Math.sin(k * dist1 - omega * time);
                let u2 = (A / dist2) * Math.sin(k * dist2 - omega * time);

                // --- Step 4: Superposition (Combine) ---
                let u_total = u1 + u2; 

                // --- Step 5: Color Mapping (Visualization) ---
                const index = (y * canvas.width + x) * 4;
                
                // Map amplitude to brightness
                let brightness = Math.abs(u_total) * 15; // Scaling factor for visibility

                // We visualize using green for positive displacement, blue for negative.
                // This makes interference regions very clear.
                data[index + 0] = 0;                           // Red (R)
                data[index + 1] = u_total > 0 ? brightness : 0;// Green (G)
                data[index + 2] = u_total < 0 ? brightness : 0;// Blue (B)
                data[index + 3] = 255;                          // Alpha (Opacity)
            }
        }

        ctx.putImageData(imageData, 0, 0);

        // Draw the slit positions as visual references
        ctx.fillStyle = 'white';
        ctx.beginPath(); ctx.arc(slit_x, slit1_y, 4, 0, 2 * Math.PI); ctx.fill();
        ctx.beginPath(); ctx.arc(slit_x, slit2_y, 4, 0, 2 * Math.PI); ctx.fill();

        requestAnimationFrame(drawWaves); // Animation loop
    }

    // Start
    drawWaves();
</script>
</body>
</html>
```

---

### Summary for Presentation
* **The Anatomy of the Pattern:** When you play the animation, you will see strong, stable radial lines branching out. These are the **fringes**. The areas with intense green/blue are maxima (constructive interference), and the dark lines between them are minima (destructive interference).

* **Effect of Wavelength ($\lambda$):** Drag the wavelength slider up (larger $\lambda$). The fringes will spread out. Drag it down (smaller $\lambda$). The fringes get much denser and closer together. This shows that the separation between fringes is **directly proportional** to the wavelength.

* **Effect of Slit Distance ($d$):** Drag the slit distance slider up (move slits apart). The fringes will get significantly closer together. Drag them close together (move slits together). The fringes get wider and fewer. This shows that the separation between fringes is **inversely proportional** to the distance between the slits.

> **Pro-Tip for Class:** Connect this visual intuition directly to the standard formula for Young's fringes: $\Delta y \approx \frac{L\lambda}{d}$ (where $L$ is the distance to the screen). This simulation perfectly demonstrates *why* $\lambda$ is in the numerator (spreads fringes out) and *why* $d$ is in the denominator (compresses them)!