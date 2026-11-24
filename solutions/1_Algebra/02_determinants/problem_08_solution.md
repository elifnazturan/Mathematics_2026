# Exercise 8. Determinant of a Product

**Given:**

$$A, B \text{ are } n \times n \text{ square matrices with } \det(A) = 3 \text{ and } \det(B) = -5$$

---

### 1. Compute $\det(AB)$, $\det(BA)$, and (If It Exists) $\det(A^{-1}B)$.

* **Method and Property Used:**
  * **Multiplicative property of determinants:** For any two square matrices $A$ and $B$ of the same size, $\det(AB) = \det(A)\det(B)$.
  * **Determinant of an inverse matrix:** A square matrix $A$ is invertible if and only if $\det(A) \neq 0$, in which case $\det(A^{-1}) = \frac{1}{\det(A)}$.

* **Compute $\det(AB)$:**
  * *Main steps:*

$$\det(AB) = \det(A)\det(B) = (3)(-5)$$

  * *Result:*

$$\det(AB) = -15$$

* **Compute $\det(BA)$:**
  * *Main steps:*

$$\det(BA) = \det(B)\det(A) = (-5)(3)$$

  * *Result:*

$$\det(BA) = -15$$

* **Compute $\det(A^{-1}B)$:**
  * *Existence check:* Since $\det(A) = 3 \neq 0$, the inverse $A^{-1}$ exists, so $A^{-1}B$ is well-defined and $\det(A^{-1}) = \frac{1}{\det(A)} = \frac{1}{3}$.
  * *Main steps:*

$$\det(A^{-1}B) = \det(A^{-1})\det(B) = \frac{1}{\det(A)}\det(B) = \frac{1}{3}(-5)$$

  * *Result:*

$$\det(A^{-1}B) = -\frac{5}{3}$$

* **Verification:** Test with concrete $2 \times 2$ matrices having $\det(A) = 3$ and $\det(B) = -5$, such as $A = \begin{pmatrix} 3 & 1 \\\\ 0 & 1 \end{pmatrix}$ and $B = \begin{pmatrix} 1 & 0 \\\\ 2 & -5 \end{pmatrix}$:
  * $AB = \begin{pmatrix} 5 & -5 \\\\ 2 & -5 \end{pmatrix} \implies \det(AB) = (5)(-5) - (-5)(2) = -25 + 10 = -15$.
  * $BA = \begin{pmatrix} 3 & 1 \\\\ 6 & -3 \end{pmatrix} \implies \det(BA) = (3)(-3) - (1)(6) = -9 - 6 = -15$.
  * $A^{-1} = \frac{1}{3}\begin{pmatrix} 1 & -1 \\\\ 0 & 3 \end{pmatrix}$, so $A^{-1}B = \frac{1}{3}\begin{pmatrix} -1 & 5 \\\\ 6 & -15 \end{pmatrix} \implies \det(A^{-1}B) = \frac{1}{9}(15 - 30) = -\frac{15}{9} = -\frac{5}{3}$.

---

### 2. Explain Why the First Two Results Are Equal Even Though Usually $AB \neq BA$.

* **Explanation and Method Used:** Although matrix multiplication is **not commutative** in general ($AB \neq BA$ as matrices), the determinant maps each square matrix to a **real number** (scalar), and multiplication of real numbers **is commutative**:

$$\det(AB) = \det(A)\det(B) = \det(B)\det(A) = \det(BA)$$

  Therefore, $AB$ and $BA$ can have completely different entries yet still share the exact same determinant.

* **Result:** $\det(AB) = \det(BA) = -15$ because $\det(A)\det(B) = (3)(-5) = (-5)(3) = \det(B)\det(A)$ in $\mathbb{R}$.

* **Verification:** In the concrete check above, $AB = \begin{pmatrix} 5 & -5 \\\\ 2 & -5 \end{pmatrix} \neq \begin{pmatrix} 3 & 1 \\\\ 6 & -3 \end{pmatrix} = BA$, confirming $AB \neq BA$ while both have determinant $-15$.
