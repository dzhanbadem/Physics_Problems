To find the equivalent resistance between two opposite corners of a cube made of 12 identical resistors (each with resistance $R$), we utilize the **principle of symmetry**.

### The Circuit Analysis

Let the two opposite corners be labeled point **A** (input) and point **B** (output).

1. **Symmetry at Junctions:** When current enters at corner **A**, it splits equally among the 3 edges connected to A. By symmetry, the potential at the three corners adjacent to A must be identical.
2. **Symmetry at the Exit:** Similarly, the current must converge at corner **B**. Because the circuit is symmetric, the three corners adjacent to B must also be at the same potential.

---

### Step-by-Step Solution

We can trace the path of the current through the cube as a series of potential "layers":

* **Layer 1 (The first 3 resistors):** Current enters at A and splits into 3 resistors, each of resistance $R$.
* Equivalent resistance of this layer: $R_1 = \frac{R}{3}$


* **Layer 2 (The middle 6 resistors):** From the first set of nodes, the current flows through 6 parallel paths (the edges of the cube connecting the first set of nodes to the second set of nodes).
* Equivalent resistance of this layer: $R_2 = \frac{R}{6}$


* **Layer 3 (The final 3 resistors):** Finally, the current converges through the 3 resistors connected to the output corner B.
* Equivalent resistance of this layer: $R_3 = \frac{R}{3}$



**Total Equivalent Resistance ($R_{\text{eq}}$):**
Since these layers are in series with one another along the path from A to B:


$$R_{\text{eq}} = R_1 + R_2 + R_3$$

$$R_{\text{eq}} = \frac{R}{3} + \frac{R}{6} + \frac{R}{3}$$

To add these, use a common denominator ($6$):


$$R_{\text{eq}} = \frac{2R}{6} + \frac{1R}{6} + \frac{2R}{6} = \frac{5R}{6}$$

### Final Answer

The equivalent resistance between two opposite corners of the cube is **$\frac{5}{6}R$**.

---

**Does this derivation help clear up the symmetry approach for your presentation, or would you like to discuss another complex network configuration?**