This is a classic "trick" physics problem. While it can be solved using a complex infinite series, there is a much simpler logical shortcut involving the total time of the motion.

### 1. The Logical Shortcut (Time-Based Approach)
Instead of calculating every individual trip the fly makes back and forth, we simply need to know two things:
1.  How long does the "event" last?
2.  How fast is the fly moving during that time?

**Step A: Calculate the time until the "crunch"**
The bicycle is 10 meters from the wall and moves at a constant speed of $1\text{ m/s}$.
$$\text{Time } (t) = \frac{\text{Distance}}{\text{Speed}} = \frac{10\text{ m}}{1\text{ m/s}} = \mathbf{10\text{ seconds}}$$
The bicycle will hit the wall in exactly 10 seconds. This is the total time the fly has to stay in the air.

**Step B: Calculate the fly's total distance**
The fly moves at a constant speed of $2\text{ m/s}$ for the entire duration of those 10 seconds (regardless of how many times it turns around).
$$\text{Distance}_{\text{fly}} = \text{Speed}_{\text{fly}} \times \text{Total Time}$$
$$\text{Distance}_{\text{fly}} = 2\text{ m/s} \times 10\text{ s} = \mathbf{20\text{ meters}}$$

---

### 2. The Series Approach (For Context)
If you were to calculate this as a series, you would find that the distance of each trip the fly makes decreases geometrically.



* **Trip 1:** Fly meets the wall. Relative speed is $2\text{ m/s}$. Distance is $10\text{ m}$. Time is $5\text{ s}$.
* **Trip 2:** Fly turns back to meet the bicycle. The bicycle has moved $5\text{ m}$, so they are now $5\text{ m}$ apart. Their closing speed is $2 + 1 = 3\text{ m/s}$. Time is $5/3\text{ s}$.
* **Total Distance:** $d = \sum_{n=1}^{\infty} d_n$

The sum of this infinite series will converge exactly to **20 meters**.

---

### 3. Summary Table
| Parameter | Value | Unit |
| :--- | :--- | :--- |
| Initial Distance | $10$ | $\text{m}$ |
| Bicycle Speed | $1$ | $\text{m/s}$ |
| Fly Speed | $2$ | $\text{m/s}$ |
| **Total Time** | **$10$** | **$\text{s}$** |
| **Total Fly Distance** | **$20$** | **$\text{m}$** |

### Physics Insight
The "trick" works because the fly's speed is constant. If the fly's speed changed with every turn, you would be forced to use the series method. Since it is constant, distance is simply the product of speed and the total time elapsed.

Would you like me to build a small interactive "Fly vs. Bicycle" animation in HTML so you can watch the trips get shorter and shorter in real-time?