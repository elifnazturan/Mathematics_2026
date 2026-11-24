# Exercise 15. Combining Determinant Properties

**Given:**

$$A \text{ and } B \text{ are invertible } 2 \times 2 \text{ matrices with } \det(A) = -2 \text{ and } \det(B) = 3$$

---

### Compute $\det(B^{-1} A^T B)$ Without Finding Matrix Entries, State Each Property Used in Order, and Explain Why the Factors Involving $B$ Cancel Out.

* **Method and Properties Used (in Order):**
  1. **Multiplicative property of determinants:** For square matrices $X, Y, Z$ of the same size, $\det(XYZ) = \det(X)\det(Y)\det(Z)$.
  2. **Determinant of an inverse matrix:** Because $B$ is invertible ($\det(B) = 3 \neq 0$), $\det(B^{-1}) = \frac{1}{\det(B)}$.
  3. **Determinant of a transpose:** Transposing a square matrix leaves its determinant unchanged, so $\det(A^T) = \det(A)$.
  4. **Commutativity of scalar multiplication in $\mathbb{R}$:** Determinants are real numbers, so their scalar factors commute and allow $\frac{1}{\det(B)}$ and $\det(B)$ to cancel.

* **Main steps:**
  * **Step 1 — Split the determinant of the matrix product** using $\det(XYZ) = \det(X)\det(Y)\det(Z)$:

$$\det(B^{-1} A^T B) = \det(B^{-1})\,\det(A^T)\,\det(B)$$

  * **Step 2 — Apply the inverse and transpose determinant rules** ($\det(B^{-1}) = \frac{1}{\det(B)}$ and $\det(A^T) = \det(A)$):

$$\det(B^{-1} A^T B) = \frac{1}{\det(B)} \cdot \det(A) \cdot \det(B)$$

  * **Step 3 — Cancel the scalar factors involving $B$** ($\det(B) = 3 \neq 0$) and substitute $\det(A) = -2$:

$$\det(B^{-1} A^T B) = \left(\frac{1}{3}\right)(-2)(3) = -2$$

* **Result:**

$$\det(B^{-1} A^T B) = -2$$

* **Why the Factors Involving $B$ Cancel Out:**
  * Even though matrix multiplication is non-commutative (so $B^{-1} A^T B \neq A^T$ as matrices in general), taking the determinant converts each matrix factor into a **nonzero real number** ($\det(B^{-1}) = \frac{1}{3}$ and $\det(B) = 3$).
  * In $\mathbb{R}$, multiplication is commutative and associative, so $\frac{1}{\det(B)} \cdot \det(A) \cdot \det(B) = \left(\frac{1}{\det(B)} \cdot \det(B)\right)\det(A) = 1 \cdot \det(A) = \det(A)$. (This illustrates the general similarity invariance property: $\det(B^{-1} M B) = \det(M)$ for any invertible $B$.)

* **Verification:** Test with concrete $2 \times 2$ matrices satisfying $\det(A) = -2$ and $\det(B) = 3$, such as $A = \begin{pmatrix} -2 & 1 \\\\ 0 & 1 \end{pmatrix}$ and $B = \begin{pmatrix} 3 & 0 \\\\ 0 & 1 \end{pmatrix}$:
  * $B^{-1} = \begin{pmatrix} \frac{1}{3} & 0 \\\\ 0 & 1 \end{pmatrix}$ and $A^T = \begin{pmatrix} -2 & 0 \\\\ 1 & 1 \end{pmatrix}$.
  * Compute the product directly:

$$B^{-1} A^T B = \begin{pmatrix} \frac{1}{3} & 0 \\\\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 & 0 \\\\ 1 & 1 \end{pmatrix} \begin{pmatrix} 3 & 0 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -\frac{2}{3} & 0 \\\\ 1 & 1 \end{pmatrix} \begin{pmatrix} 3 & 0 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -2 & 0 \\\\ 3 & 1 \end{pmatrix}$$

  * $\det(B^{-1} A^T B) = (-2)(1) - (0)(3) = -2$, confirming the property-based calculation.
