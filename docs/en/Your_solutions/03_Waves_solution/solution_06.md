To solve this, we will use the method of **pattern matching**. We compare the specific wave equation given in the problem to the standard mathematical form of a traveling wave to extract its physical properties.

## 6. Wave Equation Analysis

### The Concept
The standard mathematical model for a displacement wave traveling in the positive x-direction is:
$$y(x,t) = A \sin(kx - \omega t)$$

By looking at the equation provided, $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$, we can identify the following components:
* **Amplitude ($A$):** The multiplier in front of the sine.
* **Wave Number ($k$):** The multiplier of $x$.
* **Angular Frequency ($\omega$):** The multiplier of $t$.

---

### Step-by-Step Execution

#### a) Amplitude ($A$)
The amplitude is the maximum displacement from the equilibrium position. It is simply the coefficient $A$ in the equation.
* **Result:** $A = 0.05\text{ m}$

#### b) Wavelength ($\lambda$)
The wave number $k$ is related to wavelength by the formula $k = \frac{2\pi}{\lambda}$. 
1.  From our equation, we see $k = 2\pi\text{ rad/m}$.
2.  Set them equal: $2\pi = \frac{2\pi}{\lambda}$.
3.  Solve for $\lambda$:
    $$\lambda = 1\text{ m}$$

#### c) Frequency ($f$)
The angular frequency $\omega$ is related to frequency by the formula $\omega = 2\pi f$.
1.  From our equation, we see $\omega = 50\pi\text{ rad/s}$.
2.  Set them equal: $50\pi = 2\pi f$.
3.  Divide both sides by $2\pi$:
    $$f = \frac{50\pi}{2\pi} = 25\text{ Hz}$$

#### d) Wave Speed ($v$)
The speed of the wave can be found using the relationship between frequency and wavelength.
1.  Use the formula: $v = f \lambda$.
2.  Substitute our findings from parts (b) and (c):
    $$v = 25\text{ Hz} \times 1\text{ m}$$
3.  **Result:** $v = 25\text{ m/s}$

---

### Summary Table for Presentation
| Property | Symbol | Calculation | Value |
| :--- | :--- | :--- | :--- |
| **Amplitude** | $A$ | Directly from equation | $0.05\text{ m}$ |
| **Wavelength** | $\lambda$ | $2\pi / k$ | $1\text{ m}$ |
| **Frequency** | $f$ | $\omega / 2\pi$ | $25\text{ Hz}$ |
| **Wave Speed** | $v$ | $f \times \lambda$ | $25\text{ m/s}$ |

> **Pro-Tip for Class:** Point out the **minus sign** inside the sine function $(kx - \omega t)$. This tells us the wave is moving in the **positive x-direction** (to the right). If that sign were a plus, the wave would be moving to the left.


