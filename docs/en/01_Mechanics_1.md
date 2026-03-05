This section covers core concepts of kinematics, vector calculus, and dynamics. Here are the step-by-step solutions to your Mechanics I problems.

---

## 1. Projectile Motion

Given: $v_0 = 100 \text{ m/s}$, $\theta = 37^\circ$. (Note: $\sin(37^\circ) \approx 0.6$, $\cos(37^\circ) \approx 0.8$, $g \approx 9.8 \text{ m/s}^2$).

* **Differential Equations:**
In the horizontal ($x$) and vertical ($y$) directions:

$$\frac{d^2x}{dt^2} = 0 \quad \text{and} \quad \frac{d^2y}{dt^2} = -g$$


* **Time of Flight ($T$):** Set $y(t) = (v_0 \sin \theta)t - \frac{1}{2}gt^2 = 0$.

$$T = \frac{2v_0 \sin \theta}{g} = \frac{2(100)(0.6)}{9.8} \approx 12.24 \text{ s}$$


* **Maximum Height ($H$):** 
$$H = \frac{(v_0 \sin \theta)^2}{2g} = \frac{(60)^2}{19.6} \approx 183.67 \text{ m}$$


* **Range ($R$):**

$$R = \frac{v_0^2 \sin(2\theta)}{g} = \frac{100^2 \sin(74^\circ)}{9.8} \approx 980.9 \text{ m}$$



---

## 2. Range Optimization

To find the maximum of $R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$, we take the derivative with respect to $\theta$ and set it to zero:


$$\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot \cos(2\theta) \cdot 2 = 0$$


This implies $\cos(2\theta) = 0$. Since $2\theta$ must be $90^\circ$ for a physical launch, $\theta = 45^\circ$.

---

## 3. Path Intersection

Alice: $(2+t, 8-3t)$, Bob: $(2t-1, 2t+2)$.

* **Intersection of paths:** Set $x_A = x_B \Rightarrow 2+t = 2s-1$ and $y_A = y_B \Rightarrow 8-3t = 2s+2$.
From the first: $t = 2s-3$. Substitute into the second: $8-3(2s-3) = 2s+2 \Rightarrow 8-6s+9 = 2s+2 \Rightarrow 15 = 8s \Rightarrow s = 1.875, t = 0.75$.
The paths intersect at $(2.75, 5.75)$.
* **Collision?** No. For a collision, they must be at the same point at the *same time* ($t=s$). Since $0.75 \neq 1.875$, they do not collide.
* **Minimum Distance:** Minimize $D^2(t) = (x_A-x_B)^2 + (y_A-y_B)^2 = (3-t)^2 + (6-5t)^2$.
$f(t) = 26t^2 - 66t + 45$. Derivative $52t - 66 = 0 \Rightarrow t \approx 1.27 \text{ s}$.
**Minimum distance** $\approx \sqrt{3.04} \approx 1.74 \text{ units}$.

---

## 4. Vector Calculus

$\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$

* **Velocity:** $\vec{v}(t) = \frac{d\vec{r}}{dt} = (6t)\hat{i} + (5 - 16t)\hat{j}$
* **Acceleration:** $\vec{a}(t) = \frac{d\vec{v}}{dt} = 6\hat{i} - 16\hat{j}$

---

## 5. Relative Velocity

To go directly North, the Eastward component of the boat's velocity must cancel the river's flow.
$v_{boat} \sin \theta = v_{river} \Rightarrow 5 \sin \theta = 2 \Rightarrow \theta = \arcsin(0.4) \approx 23.58^\circ$ **West of North**.

* **Resultant Velocity North:** $v_y = 5 \cos(23.58^\circ) \approx 4.58 \text{ m/s}$.
* **Time:** $t = \frac{200}{4.58} \approx 43.67 \text{ s}$.

---

## 6. Variable Velocity

$v(t) = t^2 + 2t - 5$

* **Acceleration at $t=3$:** $a(t) = \frac{dv}{dt} = 2t + 2$. At $t=3$, $a = 2(3)+2 = 8 \text{ m/s}^2$.
* **Position at $t=3$:** $x(t) = \int (t^2+2t-5) dt = \frac{1}{3}t^3 + t^2 - 5t + C$.
Given $x(0)=4 \Rightarrow C=4$.
$x(3) = \frac{1}{3}(27) + 9 - 15 + 4 = 9 + 9 - 15 + 4 = 7$.

---

## 7. Elimination of Time

$x=2t^2 \Rightarrow t^2 = x/2$.
$y=3t^3 \Rightarrow y = 3(t^2)^{3/2} = 3(x/2)^{3/2}$.
**Equation:** $y^2 = \frac{27}{8}x^3$.

* **$\vec{v}(t)$:** $(4t, 9t^2)$; **$|\vec{v}(t)|$:** $\sqrt{16t^2 + 81t^4}$.
* **$\vec{a}(t)$:** $(4, 18t)$; **$|\vec{a}(t)|$:** $\sqrt{16 + 324t^2}$.
* **Constant acceleration?** No, it depends on $t$.

---

## 8. Circular Motion

$v = \frac{2\pi R}{T}$. $R = 6,378,000 \text{ m}$, $T = 86,400 \text{ s}$.
$a_c = \frac{v^2}{R} = \frac{4\pi^2 R}{T^2} = \frac{4\pi^2(6,378,000)}{(86,400)^2} \approx 0.0337 \text{ m/s}^2$.

---

## 9. Momentum Comparison ($p = mv$)

* **Fly:** $p = (0.002 \text{ kg})(10 \text{ m/s}) = 0.02 \text{ kg}\cdot\text{m/s}$.
* **Tennis Ball:** $p = (0.060 \text{ kg})(1 \text{ m/s}) = 0.06 \text{ kg}\cdot\text{m/s}$.
The **tennis ball** has greater momentum.

---

## 10. Kinematics (3D)

$\vec{r}(t) = (a \cos\omega t, b \sin\omega t, bt)$

* **a) Trajectory:** Since $\frac{x^2}{a^2} + \frac{y^2}{b^2} = \cos^2\omega t + \sin^2\omega t = 1$, the projection on the $xy$-plane is an ellipse. The $z$-component increases linearly ($z = bt$). This describes an **elliptical helix**.
* **b) Path Length ($s$):**
$\vec{v}(t) = (-a\omega \sin\omega t, b\omega \cos\omega t, b)$
$|\vec{v}(t)| = \sqrt{a^2\omega^2\sin^2\omega t + b^2\omega^2\cos^2\omega t + b^2}$
$s = \int_0^{t_0} \sqrt{a^2\omega^2\sin^2\omega t + b^2\omega^2\cos^2\omega t + b^2} dt$.
* **c) Special Case:** If $a=b$, the trajectory is a **circular helix**.


