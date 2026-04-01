This problem moves from basic dynamics into the calculus-based foundations of classical mechanics. We are looking at a **restoring force**, which is the basis for springs and oscillations.

---

### 1. The Equation of Motion
**The Concept:** Newton’s Second Law states $F = ma$. Since acceleration is the second derivative of position with respect to time ($a = \frac{d^2x}{dt^2}$), we can write the differential equation.

**The Setup:**
$$-kx = m\frac{d^2x}{dt^2} \implies \frac{d^2x}{dt^2} + \frac{k}{m}x = 0$$

**The Solution:**
This is a second-order linear differential equation. Its solution is a sinusoidal function:
$$x(t) = A \cos(\omega t + \phi)$$
Where $\omega = \sqrt{\frac{k}{m}}$ is the angular frequency.

---

### 2. Calculate the Work Done ($0 \to x_0$)
**The Concept:** When a force varies with position, we cannot simply multiply force by distance. We must **integrate** the force over the displacement.

**The Calculation:**
$$W = \int_{0}^{x_0} F(x) \, dx = \int_{0}^{x_0} (-kx) \, dx$$
Evaluating the integral:
$$W = \left[ -\frac{1}{2}kx^2 \right]_{0}^{x_0} = -\frac{1}{2}kx_0^2$$

---

### 3. Interpret as Potential Energy ($U$)
**The Concept:** The work done by a **conservative force** is equal to the negative change in potential energy ($W = -\Delta U$). 

Assuming $U(0) = 0$:
$$\Delta U = -W = \frac{1}{2}kx_0^2$$
So, the potential energy stored at position $x$ is:
$$U(x) = \frac{1}{2}kx^2$$
This tells us that as we pull a spring away from equilibrium, we are doing work against the force, and that energy is stored in the system.

---

### 4. Verify the Relationship $F = -\frac{dU}{dx}$
To verify, we take the negative derivative of our potential energy function with respect to $x$:
$$-\frac{d}{dx} \left( \frac{1}{2}kx^2 \right) = -\left( \frac{1}{2}k \cdot 2x \right) = -kx$$
This matches our original force $F(x) = -kx$, confirming the mathematical consistency of the system.

---

### 5. Graphing $F(x)$ and $U(x)$


* **Force $F(x)$:** A straight line with a negative slope ($-k$). It shows that as displacement $x$ increases, the restoring force becomes more negative (points back to the start).


* **Potential Energy $U(x)$:** A parabola opening upward. It shows that energy is positive regardless of whether you compress (negative $x$) or stretch (positive $x$) the spring.

---

**Teaching Tip:** Point out to the class that the "Force" is the **slope** of the "Potential Energy" graph (multiplied by $-1$). At the bottom of the $U(x)$ curve ($x=0$), the slope is zero, which is why the force is zero at the equilibrium point!

