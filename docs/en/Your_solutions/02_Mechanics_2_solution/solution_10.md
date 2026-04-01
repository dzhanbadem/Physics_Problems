To wrap up your presentation, we move into **3D Kinematics and Dynamics**. This problem demonstrates how we can derive every major physical quantity (velocity, momentum, force, and power) simply by knowing the position of an object over time.

### 1. Velocity ($\vec{v}$)
**The Concept:** Velocity is the first derivative of position with respect to time ($v = \frac{dr}{dt}$). We differentiate each component $(x, y, z)$ separately.

**The Calculation:**
* $v_x = \frac{d}{dt}(5t^2 - t) = 10t - 1$
* $v_y = \frac{d}{dt}(2t^3) = 6t^2$
* $v_z = \frac{d}{dt}(-3t + 2) = -3$

**The Result:** $\vec{v}(t) = (10t - 1)\hat{i} + 6t^2\hat{j} - 3\hat{k}$

---

### 2. Momentum ($\vec{p}$)
**The Concept:** Linear momentum is the product of mass and velocity ($\vec{p} = m\vec{v}$).
**Given:** $m = 0.5\text{ kg}$

**The Calculation:**
* $p_x = 0.5(10t - 1) = 5t - 0.5$
* $p_y = 0.5(6t^2) = 3t^2$
* $p_z = 0.5(-3) = -1.5$

**The Result:** $\vec{p}(t) = (5t - 0.5)\hat{i} + 3t^2\hat{j} - 1.5\hat{k}$

---

### 3. Acceleration ($\vec{a}$)
**The Concept:** Acceleration is the derivative of velocity with respect to time ($\vec{a} = \frac{dv}{dt}$).

**The Calculation:**
* $a_x = \frac{d}{dt}(10t - 1) = 10$
* $a_y = \frac{d}{dt}(6t^2) = 12t$
* $a_z = \frac{d}{dt}(-3) = 0$

**The Result:** $\vec{a}(t) = 10\hat{i} + 12t\hat{j} + 0\hat{k}$

---

### 4. Force ($\vec{F}$)
**The Concept:** According to Newton's Second Law, Force is mass times acceleration ($\vec{F} = m\vec{a}$).

**The Calculation:**
* $F_x = 0.5(10) = 5\text{ N}$
* $F_y = 0.5(12t) = 6t\text{ N}$
* $F_z = 0.5(0) = 0\text{ N}$

**The Result:** $\vec{F}(t) = 5\hat{i} + 6t\hat{j} + 0\hat{k}$

---

### 5. Power ($P$)
**The Concept:** Power is the rate at which work is done. It can be calculated using the dot product of the Force vector and the Velocity vector ($P = \vec{F} \cdot \vec{v}$).

**The Calculation:**
$$P = (F_x \cdot v_x) + (F_y \cdot v_y) + (F_z \cdot v_z)$$
$$P = 5(10t - 1) + 6t(6t^2) + 0(-3)$$
$$P = 50t - 5 + 36t^3$$

**The Result:** $P(t) = 36t^3 + 50t - 5$ (in Watts)

---

### Final Summary for Class


* **Velocity:** Shows how the position changes.
* **Momentum:** "Quantity of motion" scaled by mass.
* **Acceleration:** Shows that a constant force acts in $x$, but a time-varying force acts in $y$.
* **Power:** The rate at which the field is pumping energy into the particle at any given second.

**Teaching Tip:** Point out to your students that since $a_z = 0$, the force in the $z$-direction is zero. This means the particle's movement in the $z$-direction is "inertial" (constant velocity), even though the field is pushing it in other directions!

