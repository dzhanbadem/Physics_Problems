This problem explores the **Superposition Principle**, specifically how two identical waves traveling in opposite directions combine to form a **standing wave**.

## 3. Superposition: Forming a Standing Wave

### The Concept
When two waves of the same frequency and amplitude travel in opposite directions, they interfere. Unlike a traveling wave, the resulting wave pattern does not move left or right—the peaks simply oscillate up and down in place. This is why we call it a "standing" wave.



---

### Step-by-Step Execution

**1. Apply the Superposition Principle**
The resultant displacement $y(x, t)$ is the sum of the two individual waves:
$$y(x, t) = y_1 + y_2$$
$$y(x, t) = A \sin(kx - \omega t) + A \sin(kx + \omega t)$$

**2. Use the Trigonometric Identity**
To simplify this, we use the sum-to-product identity: $\sin(\alpha) + \sin(\beta) = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)$.
Let $\alpha = kx + \omega t$ and $\beta = kx - \omega t$.

* $\frac{\alpha + \beta}{2} = \frac{(kx + \omega t) + (kx - \omega t)}{2} = kx$
* $\frac{\alpha - \beta}{2} = \frac{(kx + \omega t) - (kx - \omega t)}{2} = \omega t$

Plugging these into the identity:
$$y(x, t) = [2A \sin(kx)] \cos(\omega t)$$

**3. Analyze the Resulting Equation**
* The term **$2A \sin(kx)$** represents the **amplitude** of the oscillation at any position $x$.
* The term **$\cos(\omega t)$** describes how the entire pattern oscillates in time.

---

### Identifying the Nodes
**Nodes** are points where the displacement is **always zero**, regardless of the time $t$. This happens when the spatial part of our equation equals zero:
$$\sin(kx) = 0$$

The sine function is zero when its argument is an integer multiple of $\pi$:
$$kx = n\pi \quad \text{where } n = 0, 1, 2, \dots$$

Since the wave number $k$ is defined as $k = \frac{2\pi}{\lambda}$, we substitute:
$$\left(\frac{2\pi}{\lambda}\right)x = n\pi$$
$$x = \frac{n\lambda}{2}$$

**Positions of Nodes:** $x = 0, \frac{\lambda}{2}, \lambda, \frac{3\lambda}{2}, \dots$

---

### Summary for Presentation
* **The Standing Wave Equation:** $y(x, t) = 2A \sin(kx) \cos(\omega t)$
* **Node Locations:** Occur every half-wavelength ($\lambda/2$).

> **Pro-Tip for Class:** Point out that in a standing wave, the energy is "trapped" between the nodes. While a traveling wave transports energy from one place to another, a standing wave simply sloshes energy back and forth within its envelope.

