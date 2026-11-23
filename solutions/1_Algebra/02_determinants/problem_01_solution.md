# Exercise 1. Determinant of a $2 \times 2$ Matrix

**Given:**

$$A = \begin{pmatrix} 3 & -2 \\\\ 5 & 4 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 7 \\\\ 2 & 14 \end{pmatrix}$$

---

### 1. Compute $\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ and $\det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$.

* **Method and Property Used:** For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by the product of the main diagonal entries minus the product of the anti-diagonal entries:

$$\det \begin{pmatrix} a & b \\\\ c & d \end{pmatrix} = ad - bc$$

* **Compute $\det(A)$:**
  * *Main steps:* Multiply the main diagonal ($3 \cdot 4$) and subtract the anti-diagonal product ($(-2) \cdot 5$):

$$\det \begin{pmatrix} 3 & -2 \\\\ 5 & 4 \end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10$$

  * *Result:*

$$\det \begin{pmatrix} 3 & -2 \\\\ 5 & 4 \end{pmatrix} = 22$$

  * *Verification:* $(3)(4) = 12$ and $(-2)(5) = -10$; subtracting $-10$ from $12$ adds $10$, giving $22$.

* **Compute $\det(B)$:**
  * *Main steps:* Multiply the main diagonal ($1 \cdot 14$) and subtract the anti-diagonal product ($7 \cdot 2$):

$$\det \begin{pmatrix} 1 & 7 \\\\ 2 & 14 \end{pmatrix} = (1)(14) - (7)(2) = 14 - 14$$

  * *Result:*

$$\det \begin{pmatrix} 1 & 7 \\\\ 2 & 14 \end{pmatrix} = 0$$

  * *Verification:* Notice that the second row of $B$ is $2$ times the first row ($(2, 14) = 2(1, 7)$), so the rows are linearly dependent and the determinant is $0$.

---

### 2. Which Matrix Is Invertible? Justify Your Answer.

* **Result:** Matrix $A = \begin{pmatrix} 3 & -2 \\\\ 5 & 4 \end{pmatrix}$ is **invertible**, whereas matrix $B = \begin{pmatrix} 1 & 7 \\\\ 2 & 14 \end{pmatrix}$ is **not invertible** (singular).
* **Explanation and Method Used:** A square matrix is invertible if and only if its determinant is **nonzero** ($\det \neq 0$):
  * Since $\det(A) = 22 \neq 0$, $A$ is invertible.
  * Since $\det(B) = 0$, $B$ is not invertible.
* **Verification:** For a $2 \times 2$ matrix with $\det(A) \neq 0$, the inverse is given by $\frac{1}{\det(A)}\begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$:

$$A^{-1} = \frac{1}{22}\begin{pmatrix} 4 & 2 \\\\ -5 & 3 \end{pmatrix}$$

  Multiplying gives:

$$A A^{-1} = \frac{1}{22}\begin{pmatrix} 3 & -2 \\\\ 5 & 4 \end{pmatrix}\begin{pmatrix} 4 & 2 \\\\ -5 & 3 \end{pmatrix} = \frac{1}{22}\begin{pmatrix} 12 + 10 & 6 - 6 \\\\ 20 - 20 & 10 + 12 \end{pmatrix} = \frac{1}{22}\begin{pmatrix} 22 & 0 \\\\ 0 & 22 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix}$$

  This confirms $A$ is invertible, while $\det(B) = 0$ prevents dividing by $\det(B)$ to form $B^{-1}$.

---

> **Purpose of this exercise:** to introduce the simplest determinant calculation and immediately connect it to invertibility.
