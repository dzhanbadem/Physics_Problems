To solve for the motion of a projectile, we analyze the horizontal and vertical components of its movement independently using the laws of kinematics.

### 1. Initial Velocity Components
First, we decompose the initial velocity vector $v_0 = 100 \text{ m/s}$ into its components using the angle $\theta = 37^\circ$:
* **Horizontal:** $v_{0x} = v_0 \cos(37^\circ) = 100 \times 0.8 = 80 \text{ m/s}$
* **Vertical:** $v_{0y} = v_0 \sin(37^\circ) = 100 \times 0.6 = 60 \text{ m/s}$

---

### 2. Derivation of Differential Equations
Assuming no air resistance, the only force acting on the projectile is gravity ($g \approx 9.8 \text{ m/s}^2$) acting in the negative $y$-direction.

**Horizontal Direction ($x$):**
There is no horizontal force, so acceleration $a_x = 0$.
$$\frac{d^2x}{dt^2} = 0$$
Integrating once gives the velocity: $v_x(t) = v_{0x} = 80$.
Integrating again gives the position: **$x(t) = 80t$**.

**Vertical Direction ($y$):**
The acceleration is constant and downward: $a_y = -g$.
$$\frac{d^2y}{dt^2} = -g$$
Integrating once gives the velocity: $v_y(t) = v_{0y} - gt = 60 - 9.8t$.
Integrating again gives the position: **$y(t) = 60t - \frac{1}{2}gt^2$**.



---

### 3. Time of Flight ($t_f$)
The projectile hits the ground when the vertical displacement $y(t)$ returns to zero.
$$0 = 60t - 4.9t^2$$
$$0 = t(60 - 4.9t)$$
Ignoring the trivial solution at $t=0$ (launch):
$$t_f = \frac{60}{4.9} \approx \mathbf{12.24 \text{ s}}$$

---

### 4. Maximum Height ($H$)
The maximum height occurs when the vertical velocity $v_y$ is exactly zero.
$$0 = 60 - 9.8t \implies t_{peak} \approx 6.12 \text{ s}$$
Substitute $t_{peak}$ into the $y(t)$ equation:
$$H = 60(6.12) - 4.9(6.12)^2$$
$$H \approx \mathbf{183.67 \text{ m}}$$

---

### 5. Range ($R$)
The range is the total horizontal distance traveled during the time of flight.
$$R = x(t_f) = 80 \times 12.24$$
$$R \approx \mathbf{979.2 \text{ m}}$$



---

### Summary Table
| Parameter | Value | Unit |
| :--- | :--- | :--- |
| Time of Flight | $12.24$ | $\text{s}$ |
| Max Height | $183.67$ | $\text{m}$ |
| Range | $979.2$ | $\text{m}$ |

Would you like me to create an interactive HTML simulation for this specific projectile so you can visualize the parabola on your github.dev?
