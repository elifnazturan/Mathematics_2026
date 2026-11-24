# Exercise 12. A Parameter Revealed by a Row Operation

**Given:**

$$A(t) = \begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 4 & t \\\\ 0 & 1 & 1 \end{pmatrix}$$

---

### 1. Find All Values of $t$ for Which $A(t)$ Is Not Invertible (Applying $R_2 \leftarrow R_2 - 2R_1$ First).

* **Method and Property Used:**
  * A square matrix is **not invertible** (singular) if and only if its determinant equals zero: $\det(A(t)) = 0$.
  * Adding a scalar multiple of one row to another row ($R_2 \leftarrow R_2 - 2R_1$) leaves the determinant **unchanged**.

* **Main steps:**
  * Apply $R_2 \leftarrow R_2 - 2R_1$ to $A(t)$:
    * New Row $2$: $\begin{pmatrix} 2 - 2(1) & 4 - 2(2) & t - 2(3) \end{pmatrix} = \begin{pmatrix} 0 & 0 & t - 6 \end{pmatrix}$.
    * Thus:

$$\det(A(t)) = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 0 & t - 6 \\\\ 0 & 1 & 1 \end{pmatrix}$$

  * Expand along the first column (since the $(2,1)$ and $(3,1)$ entries are $0$):

$$\det(A(t)) = 1 \cdot \det\begin{pmatrix} 0 & t - 6 \\\\ 1 & 1 \end{pmatrix} = (0)(1) - (t - 6)(1) = -(t - 6) = 6 - t$$

  * Set $\det(A(t)) = 0$ and solve for $t$:

$$6 - t = 0 \implies t = 6$$

* **Result:**

$$t = 6$$

* **Verification:** Direct cofactor expansion of the original matrix $A(t)$ along the first column gives:

$$\det(A(t)) = 1 \cdot \det\begin{pmatrix} 4 & t \\\\ 1 & 1 \end{pmatrix} - 2 \cdot \det\begin{pmatrix} 2 & 3 \\\\ 1 & 1 \end{pmatrix} + 0 = (4 - t) - 2(2 - 3) = 4 - t + 2 = 6 - t$$

  Setting $6 - t = 0$ yields $t = 6$, matching the row-reduced calculation.

---

### 2. Explain the Special Situation That Occurs in the Rows for This Value of the Parameter.

* **Explanation and Method Used:** When $t = 6$, the row operation $R_2 \leftarrow R_2 - 2R_1$ turns the entire second row into zeros, revealing **linear dependence** among the rows of $A(6)$.

* **Special Row Behavior at $t = 6$:**
  * For $t = 6$, the original second row is $\begin{pmatrix} 2 & 4 & 6 \end{pmatrix}$, which is **exact scalar multiple $2$ times** the first row $\begin{pmatrix} 1 & 2 & 3 \end{pmatrix}$:

$$R_2 = 2 R_1$$

  * Consequently, after $R_2 \leftarrow R_2 - 2R_1$, Row $2$ becomes the zero row $\begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$, so the matrix has only two linearly independent rows ($\text{rank}(A(6)) = 2 < 3$).

* **Result:** At $t = 6$, Row $2$ equals $2$ times Row $1$ ($\begin{pmatrix} 2 & 4 & 6 \end{pmatrix} = 2\begin{pmatrix} 1 & 2 & 3 \end{pmatrix}$), reducing to $\begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$ under $R_2 \leftarrow R_2 - 2R_1$ and making $A(6)$ singular.

* **Verification:** Substituting $t = 6$ gives:

$$A(6) = \begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 4 & 6 \\\\ 0 & 1 & 1 \end{pmatrix}$$

  Since $2R_1 - R_2 + 0R_3 = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$ is a nontrivial linear relation among the rows, $\det(A(6)) = 0$ and $A(6)$ is not invertible.
