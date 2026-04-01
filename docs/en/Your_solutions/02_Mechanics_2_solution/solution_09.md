This problem introduces **Air Resistance (Drag)**, which makes the physics much more realistic but the math a bit more complex. Since the drag force $F_d = -kv$ is proportional to velocity, the acceleration isn't constant.

### 1. Analytical Solution (Velocity and Position)
**The Concept:** This is a first-order linear differential equation. We rearrange it to isolate $v$ and $t$.

**Step 1: Solve for $v(t)$**
Divide by $m$ and rearrange:
$$\frac{dv}{dt} = -g - \frac{k}{m}v$$
Let $\rho = \frac{k}{m}$ (the drag coefficient per unit mass).
$$\frac{dv}{dt} = -(g + \rho v)$$
Integrating using the initial condition $v(0) = v_0$:
$$v(t) = \left(v_0 + \frac{g}{\rho}\right)e^{-\rho t} - \frac{g}{\rho}$$

**Step 2: Solve for $x(t)$**
To find position, we integrate $v(t)$ with respect to time, using $x(0) = 10$:
$$x(t) = 10 + \int_{0}^{t} v(t') dt'$$
$$x(t) = 10 + \frac{1}{\rho}\left(v_0 + \frac{g}{\rho}\right)(1 - e^{-\rho t}) - \frac{g}{\rho}t$$

---

### 2. Determine Maximum Height ($H_{max}$)
The object reaches its maximum height when its velocity is zero ($v(t) = 0$).

1. **Find the time to reach peak ($t_{up}$):**
   Set $v(t) = 0$:
   $$0 = (v_0 + \frac{g}{\rho})e^{-\rho t_{up}} - \frac{g}{\rho} \implies e^{-\rho t_{up}} = \frac{g}{g + \rho v_0}$$
   $$t_{up} = \frac{1}{\rho} \ln\left(1 + \frac{\rho v_0}{g}\right)$$

2. **Calculate $H_{max}$:**
   Plug $t_{up}$ back into the position equation $x(t)$.
   $$H_{max} = 10 + \frac{v_0}{\rho} - \frac{g}{\rho^2} \ln\left(1 + \frac{\rho v_0}{g}\right)$$

---

### 3. Comparison with the No-Drag Case
In a vacuum (no drag, $k=0$):
* **Equation:** $x(t) = 10 + v_0t - \frac{1}{2}gt^2$
* **Max Height:** $H_{vac} = 10 + \frac{v_0^2}{2g}$
* **Symmetry:** The time going up equals the time coming down.

**With Drag:**
* **Lower Peak:** $H_{max} < H_{vac}$ because drag does negative work, removing energy.
* **Asymmetry:** The object falls more slowly than it rises because drag acts upward during the fall, opposing gravity.
* **Terminal Velocity:** Unlike the vacuum case, the object will eventually reach a constant speed ($v_{term} = mg/k$) if it falls far enough.



---

### 4. Numerical Simulation (Python)
You can use this Python code to visualize the difference for your class. It uses the "Euler Method" to step through time.

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
m, g, k = 1.0, 9.8, 0.15
v0, x0 = 30.0, 10.0
dt = 0.01

# Simulation 1: With Drag
t, x, v = [0], [x0], [v0]
while x[-1] > 0:
    dv = (-m*g - k*v[-1])/m * dt
    v.append(v[-1] + dv)
    x.append(x[-1] + v[-1] * dt)
    t.append(t[-1] + dt)

# Simulation 2: No Drag (Analytical)
t_no = np.linspace(0, max(t), 100)
x_no = x0 + v0*t_no - 0.5*g*t_no**2
x_no = np.clip(x_no, 0, None)

# Plotting
plt.plot(t, x, label='With Drag')
plt.plot(t_no, x_no, '--', label='No Drag (Vacuum)')
plt.xlabel('Time (s)')
plt.ylabel('Height (m)')
plt.legend()
plt.title('Vertical Throw: Drag vs Vacuum')
plt.show()
```

**Teaching Tip:** Point out that the "With Drag" curve is not a perfect parabola—it’s "squashed." This is a visual representation of energy being lost to the environment.

