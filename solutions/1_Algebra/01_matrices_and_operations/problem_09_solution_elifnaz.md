# Exercise 9. Composition of Transformations

**Given:**

$$S = \begin{pmatrix} 2 & 0 \\\\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\\\ 1 & 0 \end{pmatrix}, \qquad x = \begin{pmatrix} 1 \\\\ 2 \end{pmatrix}$$

---

### 1. Compute $R(Sx)$ and $S(Rx)$.

* **Method and Property Used:** Multiplying a matrix by a vector applies a linear transformation to that vector. A composition of two transformations is evaluated inside-out: $R(Sx)$ first applies horizontal scaling $S$ (multiplying the $x$-coordinate by $2$ and keeping the $y$-coordinate fixed) and then applies a $90^\circ$ counterclockwise rotation $R$; $S(Rx)$ first rotates by $90^\circ$ counterclockwise and then scales horizontally by $2$.

* **Compute $R(Sx)$:**
  * *Main steps:* First compute $Sx$, then multiply the resulting vector by $R$:

$$Sx = \begin{pmatrix} 2 & 0 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 \\\\ 2 \end{pmatrix} = \begin{pmatrix} 2(1) + 0(2) \\\\ 0(1) + 1(2) \end{pmatrix} = \begin{pmatrix} 2 \\\\ 2 \end{pmatrix}$$

$$R(Sx) = \begin{pmatrix} 0 & -1 \\\\ 1 & 0 \end{pmatrix}\begin{pmatrix} 2 \\\\ 2 \end{pmatrix} = \begin{pmatrix} 0(2) + (-1)(2) \\\\ 1(2) + 0(2) \end{pmatrix}$$

  * *Result:*

$$R(Sx) = \begin{pmatrix} -2 \\\\ 2 \end{pmatrix}$$

  * *Verification:* Scaling $\binom{1}{2}$ horizontally by $2$ gives $\binom{2}{2}$. Rotating $\binom{2}{2}$ by $90^\circ$ counterclockwise maps $(u, v)$ to $(-v, u)$, giving $\binom{-2}{2}$.

* **Compute $S(Rx)$:**
  * *Main steps:* First compute $Rx$, then multiply the resulting vector by $S$:

$$Rx = \begin{pmatrix} 0 & -1 \\\\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 \\\\ 2 \end{pmatrix} = \begin{pmatrix} 0(1) + (-1)(2) \\\\ 1(1) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\\\ 1 \end{pmatrix}$$

$$S(Rx) = \begin{pmatrix} 2 & 0 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} -2 \\\\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2) + 0(1) \\\\ 0(-2) + 1(1) \end{pmatrix}$$

  * *Result:*

$$S(Rx) = \begin{pmatrix} -4 \\\\ 1 \end{pmatrix}$$

  * *Verification:* Rotating $\binom{1}{2}$ by $90^\circ$ counterclockwise gives $\binom{-2}{1}$. Scaling $\binom{-2}{1}$ horizontally by $2$ doubles the first coordinate to $-4$ while keeping the second coordinate $1$, giving $\binom{-4}{1}$.

---

### 2. Compare the Results and Geometric Meaning of Transformation Order.

* **Result:** **$R(Sx) \neq S(Rx)$**, since $\begin{pmatrix} -2 \\\\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\\\ 1 \end{pmatrix}$.
* **Explanation and Method Used:** Composition of linear transformations is generally **noncommutative** because each transformation acts on the current position of the vector, which has already been altered by the first transformation. Geometrically, $S$ stretches space only along the horizontal ($x$-) axis, whereas $R$ rotates the entire plane by $90^\circ$ counterclockwise:
  * In **$R(Sx)$**, the vector $\binom{1}{2}$ is first stretched horizontally to $\binom{2}{2}$ and then rotated $90^\circ$ counterclockwise, turning what was a horizontal stretch into a vertical displacement of length $2$ (with $x$-coordinate $-2$).
  * In **$S(Rx)$**, the vector $\binom{1}{2}$ is first rotated $90^\circ$ counterclockwise to $\binom{-2}{1}$ and then stretched horizontally by $2$, directly doubling the already negative $x$-coordinate $-2$ to $-4$ while leaving the $y$-coordinate at $1$.
* **Verification:** Their first coordinates differ ($-2 \neq -4$) and their second coordinates also differ ($2 \neq 1$), confirming both algebraically and geometrically that the order of transformations changes the final vector.

---

> **Purpose of this exercise:** to interpret matrix products and nested matrix-vector products as compositions of linear transformations and see geometrically why the order of operations matters.
