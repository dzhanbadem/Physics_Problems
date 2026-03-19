To determine if Alice and Bob collide or how close they get, we must analyze their positions as functions of time.

### 1. Collision Analysis (Same Place, Same Time)
For a **collision** to occur, Alice and Bob must be at the same coordinates at the same time $t$. We set $A(t) = B(t)$:

**Horizontal (x) match:**
$$2 + t = 2t - 1$$
$$t = 3$$

**Vertical (y) match:**
$$8 - 3t = 2t + 2$$
$$6 = 5t$$
$$t = 1.2$$

**Conclusion on Collision:** Since the $x$-coordinates only match at $t=3$ and the $y$-coordinates only match at $t=1.2$, **they do not collide.** They cross each other's paths, but at different times.

---

### 2. Path Intersection (Same Place, Different Times)
To see if their **paths** cross (even if they aren't there at the same time), we use different variables for time: $A(t_1)$ and $B(t_2)$.
1. $2 + t_1 = 2t_2 - 1 \implies t_1 = 2t_2 - 3$
2. $8 - 3t_1 = 2t_2 + 2$

Substitute (1) into (2):
$$8 - 3(2t_2 - 3) = 2t_2 + 2$$
$$8 - 6t_2 + 9 = 2t_2 + 2$$
$$17 - 2 = 8t_2 \implies t_2 = 1.875, t_1 = 0.75$$
Their paths **do** intersect at the point $P = (2.75, 5.75)$, but Alice arrives there at $t=0.75$ and Bob arrives at $t=1.875$.

---

### 3. Minimum Distance Analysis
Since they don't collide, we find the distance $D(t)$ between them at any time $t$:
$$\vec{D}(t) = B(t) - A(t) = ( (2t-1) - (2+t) , (2t+2) - (8-3t) )$$
$$\vec{D}(t) = (t - 3, 5t - 6)$$

The squared distance $f(t) = D^2$ is:
$$f(t) = (t-3)^2 + (5t-6)^2$$
$$f(t) = (t^2 - 6t + 9) + (25t^2 - 60t + 36)$$
$$f(t) = 26t^2 - 66t + 45$$



**Finding the Minimum:**
Take the derivative and set to zero:
$$f'(t) = 52t - 66 = 0$$
$$t = \frac{66}{52} \approx \mathbf{1.27 \text{ s}}$$

**Calculating the Minimum Distance:**
Substitute $t \approx 1.27$ back into the distance components:
* $\Delta x = 1.27 - 3 = -1.73$
* $\Delta y = 5(1.27) - 6 = 0.35$

$$D_{min} = \sqrt{(-1.73)^2 + (0.35)^2} \approx \mathbf{1.76 \text{ units}}$$

---

### Summary Table
| Metric | Result |
| :--- | :--- |
| **Collision?** | No |
| **Time of Closest Approach** | $1.27 \text{ s}$ |
| **Minimum Distance** | $1.76 \text{ units}$ |
| **Path Intersection Point** | $(2.75, 5.75)$ |

Would you like me to create an interactive HTML visualization for this "Near Miss" scenario so you can see Alice and Bob moving on your GitHub project?