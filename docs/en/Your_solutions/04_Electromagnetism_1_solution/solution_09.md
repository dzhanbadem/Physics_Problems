This problem elevates the Lorentz force calculation from simple multiplication to **vector cross products**. When velocity and magnetic fields are given in component form (using $\hat{i}, \hat{j}, \hat{k}$), we use the determinant method to find the force vector.

---

## Problem Breakdown: Vector Cross Product

### 1. The Concept
The magnetic force on a moving charge is defined by the vector cross product:
$$\vec{F} = q(\vec{v} \times \vec{B})$$
The cross product $\vec{v} \times \vec{B}$ results in a new vector that is perpendicular to both the velocity and the magnetic field.

### 2. The Variables
*   **Charge of a proton ($q$):** $1.6 \times 10^{-19} \text{ C}$
*   **Velocity ($\vec{v}$):** $(2, -4, 1)$
*   **Magnetic Field ($\vec{B}$):** $(1, 2, -1)$

http://googleusercontent.com/image_content/153



### 3. Step 1: Calculating the Cross Product ($\vec{v} \times \vec{B}$)
We set up a determinant to solve for the components:

$$\vec{v} \times \vec{B} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ 2 & -4 & 1 \\ 1 & 2 & -1 \end{vmatrix}$$

**Breaking it down by components:**
*   **$\hat{i}$ component:** $(-4 \cdot -1) - (1 \cdot 2) = 4 - 2 = \mathbf{2}$
*   **$\hat{j}$ component:** $-[(2 \cdot -1) - (1 \cdot 1)] = -[-2 - 1] = \mathbf{3}$
*   **$\hat{k}$ component:** $(2 \cdot 2) - (-4 \cdot 1) = 4 + 4 = \mathbf{8}$

So, the vector result is: $\vec{v} \times \vec{B} = (2\hat{i} + 3\hat{j} + 8\hat{k})$

### 4. Step 2: Finding the Magnitude of the Cross Product
To find the strength of this resultant vector, we use the Pythagorean theorem for 3D space:
$$|\vec{v} \times \vec{B}| = \sqrt{2^2 + 3^2 + 8^2}$$
$$|\vec{v} \times \vec{B}| = \sqrt{4 + 9 + 64} = \sqrt{77} \approx 8.775$$

### 5. Step 3: Calculating the Force Magnitude
Now, multiply the result by the charge of the proton ($q$):
$$F = q \cdot |\vec{v} \times \vec{B}|$$
$$F = (1.6 \times 10^{-19} \text{ C}) \cdot (8.775)$$
$$F \approx 1.40 \times 10^{-18} \text{ N}$$

### 6. Final Result
*   **Magnitude of Magnetic Force:** $1.40 \times 10^{-18} \text{ N}$

---

### Logic Check for your Class:
Explain that even though the velocity and field have values like "2" or "4," the resulting force is tiny because the proton's charge is so small. Also, point out that because the cross product vector is $(2, 3, 8)$, the force is pushing the proton mostly in the **z-direction** ($\hat{k}$), even though its initial velocity was mostly in the x-y plane.

