To solve this problem, we analyze the wave equation in the form $E(x,t) = E_0 \sin(kx - \omega t)$, where $E_0$ is the amplitude, $k$ is the wave number, and $\omega$ is the angular frequency.

### Given Information

* **Wave Equation:** $E_y(x,t) = 100 \sin(10^7 x - \omega t)$
* **Amplitude ($E_0$):** $100 \text{ V/m}$
* **Wave number ($k$):** $10^7 \text{ rad/m}$
* **Speed of light ($c$):** $\approx 3 \times 10^8 \text{ m/s}$

---

### 1. Direction of Propagation

In the term $(kx - \omega t)$, a **negative sign** between the terms indicates that the wave is traveling in the **positive $x$-direction** ($+x$).

### 2. Angular Frequency ($\omega$)

For an electromagnetic wave in a vacuum, the relationship between angular frequency and wave number is given by $\omega = ck$.


$$\omega = (3 \times 10^8 \text{ m/s}) \times (10^7 \text{ rad/m})$$

$$\omega = 3 \times 10^{15} \text{ rad/s}$$

### 3. Wavelength ($\lambda$)

The wave number $k$ is defined as $k = \frac{2\pi}{\lambda}$. Rearranging to solve for $\lambda$:


$$\lambda = \frac{2\pi}{k} = \frac{2\pi}{10^7 \text{ m}^{-1}}$$

$$\lambda \approx 6.28 \times 10^{-7} \text{ m} \text{ (or } 628 \text{ nm)}$$

### 4. Equation for the Magnetic Field ($B_z$)

The magnetic field $B$ is related to the electric field by $B_0 = \frac{E_0}{c}$.

* **Amplitude:** $B_0 = \frac{100 \text{ V/m}}{3 \times 10^8 \text{ m/s}} \approx 3.33 \times 10^{-7} \text{ T}$.
* **Orientation:** Since the electric field oscillates in the $y$-direction and the wave propagates in the $x$-direction, the magnetic field must oscillate in the $z$-direction (based on the right-hand rule for electromagnetic waves: $\vec{E} \times \vec{B}$ points in the direction of propagation).

The magnetic field equation is:


$$B_z(x,t) = B_0 \sin(kx - \omega t)$$

$$B_z(x,t) = (3.33 \times 10^{-7}) \sin(10^7 x - 3 \times 10^{15} t) \text{ T}$$

---

**Would you like to move on to the next question?**