## 3. Path Intersection

Alice: $(2+t, 8-3t)$, Bob: $(2t-1, 2t+2)$.

* **Intersection of paths:** Set $x_A = x_B \Rightarrow 2+t = 2s-1$ and $y_A = y_B \Rightarrow 8-3t = 2s+2$.
From the first: $t = 2s-3$. Substitute into the second: $8-3(2s-3) = 2s+2 \Rightarrow 8-6s+9 = 2s+2 \Rightarrow 15 = 8s \Rightarrow s = 1.875, t = 0.75$.
The paths intersect at $(2.75, 5.75)$.
* **Collision?** No. For a collision, they must be at the same point at the *same time* ($t=s$). Since $0.75 \neq 1.875$, they do not collide.
* **Minimum Distance:** Minimize $D^2(t) = (x_A-x_B)^2 + (y_A-y_B)^2 = (3-t)^2 + (6-5t)^2$.
$f(t) = 26t^2 - 66t + 45$. Derivative $52t - 66 = 0 \Rightarrow t \approx 1.27 \text{ s}$.
**Minimum distance** $\approx \sqrt{3.04} \approx 1.74 \text{ units}$.