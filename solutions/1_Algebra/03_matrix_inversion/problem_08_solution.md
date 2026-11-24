# Exercise 8. Inverse of a Transformation

**Given:**

$$S = \begin{pmatrix} 2 & 0 \\\\ 0 & \frac{1}{2} \end{pmatrix}$$

---

### 1. Find $S^{-1}$ and Explain What the Inverse Transformation Does Geometrically.

* **Method and Property Used:**
  * **Diagonal Matrix Inverse Rule:** A diagonal matrix $D = \begin{pmatrix} d_1 & 0 \\\\ 0 & d_2 \end{pmatrix}$ with $d_1, d_2 \neq 0$ is invertible, and its inverse is obtained by taking the reciprocal of each diagonal entry:

$$D^{-1} = \begin{pmatrix} \frac{1}{d_1} & 0 \\\\ 0 & \frac{1}{d_2} \end{pmatrix}$$

  * **Geometric Interpretation of Diagonal Scaling:** Applying $D = \begin{pmatrix} d_1 & 0 \\\\ 0 & d_2 \end{pmatrix}$ to $\begin{pmatrix} x \\\\ y \end{pmatrix}$ yields $\begin{pmatrix} d_1 x \\\\ d_2 y \end{pmatrix}$, scaling the $x$-coordinate by $d_1$ and the $y$-coordinate by $d_2$.

* **Main steps:**
  * **Step 1 — Compute $\det(S)$ to confirm invertibility:**

$$\det(S) = (2)\left(\frac{1}{2}\right) - (0)(0) = 1 \neq 0$$

  * **Step 2 — Compute $S^{-1}$:**

$$S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & \frac{1}{1/2} \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & 2 \end{pmatrix}$$

  * **Step 3 — Geometric Explanation:**
    * The original transformation $S\begin{pmatrix} x \\\\ y \end{pmatrix} = \begin{pmatrix} 2x \\\\ \frac{1}{2}y \end{pmatrix}$ **stretches** the plane horizontally by a factor of $2$ (along the $x$-axis) and **compresses** it vertically by a factor of $\frac{1}{2}$ (along the $y$-axis).
    * The inverse transformation $S^{-1}\begin{pmatrix} x \\\\ y \end{pmatrix} = \begin{pmatrix} \frac{1}{2}x \\\\ 2y \end{pmatrix}$ undoes both scalings simultaneously: it **compresses** horizontally by a factor of $\frac{1}{2}$ (halving the $x$-coordinate) and **stretches** vertically by a factor of $2$ (doubling the $y$-coordinate).

* **Result:**

$$S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & 2 \end{pmatrix}$$

  Geometrically, $S^{-1}$ compresses horizontally by $\frac{1}{2}$ and stretches vertically by $2$, reversing the horizontal stretch ($2$) and vertical compression ($\frac{1}{2}$) of $S$.

* **Verification:** Check that $S S^{-1} = I_2$ and $S^{-1} S = I_2$:

$$S S^{-1} = \begin{pmatrix} 2 & 0 \\\\ 0 & \frac{1}{2} \end{pmatrix}\begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2, \qquad S^{-1} S = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & 2 \end{pmatrix}\begin{pmatrix} 2 & 0 \\\\ 0 & \frac{1}{2} \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

---

### 2. Check the Effect of the Pair $(S, S^{-1})$ on a Single Simple Vector.

* **Method and Property Used:** Apply $S$ followed by $S^{-1}$ (and $S^{-1}$ followed by $S$) to a simple test vector $v \in \mathbb{R}^2$ to verify that $S^{-1}(Sv) = v$ and $S(S^{-1}v) = v$.

* **Main steps:**
  * Choose the simple vector $v = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix}$.
  * **Apply $S$ to $v$:**

$$w = S v = \begin{pmatrix} 2 & 0 \\\\ 0 & \frac{1}{2} \end{pmatrix}\begin{pmatrix} 3 \\\\ 4 \end{pmatrix} = \begin{pmatrix} 2(3) \\\\ \frac{1}{2}(4) \end{pmatrix} = \begin{pmatrix} 6 \\\\ 2 \end{pmatrix}$$

    *(Horizontally stretched from $3$ to $6$, vertically compressed from $4$ to $2$.)*

  * **Apply $S^{-1}$ to the transformed vector $w = Sv$:**

$$S^{-1}(S v) = S^{-1} w = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & 2 \end{pmatrix}\begin{pmatrix} 6 \\\\ 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(6) \\\\ 2(2) \end{pmatrix} = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix} = v$$

    *(Horizontally compressed from $6$ back to $3$, vertically stretched from $2$ back to $4$.)*

* **Result:**

$$v = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix} \xrightarrow{\;S\;} \begin{pmatrix} 6 \\\\ 2 \end{pmatrix} \xrightarrow{\;S^{-1}\;} \begin{pmatrix} 3 \\\\ 4 \end{pmatrix}$$

* **Verification:** Reversing the order on the same vector $v = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix}$ also restores $v$:

$$S(S^{-1}v) = \begin{pmatrix} 2 & 0 \\\\ 0 & \frac{1}{2} \end{pmatrix}\begin{pmatrix} \frac{3}{2} \\\\ 8 \end{pmatrix} = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix} = v$$
