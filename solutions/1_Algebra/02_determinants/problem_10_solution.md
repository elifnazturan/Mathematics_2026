# Exercise 10. Spotting Dependence

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 4 & 6 \\\\ 0 & 1 & 5 \end{pmatrix}$$

---

### 1. Explain Why $\det(A) = 0$ Without Performing a Full Determinant Calculation, and Identify the Specific Relation Between the Rows.

* **Method and Property Used:**
  * **Proportional rows property:** If one row of a square matrix is a scalar multiple of another row ($R_i = c R_j$ for $i \neq j$), the determinant of the matrix is **zero**.
  * **Equivalence via row operations:** Subtracting $c R_j$ from $R_i$ ($R_i \leftarrow R_i - c R_j$) leaves the determinant unchanged and creates an entire row of zeros, and any matrix with a zero row has $\det = 0$.

* **Specific Relation Between the Rows:**
  * Compare Row $1$ and Row $2$:

$$R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}, \qquad R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}$$

  * Every entry in Row $2$ is exactly $2$ times the corresponding entry in Row $1$:

$$R_2 = 2 R_1 \qquad \text{(or equivalently, } 2 R_1 - R_2 = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}\text{)}$$

* **Main steps:**
  * Apply the elementary row operation $R_2 \leftarrow R_2 - 2R_1$, which leaves $\det(A)$ unchanged:

$$\det\begin{pmatrix} 1 & 2 & 3 \\\\ 2 & 4 & 6 \\\\ 0 & 1 & 5 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 & 3 \\\\ 0 & 0 & 0 \\\\ 0 & 1 & 5 \end{pmatrix}$$

  * Expanding along the second row (where every entry is $0$) immediately yields $0$ without computing any $2 \times 2$ minors.

* **Result:**

$$\det(A) = 0 \qquad \text{because } R_2 = 2 R_1$$

* **Verification:** Checking the $2 \times 2$ minors along Row $3$ confirms cancellation:

$$\det(A) = 0 \cdot \det\begin{pmatrix} 2 & 3 \\\\ 4 & 6 \end{pmatrix} - 1 \cdot \det\begin{pmatrix} 1 & 3 \\\\ 2 & 6 \end{pmatrix} + 5 \cdot \det\begin{pmatrix} 1 & 2 \\\\ 2 & 4 \end{pmatrix} = 0 - 1(6 - 6) + 5(4 - 4) = 0$$

---

### 2. Connect This Row Relation to the Non-Invertibility of the Matrix.

* **Explanation and Method Used:** By the **Invertible Matrix Theorem**, for a square matrix $A$, the following statements are logically equivalent:
  1. The rows of $A$ are **linearly dependent** (here $2R_1 - R_2 + 0R_3 = \mathbf{0}$, a nontrivial linear combination giving the zero vector).
  2. Row reduction cannot produce a pivot in every row (Row $2$ reduces to $\begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$, so $\text{rank}(A) = 2 < 3$ and $A$ cannot be reduced to $I_3$).
  3. $\det(A) = 0$.
  4. $A$ is **not invertible** (singular): no matrix $A^{-1}$ exists such that $A A^{-1} = I_3$.

* **Result:** Because $R_2 = 2R_1$, the rows of $A$ are linearly dependent, which forces $\det(A) = 0$ and guarantees that $A$ is **not invertible**.

* **Verification:** Suppose for contradiction that an inverse $A^{-1}$ existed. Taking determinants of $A A^{-1} = I_3$ would give:

$$\det(A)\det(A^{-1}) = \det(I_3) \implies 0 \cdot \det(A^{-1}) = 1 \implies 0 = 1$$

  This contradiction proves no inverse $A^{-1}$ can exist.
