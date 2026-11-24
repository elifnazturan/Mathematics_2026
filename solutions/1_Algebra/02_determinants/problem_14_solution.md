# Exercise 14. System of Equations and Determinant

**Given:**

$$A x = b, \qquad \text{where } A = \begin{pmatrix} 1 & 2 \\\\ k & 4 \end{pmatrix}$$

---

### 1. For Which Values of $k$ Does the System Have a Unique Solution for Every Right-Hand Side $b$?

* **Method and Property Used:**
  * By the **Invertible Matrix Theorem** (and **Cramer's Rule**), a square linear system $Ax = b$ has a **unique solution for every** right-hand side vector $b \in \mathbb{R}^2$ if and only if $A$ is invertible, which holds if and only if $\det(A) \neq 0$.

* **Main steps:**
  * Compute $\det(A)$:

$$\det(A) = \det\begin{pmatrix} 1 & 2 \\\\ k & 4 \end{pmatrix} = (1)(4) - (2)(k) = 4 - 2k$$

  * Require $\det(A) \neq 0$:

$$4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2$$

* **Result:**

$$k \neq 2 \qquad (\text{all } k \in \mathbb{R} \setminus \{2\})$$

* **Verification:** When $k \neq 2$, $A^{-1}$ exists and equals:

$$A^{-1} = \frac{1}{4 - 2k}\begin{pmatrix} 4 & -2 \\\\ -k & 1 \end{pmatrix}$$

  Multiplying any $b = \begin{pmatrix} b_1 \\\\ b_2 \end{pmatrix}$ on the left by $A^{-1}$ produces the single, well-defined solution $x = A^{-1}b$.

---

### 2. For the Remaining Value of $k$, Give an Example of $b$ With Infinitely Many Solutions and an Example of $b$ With No Solution.

* **Method and Property Used:**
  * For the remaining value $k = 2$, $\det(A) = 0$ and the matrix becomes $A = \begin{pmatrix} 1 & 2 \\\\ 2 & 4 \end{pmatrix}$, whose second row is $2$ times its first row ($R_2 = 2R_1$).
  * Writing $b = \begin{pmatrix} b_1 \\\\ b_2 \end{pmatrix}$, the system $x_1 + 2x_2 = b_1$ and $2x_1 + 4x_2 = b_2$ is **consistent (infinitely many solutions)** if and only if $b_2 = 2b_1$, and **inconsistent (no solution)** if and only if $b_2 \neq 2b_1$.

* **Main steps:**
  * Substitute $k = 2$ and form the augmented matrix $\left[\begin{array}{cc|c} 1 & 2 & b_1 \\\\ 2 & 4 & b_2 \end{array}\right]$, then apply $R_2 \leftarrow R_2 - 2R_1$:

$$\left[\begin{array}{cc|c} 1 & 2 & b_1 \\\\ 2 & 4 & b_2 \end{array}\right] \sim \left[\begin{array}{cc|c} 1 & 2 & b_1 \\\\ 0 & 0 & b_2 - 2b_1 \end{array}\right]$$

  * **Case A — Infinitely many solutions ($b_2 = 2b_1$):** Choose $b_1 = 3$, so $b_2 = 2(3) = 6$, giving $b = \begin{pmatrix} 3 \\\\ 6 \end{pmatrix}$.
  * **Case B — No solution ($b_2 \neq 2b_1$):** Choose $b_1 = 3$ and $b_2 = 5$ ($5 \neq 6$), giving $b = \begin{pmatrix} 3 \\\\ 5 \end{pmatrix}$.

* **Result:**
  * **Remaining value:** $k = 2$.
  * **Example of $b$ with infinitely many solutions:** $b = \begin{pmatrix} 3 \\\\ 6 \end{pmatrix}$.
  * **Example of $b$ with no solution:** $b = \begin{pmatrix} 3 \\\\ 5 \end{pmatrix}$.

* **Verification:**
  * For $b = \begin{pmatrix} 3 \\\\ 6 \end{pmatrix}$: the reduced system is $x_1 + 2x_2 = 3$ and $0 = 0$. Setting $x_2 = t \in \mathbb{R}$ gives $x = \begin{pmatrix} 3 - 2t \\\\ t \end{pmatrix}$, which satisfies $A x = \begin{pmatrix} (3 - 2t) + 2t \\\\ 2(3 - 2t) + 4t \end{pmatrix} = \begin{pmatrix} 3 \\\\ 6 \end{pmatrix}$ for every real $t$ (infinitely many solutions).
  * For $b = \begin{pmatrix} 3 \\\\ 5 \end{pmatrix}$: the second row gives $0x_1 + 0x_2 = 5 - 2(3) = -1$, i.e., $0 = -1$, a contradiction confirming no solution exists.
