To derive the differential equation for a series RLC circuit, we apply Kirchhoff’s Voltage Law (KVL), which states that the sum of the potential drops around a closed loop must equal the source voltage.

### The Differential Equation for an RLC Circuit

For a series circuit with a source $V(t)$, the sum of the voltages across the inductor ($L$), resistor ($R$), and capacitor ($C$) is:


$$L \frac{dI}{dt} + RI + V_C = V(t)$$

Since current is the rate of change of charge ($I = \frac{dq}{dt}$) and the voltage across the capacitor is $V_C = \frac{q}{C}$, we can express the entire equation in terms of charge ($q$):


$$L \frac{d^2q}{dt^2} + R \frac{dq}{dt} + \frac{1}{C}q = V(t)$$

---

### Comparison to a Damped Harmonic Oscillator

A mechanical damped harmonic oscillator (like a mass $m$ on a spring with constant $k$ and damping coefficient $b$) is described by Newton's Second Law:


$$m \frac{d^2x}{dt^2} + b \frac{dx}{dt} + kx = F(t)$$

When you compare these two equations, you can see they are mathematically identical in form:

| Physical System | Inertia/Storage | Damping/Resistance | Restoring Force | Driver |
| --- | --- | --- | --- | --- |
| **RLC Circuit** | $L$ (Inductance) | $R$ (Resistance) | $1/C$ (Capacitance) | $V(t)$ |
| **Mechanical Oscillator** | $m$ (Mass) | $b$ (Damping) | $k$ (Spring Constant) | $F(t)$ |

---

### Key Analogies

* **Inductance ($L$) vs. Mass ($m$):** Both represent the "inertia" of the system. $L$ opposes changes in current, just as $m$ opposes changes in velocity.
* **Resistance ($R$) vs. Damping ($b$):** Both represent energy dissipation. In the circuit, $R$ turns electrical energy into heat; in the mechanical system, $b$ (often air resistance or friction) turns kinetic energy into heat.
* **Reciprocal Capacitance ($1/C$) vs. Spring Constant ($k$):** Both represent a restoring force. A capacitor stores energy in an electric field and "pushes back" against charge, similar to how a spring stores potential energy and pushes back against displacement.
* **Voltage ($V$) vs. Force ($F$):** Both act as the "driver" or external influence that sets the system in motion.

---

**Would you like to explore how these analogies affect the resonant frequency of the circuit?**