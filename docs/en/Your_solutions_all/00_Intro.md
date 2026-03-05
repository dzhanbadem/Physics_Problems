```python
import numpy as np

# Vector Algebra
a = np.array([2, 1, -3])
b = np.array([4, -2, 1])

# a) Magnitudes
mag_a = np.linalg.norm(a)
mag_b = np.linalg.norm(b)

# b) Dot product
dot_product = np.dot(a, b)

# c) Cross product
cross_product = np.cross(a, b)

# d) Angle
cos_theta = dot_product / (mag_a * mag_b)
angle_rad = np.arccos(cos_theta)
angle_deg = np.degrees(angle_rad)

# System of Equations
# 2x + 3y = 12
# 1x - 1y = 1
coeff_matrix = np.array([[2, 3], [1, -1]])
const_matrix = np.array([12, 1])
solution = np.linalg.solve(coeff_matrix, const_matrix)

print(f"{mag_a=}")
print(f"{mag_b=}")
print(f"{dot_product=}")
print(f"{cross_product=}")
print(f"{angle_rad=}")
print(f"{angle_deg=}")
print(f"{solution=}")



```

```text
mag_a=3.7416573867739413
mag_b=4.58257569495584
dot_product=3
cross_product=array([ -5, -14,  -8])
angle_rad=1.3949275767021716
angle_deg=79.92346287144585
solution=array([3., 2.])


```

## 1. Vector Algebra

Given vectors: $\vec{a} = [2, 1, -3]$ and $\vec{b} = [4, -2, 1]$.

### a) Magnitude of each vector

The magnitude of a vector $\vec{v} = [x, y, z]$ is calculated as $|\vec{v}| = \sqrt{x^2 + y^2 + z^2}$.

* **Magnitude of $\vec{a}$:**

$$|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2} = \sqrt{4 + 1 + 9} = \sqrt{14} \approx 3.7417$$


* **Magnitude of $\vec{b}$:**

$$|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2} = \sqrt{16 + 4 + 1} = \sqrt{21} \approx 4.5826$$



### b) Dot product $\vec{a} \cdot \vec{b}$

The dot product is calculated as $\vec{a} \cdot \vec{b} = a_x b_x + a_y b_y + a_z b_z$.

$$\vec{a} \cdot \vec{b} = (2 \times 4) + (1 \times -2) + (-3 \times 1)$$

$$\vec{a} \cdot \vec{b} = 8 - 2 - 3 = 3$$

### c) Cross product $\vec{a} \times \vec{b}$

The cross product is calculated using the determinant of a matrix:


$$\vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & -3 \\ 4 & -2 & 1 \end{vmatrix}$$

$$\vec{a} \times \vec{b} = [(1)(1) - (-3)(-2)]\mathbf{i} - [(2)(1) - (-3)(4)]\mathbf{j} + [(2)(-2) - (1)(4)]\mathbf{k}$$

$$\vec{a} \times \vec{b} = [1 - 6]\mathbf{i} - [2 + 12]\mathbf{j} + [-4 - 4]\mathbf{k}$$

$$\vec{a} \times \vec{b} = [-5, -14, -8]$$

### d) Angle between vectors $\vec{a}$ and $\vec{b}$

The angle $\theta$ is found using the formula $\cos(\theta) = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}| |\vec{b}|}$.

$$\cos(\theta) = \frac{3}{\sqrt{14} \cdot \sqrt{21}} = \frac{3}{\sqrt{294}} \approx 0.17496$$

$$\theta = \arccos(0.17496) \approx 1.3949 \text{ radians or } 79.92^\circ$$

---

## 2. Systems of Equations

Solve the system:

1. $2x + 3y = 12$
2. $x - y = 1$

**Step 1: Express $x$ in terms of $y$ using equation (2):**


$$x = y + 1$$

**Step 2: Substitute $x$ into equation (1):**


$$2(y + 1) + 3y = 12$$

$$2y + 2 + 3y = 12$$

$$5y + 2 = 12$$

$$5y = 10$$

$$y = 2$$

**Step 3: Solve for $x$:**


$$x = 2 + 1 = 3$$

**Solution:**


$$x = 3, y = 2$$
