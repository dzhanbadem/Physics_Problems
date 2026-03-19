To find the dimensions of the rectangle with the maximum area, we use calculus to model the area as a function of a single variable and then find its stationary point.

### 1. Modeling the Rectangle
Since the rectangle is in the **first quadrant** and lies under the curve $y = 3 - x^2$:
* One vertex of the rectangle is at the origin $(0, 0)$.
* The opposite vertex lies on the curve at some point $(x, y)$.
* The **Width** of the rectangle is $x$.
* The **Height** of the rectangle is $y = 3 - x^2$.



---

### 2. The Area Function
The area $A$ of a rectangle is the product of its width and height:
$$A = x \cdot y$$
Substitute the equation for the curve:
$$A(x) = x(3 - x^2) = 3x - x^3$$

**Constraints:** Since the rectangle is in the first quadrant, $x$ must be between $0$ and the x-intercept of the curve ($\sqrt{3} \approx 1.732$).

---

### 3. Finding the Maximum Area
To find the maximum, we take the derivative of the area function with respect to $x$ and set it to zero.

**Step A: Differentiate $A(x)$**
$$A'(x) = \frac{d}{dt}(3x - x^3) = 3 - 3x^2$$

**Step B: Solve for critical points**
Set $A'(x) = 0$:
$$3 - 3x^2 = 0$$
$$3x^2 = 3$$
$$x^2 = 1 \implies x = 1$$
*(We ignore $x = -1$ because we are restricted to the first quadrant).*

**Step C: Find the corresponding Height ($y$)**
Plug $x = 1$ back into the curve equation:
$$y = 3 - (1)^2 = 2$$



---

### 4. Verification (Second Derivative Test)
To ensure this is a maximum, we check the second derivative:
$$A''(x) = -6x$$
At $x = 1$, $A''(1) = -6$. Since the second derivative is negative, the graph is concave down, confirming that $x = 1$ is indeed a **maximum**.

---

### 5. Final Dimensions
The rectangle that yields the maximum area has the following dimensions:
* **Width:** $1$ unit
* **Height:** $2$ units
* **Maximum Area:** $1 \times 2 = \mathbf{2 \text{ square units}}$

### Summary Table
| Parameter | Optimal Value |
| :--- | :--- |
| **x (Width)** | **1** |
| **y (Height)** | **2** |
| **Max Area** | **2** |
| **Curve Range** | $0 \leq x \leq \sqrt{3}$ |

Would you like me to create an interactive HTML visualization for this optimization problem so you can slide the rectangle back and forth and see the area change in real-time?