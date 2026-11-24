# Exercise 3. When Does the Inverse Not Exist?

**Given:**

$$A = \begin{pmatrix} 2 & 4 \\\\ 1 & 2 \end{pmatrix}$$

---

### Explain in Two Ways Why $A^{-1}$ Does Not Exist: Using the Determinant and Using Dependence Between Rows.

* **Method and Property Used:**
  * **Way 1 — Determinant Criterion for Invertibility:** A square matrix $A$ is invertible if and only if $\det(A) \neq 0$. If $\det(A) = 0$, $A$ is singular and $A^{-1}$ does not exist (and the $2 \times 2$ inverse formula $\frac{1}{\det(A)}\begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$ would require division by zero).
  * **Way 2 — Linear Dependence of Rows (Invertible Matrix Theorem):** An $n \times n$ matrix $A$ is invertible if and only if its rows are linearly independent (equivalently, row reduction yields $n$ pivots and reduces $A$ to $I_n$). If one row is a scalar multiple of another, row reduction produces a zero row and no inverse exists.

* **Main steps:**
  * **Way 1 — Using the Determinant:**
    * Compute $\det(A)$:

$$\det(A) = \det\begin{pmatrix} 2 & 4 \\\\ 1 & 2 \end{pmatrix} = (2)(2) - (4)(1) = 4 - 4 = 0$$

    * Since $\det(A) = 0$, $A$ is singular and $A^{-1}$ does not exist.

  * **Way 2 — Using Dependence Between the Rows:**
    * Compare Row $1 = \begin{pmatrix} 2 & 4 \end{pmatrix}$ and Row $2 = \begin{pmatrix} 1 & 2 \end{pmatrix}$:

$$R_1 = 2 R_2 \qquad \left(\text{or equivalently, } R_1 - 2 R_2 = \begin{pmatrix} 0 & 0 \end{pmatrix}\right)$$

    * Because Row $1$ is a scalar multiple of Row $2$, the rows are **linearly dependent**. Applying $R_1 \leftarrow R_1 - 2R_2$ reduces $A$ to $\begin{pmatrix} 0 & 0 \\\\ 1 & 2 \end{pmatrix}$, which has only $1$ pivot ($< 2$) and can never be row-reduced to $I_2$.

  * **Connection Between Both Explanations:** Row dependence ($R_1 = 2R_2$) directly forces $\det(A) = 0$, so both conditions describe the exact same collapse of rank ($\text{rank}(A) = 1 < 2$).

* **Result:**

$$A^{-1} \text{ does not exist because } \det(A) = 0 \text{ and the rows of } A \text{ are linearly dependent } (R_1 = 2R_2).$$

* **Verification:** Suppose for contradiction that an inverse $B = \begin{pmatrix} x & y \\\\ z & w \end{pmatrix}$ existed such that $A B = I_2$:

$$\begin{pmatrix} 2 & 4 \\\\ 1 & 2 \end{pmatrix} \begin{pmatrix} x & y \\\\ z & w \end{pmatrix} = \begin{pmatrix} 2x + 4z & 2y + 4w \\\\ x + 2z & y + 2w \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix}$$

  Comparing the first-column entries requires both $x + 2z = 0$ and $2(x + 2z) = 1$, which gives $2(0) = 1 \implies 0 = 1$, a contradiction proving no inverse $A^{-1}$ can exist.
