This problem ties together everything we've covered: kinematics, vectors, and the fundamental relationship between work and energy. Since the force is constant, the math is straightforward but requires careful bookkeeping of the $x$ and $y$ components.

---

### 1. Determine Acceleration ($\vec{a}$), Velocity ($\vec{v}$), and Position ($\vec{r}$)

**The Concept:** Since the force is constant, the acceleration is constant. We can use standard integration (or kinematic equations) for each component.

* **Acceleration ($\vec{a}$):** $\vec{a} = \frac{\vec{F}}{m} = \frac{[6, 2]}{2} = [3, 1]\ \mathrm{m/s^2}$
* **Velocity ($\vec{v}$):** $\vec{v}(t) = \vec{v}_0 + \vec{a}t = [1, -1] + [3t, 1t] = [1 + 3t, -1 + t]\ \mathrm{m/s}$
* **Position ($\vec{r}$):** $\vec{r}(t) = \vec{r}_0 + \vec{v}_0t + \frac{1}{2}\vec{a}t^2$
    Since $\vec{r}_0 = (0,0)$:
    $\vec{r}(t) = [1t + 1.5t^2, -1t + 0.5t^2]\ \mathrm{m}$

---

### 2. The Trajectory
The trajectory is a **parabola**. You can see this because both $x$ and $y$ are quadratic functions of time.



* At $t=0$, the particle is at $(0,0)$ moving toward the bottom-right.
* As time increases, the constant force pulls it toward the top-right, eventually curving the path into a parabolic arc.

---

### 3. Calculate Work Done at $t=3\ \mathrm{s}$

**The Concept:** For a constant force, Work ($W$) is the dot product of Force and Displacement: $W = \vec{F} \cdot \Delta \vec{r}$.

**Step 1: Find Displacement at $t=3$**
* $x(3) = 1(3) + 1.5(3)^2 = 3 + 13.5 = 16.5\ \mathrm{m}$
* $y(3) = -1(3) + 0.5(3)^2 = -3 + 4.5 = 1.5\ \mathrm{m}$
* $\Delta \vec{r} = [16.5, 1.5]\ \mathrm{m}$

**Step 2: Calculate Dot Product**
$$W = \vec{F} \cdot \Delta \vec{r} = (6 \times 16.5) + (2 \times 1.5)$$
$$W = 99 + 3 = 102\ \mathrm{J}$$

---

### 4. Verification with the Work-Energy Theorem

**The Concept:** The Work-Energy Theorem states that the work done on an object equals its change in Kinetic Energy: $W = \Delta KE = KE_f - KE_i$.

**Step 1: Initial Kinetic Energy ($KE_i$) at $t=0$**
* $v_0^2 = (1)^2 + (-1)^2 = 2$
* $KE_i = \frac{1}{2} m v_0^2 = \frac{1}{2}(2)(2) = 2\ \mathrm{J}$

**Step 2: Final Kinetic Energy ($KE_f$) at $t=3$**
Find velocity at $t=3$:
* $v_x(3) = 1 + 3(3) = 10$
* $v_y(3) = -1 + 1(3) = 2$
* $v_f^2 = (10)^2 + (2)^2 = 104$
* $KE_f = \frac{1}{2} m v_f^2 = \frac{1}{2}(2)(104) = 104\ \mathrm{J}$

**Step 3: Compare Results**
$$\Delta KE = 104\ \mathrm{J} - 2\ \mathrm{J} = 102\ \mathrm{J}$$

**Conclusion:** Since $W = 102\ \mathrm{J}$ and $\Delta KE = 102\ \mathrm{J}$, the theorem is verified.

---

**Teaching Tip:** This is a powerful "closing" problem for your presentation. It shows that whether we look at the problem through the lens of **forces and displacement** or **energy and speeds**, the laws of physics consistently give us the same answer!

