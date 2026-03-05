# Problem Set: Mechanics I – Solutions

---

## Task 01 – Projectile Motion

### Problem Statement

A projectile is fired from the ground with an initial velocity of $100 \text{ m/s}$ at an angle of $37^\circ$ above the horizontal. Assume no air resistance.

* Derive the differential equations of motion in the horizontal and vertical directions.
* Determine the time of flight.
* Determine the maximum height.
* Determine the range.

### Theory

Projectile motion is a form of motion experienced by an object or particle that is projected near the Earth's surface and moves along a curved path under the action of gravity only. Neglecting air resistance, the only force acting is gravity, which acts vertically downward.

The initial velocity components are:

$$
v_{0x} = v_0 \cos(\theta)
$$

$$
v_{0y} = v_0 \sin(\theta)
$$

### Step-by-Step Solution

**1. Differential Equations of Motion**

According to Newton's Second Law, $\vec{F} = m\vec{a}$. With gravity as the only force:

$$
\begin{align}
m \frac{d^2x}{dt^2} &= 0 \\
m \frac{d^2y}{dt^2} &= -mg
\end{align}
$$

Thus, the differential equations are:

$$
\frac{d^2x}{dt^2} = 0
$$

$$
\frac{d^2y}{dt^2} = -g
$$

Integrating these with respect to time gives the velocity components, and integrating again gives the position equations:

$$
x(t) = v_0 \cos(\theta) t
$$

$$
y(t) = v_0 \sin(\theta) t - \frac{1}{2}gt^2
$$

**2. Time of Flight ($T$)**

The projectile returns to the ground when $y(t) = 0$:

$$
v_0 \sin(\theta) T - \frac{1}{2}gT^2 = 0
$$

Solving for $T$ (ignoring $T=0$):

$$
T = \frac{2v_0 \sin(\theta)}{g}
$$

Using $v_0 = 100 \text{ m/s}$, $\sin(37^\circ) \approx 0.6$, and $g \approx 9.81 \text{ m/s}^2$:

$$
T = \frac{2(100)(0.6)}{9.81} \approx 12.23 \text{ s}
$$

**3. Maximum Height ($H$)**

Maximum height occurs when the vertical velocity $v_y = 0$:

$$
v_y(t) = v_0 \sin(\theta) - gt = 0 \implies t_{up} = \frac{v_0 \sin(\theta)}{g}
$$

Substituting $t_{up}$ into the $y(t)$ equation:

$$
H = \frac{(v_0 \sin(\theta))^2}{2g}
$$

$$
H = \frac{(100 \times 0.6)^2}{2 \times 9.81} = \frac{3600}{19.62} \approx 183.49 \text{ m}
$$

**4. Range ($R$)**

The range is the horizontal distance traveled at $t = T$:

$$
R = x(T) = v_0 \cos(\theta) \left( \frac{2v_0 \sin(\theta)}{g} \right) = \frac{v_0^2 \sin(2\theta)}{g}
$$

Using $\sin(74^\circ) \approx 0.961$:

$$
R = \frac{100^2 \times 0.961}{9.81} \approx 979.61 \text{ m}
$$



### Final Result

* **Equations:** $\ddot{x} = 0$, $\ddot{y} = -g$
* **Time of Flight:** $\approx 12.23 \text{ s}$
* **Max Height:** $\approx 183.49 \text{ m}$
* **Range:** $\approx 979.61 \text{ m}$

### Interpretation

The motion is a superposition of constant velocity motion in the $x$-direction and constant acceleration motion in the $y$-direction, resulting in a parabolic trajectory.

---

## Task 02 – Range Optimization

### Problem Statement

For projectile motion, show analytically that the maximum range $R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}$ for a given initial velocity is achieved at a launch angle of $45^\circ$.

### Theory

To find the extremum of a function, we take the first derivative with respect to the independent variable and set it to zero.

### Step-by-Step Solution

We start with the range equation:

$$
R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}
$$

To find the angle $\theta$ that maximizes $R$, we calculate $\frac{dR}{d\theta}$:

$$
\frac{dR}{d\theta} = \frac{v_0^2}{g} \frac{d}{d\theta} (\sin(2\theta))
$$

Using the chain rule:

$$
\frac{dR}{d\theta} = \frac{v_0^2}{g} \cdot 2\cos(2\theta)
$$

Set the derivative to zero:

$$
\frac{2v_0^2 \cos(2\theta)}{g} = 0
$$

Since $v_0$ and $g$ are non-zero constants:

$$
\cos(2\theta) = 0
$$

The value for which the cosine is zero in the context of a launch angle ($0 < \theta < 90^\circ$) is:

$$
2\theta = 90^\circ \implies \theta = 45^\circ
$$

To confirm it is a maximum, we check the second derivative:

$$
\frac{d^2R}{d\theta^2} = -\frac{4v_0^2 \sin(2\theta)}{g}
$$

At $\theta = 45^\circ$, $\sin(90^\circ) = 1$, making the second derivative negative, which confirms a local maximum.

### Final Result

The maximum range is achieved when $\theta = 45^\circ$.

---

## Task 03 – Path Intersection

### Problem Statement

Alice moves along $A(t) = (2+t, 8-3t)$ and Bob moves along $B(t) = (2t-1, 2t+2)$. Determine if their paths intersect. If yes, determine when and where they collide. If not, determine the minimum distance and when it occurs.

### Theory

An intersection of paths occurs if there exist times $t_1$ and $t_2$ such that $A(t_1) = B(t_2)$. A collision occurs only if $t_1 = t_2$.

### Step-by-Step Solution

**1. Path Intersection**

We set coordinates equal using different parameters $t$ and $s$:

$$
\begin{align}
2 + t &= 2s - 1 \quad (1) \\
8 - 3t &= 2s + 2 \quad (2)
\end{align}
$$

From (1): $t = 2s - 3$. Substitute into (2):

$$
8 - 3(2s - 3) = 2s + 2
$$

$$
8 - 6s + 9 = 2s + 2 \implies 17 - 6s = 2s + 2 \implies 8s = 15 \implies s = 1.875
$$

Now find $t$:

$$
t = 2(1.875) - 3 = 0.75
$$

The paths intersect. However, since $t \neq s$ ($0.75 \neq 1.875$), they reach the intersection point at different times. No collision occurs.

**2. Minimum Distance**

The distance squared $D^2(t)$ between them at any time $t$ is:

$$
D^2(t) = (x_A - x_B)^2 + (y_A - y_B)^2
$$

$$
D^2(t) = (2+t - (2t-1))^2 + (8-3t - (2t+2))^2
$$

$$
D^2(t) = (3-t)^2 + (6-5t)^2 = (9 - 6t + t^2) + (36 - 60t + 25t^2)
$$

$$
D^2(t) = 26t^2 - 66t + 45
$$

To minimize, find the derivative and set to zero:

$$
\frac{d(D^2)}{dt} = 52t - 66 = 0 \implies t = \frac{66}{52} \approx 1.27 \text{ s}
$$

Substituting $t \approx 1.27$ into $D^2$:

$$
D^2(1.27) = 26(1.27)^2 - 66(1.27) + 45 \approx 3.038
$$

$$
D_{min} = \sqrt{3.038} \approx 1.74 \text{ units}
$$

### Final Result

* **Collision:** No.
* **Time of min distance:** $t \approx 1.27 \text{ s}$.
* **Minimum distance:** $\approx 1.74 \text{ units}$.

---

## Task 04 – Vector Calculus

### Problem Statement

The position of an object is given by $\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}$. Find the object's velocity and acceleration vectors.

### Theory

Velocity is the first derivative of position, and acceleration is the first derivative of velocity (second derivative of position).

$$
\vec{v}(t) = \frac{d\vec{r}}{dt}, \quad \vec{a}(t) = \frac{d\vec{v}}{dt}
$$

### Step-by-Step Solution

Given:

$$
\vec{r}(t) = \begin{pmatrix} 3t^2 \\ 5t - 8t^2 \end{pmatrix}
$$

**1. Velocity Vector**

Differentiate each component with respect to $t$:

$$
v_x = \frac{d}{dt}(3t^2) = 6t
$$

$$
v_y = \frac{d}{dt}(5t - 8t^2) = 5 - 16t
$$

$$
\vec{v}(t) = 6t\hat{i} + (5 - 16t)\hat{j}
$$

**2. Acceleration Vector**

Differentiate the velocity components:

$$
a_x = \frac{d}{dt}(6t) = 6
$$

$$
a_y = \frac{d}{dt}(5 - 16t) = -16
$$

$$
\vec{a}(t) = 6\hat{i} - 16\hat{j}
$$

### Final Result

$$
\vec{v}(t) = (6t, 5-16t)
$$

$$
\vec{a} = (6, -16)
$$

---

## Task 05 – Relative Velocity

### Problem Statement

A river flows east at $2 \text{ m/s}$. A boat moving at $5 \text{ m/s}$ in still water wants to go directly north. Determine the heading angle and travel time for a 200m wide river.

### Theory

The velocity of the boat relative to the ground $\vec{v}_{bg}$ is the sum of the boat's velocity relative to the water $\vec{v}_{bw}$ and the water's velocity relative to the ground $\vec{v}_{wg}$.

$$
\vec{v}_{bg} = \vec{v}_{bw} + \vec{v}_{wg}
$$

For the boat to move directly north, the eastward component of $\vec{v}_{bg}$ must be zero.

### Step-by-Step Solution

Let the heading angle be $\theta$ measured West of North.

**1. Heading Angle**

The components of $\vec{v}_{bw}$ are $(-5\sin\theta, 5\cos\theta)$. The velocity of the river is $(2, 0)$.

$$
\vec{v}_{bg} = (-5\sin\theta + 2)\hat{i} + (5\cos\theta)\hat{j}
$$

Set the $x$-component to zero:

$$
-5\sin\theta + 2 = 0 \implies \sin\theta = 0.4
$$

$$
\theta = \arcsin(0.4) \approx 23.58^\circ
$$

**2. Travel Time**

The northward speed is $v_y = 5\cos(23.58^\circ) \approx 4.58 \text{ m/s}$.

$$
t = \frac{\text{width}}{v_y} = \frac{200}{4.58} \approx 43.67 \text{ s}
$$



### Final Result

* **Heading:** $23.58^\circ$ West of North.
* **Time:** $\approx 43.67 \text{ s}$.

---

## Task 06 – Variable Velocity

### Problem Statement

$v(t) = t^2 + 2t - 5$. If $x(0)=4$, find position and acceleration at $t=3$.

### Theory

$$
x(t) = \int v(t) dt, \quad a(t) = \frac{dv}{dt}
$$

### Step-by-Step Solution

**1. Acceleration**

$$
a(t) = \frac{d}{dt}(t^2 + 2t - 5) = 2t + 2
$$

At $t=3$:

$$
a(3) = 2(3) + 2 = 8 \text{ m/s}^2
$$

**2. Position**

$$
x(t) = \int (t^2 + 2t - 5) dt = \frac{1}{3}t^3 + t^2 - 5t + C
$$

Using $x(0)=4$: $0 + 0 - 0 + C = 4 \implies C = 4$.

$$
x(3) = \frac{1}{3}(3)^3 + (3)^2 - 5(3) + 4 = 9 + 9 - 15 + 4 = 7 \text{ m}
$$

### Final Result

At $t=3$: $x = 7 \text{ m}$ and $a = 8 \text{ m/s}^2$.

---

## Task 07 – Elimination of Time

### Problem Statement

$x(t)=2t^2, y(t)=3t^3$. Eliminate $t$, calculate $\vec{v}, \vec{a}$, and check if $\vec{a}$ is constant.

### Step-by-Step Solution

**1. Eliminate $t$**

From $x = 2t^2$, we have $t^2 = x/2 \implies t = (x/2)^{1/2}$.
Substitute into $y$:

$$
y = 3((x/2)^{1/2})^3 = 3(x/2)^{3/2}
$$

Squared form: $y^2 = \frac{27}{8}x^3$.

**2. Kinematics**

$$
\vec{v}(t) = \left( \frac{dx}{dt}, \frac{dy}{dt} \right) = (4t, 9t^2)
$$

$$
|\vec{v}(t)| = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}
$$

$$
\vec{a}(t) = \left( \frac{dv_x}{dt}, \frac{dv_y}{dt} \right) = (4, 18t)
$$

$$
|\vec{a}(t)| = \sqrt{16 + 324t^2}
$$

**3. Acceleration Check**

The acceleration vector $\vec{a}(t) = (4, 18t)$ depends on time $t$. Therefore, the acceleration is **not constant**.

---

## Task 08 – Circular Motion

### Problem Statement

Calculate centripetal acceleration at Earth's equator ($R = 6378 \text{ km}$).

### Theory

$$
a_c = \frac{v^2}{R} = \omega^2 R = \left( \frac{2\pi}{T} \right)^2 R
$$

### Step-by-Step Solution

$R = 6.378 \times 10^6 \text{ m}$.
$T = 24 \text{ hours} = 86400 \text{ s}$.

$$
a_c = \frac{4\pi^2 (6.378 \times 10^6)}{(86400)^2}
$$

$$
a_c \approx \frac{2.518 \times 10^8}{7.465 \times 10^9} \approx 0.0337 \text{ m/s}^2
$$

### Final Result

$a_c \approx 0.034 \text{ m/s}^2$.

---

## Task 09 – Momentum Comparison

### Problem Statement

Compare $p$ of a 2g fly at 10 m/s vs. 60g ball at 1 m/s.

### Step-by-Step Solution

$$
p = mv
$$

* **Fly:** $p = 0.002 \text{ kg} \times 10 \text{ m/s} = 0.02 \text{ kg}\cdot\text{m/s}$
* **Ball:** $p = 0.060 \text{ kg} \times 1 \text{ m/s} = 0.06 \text{ kg}\cdot\text{m/s}$

The tennis ball has greater momentum.

---

## Task 10 – Kinematics (Elliptical Helix)

### Problem Statement

$\vec{r}(t) = (a \cos(\omega t), b \sin(\omega t), bt)$. Find trajectory and path length.

### Step-by-Step Solution

**1. Trajectory**

From $x = a \cos(\omega t)$ and $y = b \sin(\omega t)$:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = \cos^2(\omega t) + \sin^2(\omega t) = 1
$$

The projection on the $xy$-plane is an ellipse. Since $z = bt$ increases linearly, the path is an **elliptical helix**.

**2. Path Length ($s$)**

$$
\vec{v}(t) = (-a\omega \sin(\omega t), b\omega \cos(\omega t), b)
$$

$$
|\vec{v}(t)| = \sqrt{a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) + b^2}
$$

$$
s = \int_{0}^{t_0} \sqrt{a^2\omega^2\sin^2(\omega t) + b^2\omega^2\cos^2(\omega t) + b^2} dt
$$

If $a=b$, the speed is constant: $|\vec{v}| = \sqrt{a^2\omega^2 + b^2}$.