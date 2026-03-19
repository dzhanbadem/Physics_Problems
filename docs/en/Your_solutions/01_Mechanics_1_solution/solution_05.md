To solve this problem, we use **vector addition** for relative velocity. For the boat to move "directly north," its eastward velocity from its motor must exactly cancel out the river's eastward current.

### 1. Vector Setup
Let:
* $\vec{v}_r = 2 \text{ m/s}$ (Velocity of the river, East)
* $\vec{v}_{b/r} = 5 \text{ m/s}$ (Velocity of the boat relative to the water)
* $\vec{v}_{b/g}$ = Velocity of the boat relative to the ground (This must point **Due North**)



---

### 2. Finding the Heading (Angle)
The boat must aim upstream (to the West) to counteract the current. This forms a right-angled triangle where:
* The **hypotenuse** is the boat's speed ($5 \text{ m/s}$).
* The **opposite side** is the river's speed ($2 \text{ m/s}$).

Using trigonometry:
$$\sin(\theta) = \frac{\text{Opposite}}{\text{Hypotenuse}} = \frac{v_r}{v_{b/r}}$$
$$\sin(\theta) = \frac{2}{5} = 0.4$$
$$\theta = \arcsin(0.4) \approx \mathbf{23.58^\circ}$$

**Direction:** The boat should head **$23.58^\circ$ West of North**.

---

### 3. Finding the Crossing Time
To find the time, we first need the **resultant velocity ($v_{b/g}$)** pointing North. We use the Pythagorean theorem:
$$(v_{b/r})^2 = (v_r)^2 + (v_{b/g})^2$$
$$5^2 = 2^2 + (v_{b/g})^2$$
$$25 = 4 + (v_{b/g})^2 \implies (v_{b/g})^2 = 21$$
$$v_{b/g} = \sqrt{21} \approx \mathbf{4.58 \text{ m/s}}$$

Now, we use the width of the river ($d = 200 \text{ m}$):
$$\text{Time} (t) = \frac{\text{Distance}}{\text{Velocity}_{\text{North}}}$$
$$t = \frac{200 \text{ m}}{4.58 \text{ m/s}} \approx \mathbf{43.67 \text{ s}}$$

---

### 4. Summary Table
| Variable | Value | Unit |
| :--- | :--- | :--- |
| River Speed | $2.0$ | $\text{m/s}$ |
| Boat Speed (Still Water) | $5.0$ | $\text{m/s}$ |
| **Heading Angle** | **$23.58^\circ$** | **West of North** |
| **Resultant Northward Speed**| **$4.58$** | **$\text{m/s}$** |
| **Crossing Time** | **$43.67$** | **seconds** |



Would you like me to build an interactive HTML tool where you can change the river's current speed and see how the boat's "aim" automatically adjusts to stay on course?