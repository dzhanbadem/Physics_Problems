To show analytically that the maximum range is achieved at $45^\circ$, we must first derive the range equation and then use calculus to find its maximum point.

### 1. Derivation of the Range Equation
The range ($R$) is the horizontal distance $x(t)$ traveled during the total time of flight ($t_f$). 

From the previous kinematics equations:
* Horizontal position: $x(t) = (v_0 \cos \theta)t$
* Vertical position: $y(t) = (v_0 \sin \theta)t - \frac{1}{2}gt^2$

**Step A: Find Time of Flight ($t_f$)**
The projectile hits the ground when $y(t) = 0$:
$$0 = t(v_0 \sin \theta - \frac{1}{2}gt)$$
Solving for $t$ (excluding the launch at $t=0$):
$$t_f = \frac{2v_0 \sin \theta}{g}$$

**Step B: Substitute $t_f$ into $x(t)$**
$$R = (v_0 \cos \theta) \left( \frac{2v_0 \sin \theta}{g} \right)$$
$$R = \frac{v_0^2 (2 \sin \theta \cos \theta)}{g}$$

Using the trigonometric identity $\sin(2\theta) = 2 \sin \theta \cos \theta$, we get:
$$R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$$



---

### 2. Optimization using Calculus
To find the angle $\theta$ that maximizes $R$, we take the derivative of $R$ with respect to $\theta$ and set it to zero.

**Step C: Differentiate $R(\theta)$**
$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot \frac{d}{d\theta}[\sin(2\theta)]$$
$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot 2\cos(2\theta)$$

**Step D: Set the derivative to zero**
For a maximum or minimum:
$$0 = \frac{2v_0^2}{g} \cos(2\theta)$$
Since $v_0$ and $g$ are non-zero constants, we solve for $\cos(2\theta) = 0$:
$$2\theta = 90^\circ$$
$$\theta = 45^\circ$$



---

### 3. Conclusion
The range is a function of $\sin(2\theta)$. Since the maximum value of the sine function is **1** (which occurs when the argument is $90^\circ$), the range $R$ is maximized when:
$$\sin(2\theta) = 1 \implies 2\theta = 90^\circ \implies \theta = 45^\circ$$

**Physics Insight:** At $45^\circ$, the projectile has a perfect balance between its horizontal velocity (which covers distance) and its vertical velocity (which provides time in the air). At higher angles, it stays in the air longer but moves too slowly horizontally; at lower angles, it moves quickly but hits the ground too soon.

---

### Summary Table: Effect of Angle on Range
| Angle ($\theta$) | $\sin(2\theta)$ | Result |
| :--- | :--- | :--- |
| $0^\circ$ | $0$ | Range is zero (hits ground immediately). |
| $30^\circ$ | $0.866$ | Sub-optimal range. |
| **$45^\circ$** | **$1.000$** | **Maximum Range.** |
| $60^\circ$ | $0.866$ | Same range as $30^\circ$ (complementary angles). |
| $90^\circ$ | $0$ | Range is zero (fired straight up). |

Would you like me to update your GitHub interactive simulation to include a "Max Range" visual guide showing how the arc changes at $45^\circ$?
