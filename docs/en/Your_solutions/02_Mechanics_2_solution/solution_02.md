For this problem, we move from the gravity-driven pendulum to a mass-spring system. The key here is to compare the given mathematical equation to the standard physical model of Simple Harmonic Motion (SHM).

### 1. The "Given" & "Find"
* **Given Equation:** $x(t) = 0.2 \cos(10\pi t)$
* **Given Mass ($m$):** $10\text{ kg}$
* **Find:** Spring constant ($k$) and Total Mechanical Energy ($E_{total}$)

---

### 2. The Concept
In SHM, the position of an object is described by the general equation:
$$x(t) = A \cos(\omega t)$$

By comparing the given equation to the general one, we can extract:
* **Amplitude ($A$):** $0.2\text{ m}$
* **Angular Frequency ($\omega$):** $10\pi\text{ rad/s}$

We also know the relationship between the mass, the spring constant, and the angular frequency:
$$\omega = \sqrt{\frac{k}{m}}$$



---

### 3. Part A: Solving for the Spring Constant ($k$)
**The Setup:**
To find $k$, we rearrange the angular frequency formula:
$$\omega^2 = \frac{k}{m} \implies k = m\omega^2$$

**The Calculation:**
1.  **Plug in the values:** $k = 10 \times (10\pi)^2$
2.  **Square the frequency:** $(10\pi)^2 = 100\pi^2$
3.  **Finalize:** $k = 10 \times 100\pi^2 = 1000\pi^2$

Using $\pi^2 \approx 9.87$:
$$k \approx 1000 \times 9.87 = 9,870\text{ N/m}$$

---

### 4. Part B: Total Mechanical Energy ($E_{total}$)
**The Concept:**
Total mechanical energy in a spring system is constant and is equal to the maximum potential energy stored in the spring when it is fully stretched (at the amplitude $A$).

**The Setup:**
$$E_{total} = \frac{1}{2} k A^2$$

**The Calculation:**
1.  **Plug in the values:** $E_{total} = \frac{1}{2} (1000\pi^2) (0.2)^2$
2.  **Square the amplitude:** $(0.2)^2 = 0.04$
3.  **Multiply:** $E_{total} = 0.5 \times 1000\pi^2 \times 0.04$
4.  **Simplify:** $E_{total} = 20\pi^2$

Using $\pi^2 \approx 9.87$:
$$E_{total} \approx 20 \times 9.87 = 197.4\text{ J}$$

---

### 5. The Result
* **Spring Constant ($k$):** **$1000\pi^2\text{ N/m}$** (or approx. **$9,870\text{ N/m}$**)
* **Total Energy ($E_{total}$):** **$20\pi^2\text{ J}$** (or approx. **$197.4\text{ J}$**)

**Teaching Tip:** Remind your class that the "Total Energy" remains the same throughout the oscillation; it just converts back and forth between potential energy (at the ends) and kinetic energy (in the middle).

