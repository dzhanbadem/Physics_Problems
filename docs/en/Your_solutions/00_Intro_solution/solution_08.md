Finding the area under a curve is a classic application of the **Fundamental Theorem of Calculus**. Since the function $f(x) = \sin(x)$ is non-negative on the interval $[0, \pi]$, the definite integral will give us the exact area.

---

## Problem: Area under $f(x) = \sin(x)$ from $0$ to $\pi$

### Step 1: Set up the Definite Integral

The area $A$ is defined by the integral:


$$A = \int_{0}^{\pi} \sin(x) \, dx$$

### Step 2: Find the Antiderivative

We need to find a function $F(x)$ such that $F'(x) = \sin(x)$.
Recall that the derivative of $\cos(x)$ is $-\sin(x)$. Therefore, the antiderivative of $\sin(x)$ is:


$$\int \sin(x) \, dx = -\cos(x)$$

### Step 3: Apply the Fundamental Theorem of Calculus

We evaluate the antiderivative at the upper limit ($\pi$) and subtract the evaluation at the lower limit ($0$):


$$A = [-\cos(x)]_{0}^{\pi}$$

This expands to:


$$A = (-\cos(\pi)) - (-\cos(0))$$

### Step 4: Evaluate the Trigonometric Values

Now, we plug in the known values for the cosine function:

* $\cos(\pi) = -1$
* $\cos(0) = 1$

Substitute these back into our area equation:


$$A = (-(-1)) - (-1)$$

$$A = 1 - (-1)$$

$$A = 1 + 1$$

### Final Result:

$$A = 2$$

The total area under one "hump" of the sine curve is exactly **2 square units**.

---

### Tips for your Presentation:

