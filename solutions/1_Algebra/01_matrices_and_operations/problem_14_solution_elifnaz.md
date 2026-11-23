# Exercise 14. Rotation Matrices

**Given:**

$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\\\ \sin\theta & \cos\theta \end{pmatrix}$$

---

### 1. Compute $R(\alpha)R(\beta)$ and Use Angle-Addition Identities to Show $R(\alpha)R(\beta) = R(\alpha + \beta)$.

* **Method and Property Used:** Multiplying two $2 \times 2$ rotation matrices uses row-by-column dot products, followed by the standard **angle-addition identities** for sine and cosine:

$$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$

* **Main steps:**
  * Write the product $R(\alpha)R(\beta)$:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\\\ \sin\alpha & \cos\alpha \end{pmatrix}\begin{pmatrix} \cos\beta & -\sin\beta \\\\ \sin\beta & \cos\beta \end{pmatrix}$$

  * Compute each entry via dot products:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha\cos\beta + (-\sin\alpha)(\sin\beta) & \cos\alpha(-\sin\beta) + (-\sin\alpha)(\cos\beta) \\\\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \sin\alpha(-\sin\beta) + \cos\alpha\cos\beta \end{pmatrix}$$

  * Simplify signs and apply the angle-addition identities:
    * Entry $(1, 1)$: $\cos\alpha\cos\beta - \sin\alpha\sin\beta = \cos(\alpha + \beta)$
    * Entry $(1, 2)$: $-(\sin\alpha\cos\beta + \cos\alpha\sin\beta) = -\sin(\alpha + \beta)$
    * Entry $(2, 1)$: $\sin\alpha\cos\beta + \cos\alpha\sin\beta = \sin(\alpha + \beta)$
    * Entry $(2, 2)$: $\cos\alpha\cos\beta - \sin\alpha\sin\beta = \cos(\alpha + \beta)$

* **Result:**

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha + \beta) & -\sin(\alpha + \beta) \\\\ \sin(\alpha + \beta) & \cos(\alpha + \beta) \end{pmatrix} = R(\alpha + \beta)$$

* **Verification:** Test with $\alpha = \frac{\pi}{2}$ ($90^\circ$ rotation) and $\beta = \frac{\pi}{2}$ ($90^\circ$ rotation):

$$R\!\left(\frac{\pi}{2}\right)R\!\left(\frac{\pi}{2}\right) = \begin{pmatrix} 0 & -1 \\\\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & -1 \\\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} -1 & 0 \\\\ 0 & -1 \end{pmatrix} = R(\pi)$$

  This matches $\cos\pi = -1$ and $\sin\pi = 0$.

---

### 2. Geometric Interpretation of the Result.

* **Explanation and Method Used:** Applying $R(\alpha)R(\beta)$ to a vector $x$ means first rotating $x$ counterclockwise by angle $\beta$ and then rotating the resulting vector counterclockwise by angle $\alpha$.
* **Result:** Rotating first by $\beta$ and then by $\alpha$ has the exact same geometric effect on the plane as a **single counterclockwise rotation by the sum of the angles, $\alpha + \beta$**.
* **Verification:** In the $\alpha = \frac{\pi}{2}, \beta = \frac{\pi}{2}$ check above, two consecutive $90^\circ$ counterclockwise turns move a vector to a $180^\circ$ turn, which is given directly by $R(\pi)$.

---

> **Purpose of this exercise:** to show consistency between matrix algebra and the geometry of composing planar rotations.
