To solve this, we will apply the fundamental rules of resistor combinations and Ohm's Law.

### Given Information

* **Resistors:** $R_1 = 15\,\Omega$, $R_2 = 30\,\Omega$, $R_3 = 50\,\Omega$
* **Voltage ($V$):** $12\,\text{V}$

---

### Case 1: Series Connection

In a series circuit, the total resistance is simply the sum of individual resistances, and the current is the same through all components.

**1. Equivalent Resistance ($R_{\text{series}}$):**


$$R_{\text{series}} = R_1 + R_2 + R_3$$

$$R_{\text{series}} = 15 + 30 + 50 = 95\,\Omega$$

**2. Total Current ($I_{\text{series}}$):**
Using Ohm's Law ($I = V/R$):


$$I_{\text{series}} = \frac{12\,\text{V}}{95\,\Omega} \approx 0.126\,\text{A} \, (126\,\text{mA})$$

---

### Case 2: Parallel Connection

In a parallel circuit, the reciprocal of the total resistance is the sum of the reciprocals of individual resistances.

**1. Equivalent Resistance ($R_{\text{parallel}}$):**


$$\frac{1}{R_{\text{parallel}}} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}$$

$$\frac{1}{R_{\text{parallel}}} = \frac{1}{15} + \frac{1}{30} + \frac{1}{50}$$


To add these, find a common denominator ($150$):


$$\frac{1}{R_{\text{parallel}}} = \frac{10}{150} + \frac{5}{150} + \frac{3}{150} = \frac{18}{150}$$

$$R_{\text{parallel}} = \frac{150}{18} \approx 8.33\,\Omega$$

**2. Total Current ($I_{\text{parallel}}$):**
Using Ohm's Law:


$$I_{\text{parallel}} = \frac{12\,\text{V}}{8.33\,\Omega} \approx 1.44\,\text{A}$$

---

### Summary Table

| Connection Type | Total Resistance ($R_{\text{eq}}$) | Total Current ($I$) |
| --- | --- | --- |
| **Series** | $95\,\Omega$ | $0.126\,\text{A}$ |
| **Parallel** | $8.33\,\Omega$ | $1.44\,\text{A}$ |

---

**Would you like me to add another circuit problem to your list?**