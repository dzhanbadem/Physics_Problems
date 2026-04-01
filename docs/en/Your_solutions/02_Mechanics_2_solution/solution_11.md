This final problem is a classic application of **Integral Calculus in Kinematics**. When the force is a function of time, we cannot use the standard "constant acceleration" equations. Instead, we must integrate the acceleration to find velocity, and integrate velocity to find position.

### 1. The "Given" & "Find"
* **Mass ($m$):** $3\text{ kg}$
* **Force Field ($\vec{F}$):** $(15t) \hat{i} + (3t - 12) \hat{j} + (-6t^2) \hat{k}$
* **Initial Velocity ($\vec{v}_0$):** $(2, 0, 1)\text{ m/s}$
* **Initial Position ($\vec{r}_0$):** $(5, 2, -3)\text{ m}$
* **Find:** $\vec{v}(t)$ and $\vec{r}(t)$

---

### 2. The Concept: Acceleration ($\vec{a}$)
First, we find the acceleration vector using Newton's Second Law ($\vec{a} = \frac{\vec{F}}{m}$). Since the mass is $3\text{ kg}$, we divide each component of the force by $3$:

* $a_x = \frac{15t}{3} = 5t$
* $a_y = \frac{3t - 12}{3} = t - 4$
* $a_z = \frac{-6t^2}{3} = -2t^2$

**Acceleration Vector:** $\vec{a}(t) = (5t, t - 4, -2t^2)$

---

### 3. Step 1: Finding Velocity ($\vec{v}$)
Velocity is the integral of acceleration: $\vec{v}(t) = \vec{v}_0 + \int_{0}^{t} \vec{a}(t') dt'$.

**The Calculation:**
* **$v_x$:** $2 + \int_{0}^{t} 5t' dt' = 2 + 2.5t^2$
* **$v_y$:** $0 + \int_{0}^{t} (t' - 4) dt' = 0.5t^2 - 4t$
* **$v_z$:** $1 + \int_{0}^{t} -2(t')^2 dt' = 1 - \frac{2}{3}t^3$

**Velocity Result:**
$$\vec{v}(t) = (2.5t^2 + 2) \hat{i} + (0.5t^2 - 4t) \hat{j} + (1 - \frac{2}{3}t^3) \hat{k}$$

---

### 4. Step 2: Finding Position ($\vec{r}$)
Position is the integral of velocity: $\vec{r}(t) = \vec{r}_0 + \int_{0}^{t} \vec{v}(t') dt'$.

**The Calculation:**
* **$x(t)$:** $5 + \int_{0}^{t} (2.5(t')^2 + 2) dt' = 5 + \frac{2.5}{3}t^3 + 2t$
* **$y(t)$:** $2 + \int_{0}^{t} (0.5(t')^2 - 4t') dt' = 2 + \frac{0.5}{3}t^3 - 2t^2$
* **$z(t)$:** $-3 + \int_{0}^{t} (1 - \frac{2}{3}(t')^3) dt' = -3 + t - \frac{2}{12}t^4$ (which simplifies to $-3 + t - \frac{1}{6}t^4$)

---

### 5. Final Result
The time-dependent equations for the particle are:

**Velocity:**
$$\vec{v}(t) = \left( 2.5t^2 + 2, \quad 0.5t^2 - 4t, \quad 1 - \frac{2}{3}t^3 \right) \text{m/s}$$

**Position:**
$$\vec{r}(t) = \left( \frac{5}{6}t^3 + 2t + 5, \quad \frac{1}{6}t^3 - 2t^2 + 2, \quad -\frac{1}{6}t^4 + t - 3 \right) \text{m}$$



**Teaching Tip:** Explain to the class that each integration adds a "constant of integration," which represents the state of the object at $t=0$. This is why the initial velocity and position values are added back into the final polynomial. Notice how the "power" of $t$ increases with each integration—from $t^2$ in force to $t^4$ in position!