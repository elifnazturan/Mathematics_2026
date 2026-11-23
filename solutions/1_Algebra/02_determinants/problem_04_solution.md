# Exercise 4. Triangular Matrix

**Given:**

$$T = \begin{pmatrix} 2 & 4 & 1 \\\\ 0 & -3 & 5 \\\\ 0 & 0 & 7 \end{pmatrix}$$

---

### 1. Compute $\det(T)$ Without Expanding.

* **Method and Property Used:** The determinant of an **upper (or lower) triangular matrix** equals the product of its main diagonal entries, because all entries below (or above) the main diagonal are zero.

* **Main steps:** Multiply the entries along the main diagonal ($2$, $-3$, and $7$):

$$\det \begin{pmatrix} 2 & 4 & 1 \\\\ 0 & -3 & 5 \\\\ 0 & 0 & 7 \end{pmatrix} = (2)(-3)(7) = (-6)(7)$$

* **Result:**

$$\det(T) = -42$$

* **Verification:** Expanding along the first column gives $2 \cdot \det\begin{pmatrix} -3 & 5 \\\\ 0 & 7 \end{pmatrix} - 0 + 0 = 2 \cdot (-3 \cdot 7 - 5 \cdot 0) = 2(-21) = -42$, matching the diagonal product.

---

### 2. State the Rule for an Arbitrary Triangular Matrix and Explain It Using This Example.

* **Method and Property Used:** For an $n \times n$ triangular matrix $U$ (upper or lower triangular), the rule is:

$$\det(U) = u_{11} u_{22} \cdots u_{nn}$$

* **Explanation Using This Example:**
  * In $T = \begin{pmatrix} 2 & 4 & 1 \\\\ 0 & -3 & 5 \\\\ 0 & 0 & 7 \end{pmatrix}$, all entries below the main diagonal are $0$ ($t_{21} = 0$, $t_{31} = 0$, $t_{32} = 0$).
  * When expanding along the first column, only the top-left entry $2$ multiplies a nonzero cofactor determinant, leaving $2 \cdot \det\begin{pmatrix} -3 & 5 \\\\ 0 & 7 \end{pmatrix}$.
  * In that remaining $2 \times 2$ block, the entry below its main diagonal is also $0$, so expanding along its first column leaves only $(-3) \cdot \det\begin{pmatrix} 7 \end{pmatrix} = (-3)(7)$.
  * Cascading through the zeros below the diagonal leaves only the diagonal entries multiplied together: $2 \cdot (-3) \cdot 7$.

* **Result:** For any triangular matrix, the determinant is the **product of its diagonal entries**, which for $T$ is $(2)(-3)(7) = -42$.

* **Verification:** Since $\det(T) = -42 \neq 0$ (and none of the diagonal entries $2, -3, 7$ is zero), the triangular matrix $T$ is invertible.
