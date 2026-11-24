# Exercise 4. Gauss-Jordan

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\\\ 3 & 5 \end{pmatrix}$$

---

### 1. Find $A^{-1}$ Using the Gauss-Jordan Method and Show the Augmented Matrix $[A \mid I]$ After Successive Operations.

* **Method and Property Used:**
  * **Gauss-Jordan Elimination on $[A \mid I_2]$:** Adjoin the $2 \times 2$ identity matrix $I_2$ to the right of $A$ to form the augmented matrix $[A \mid I_2]$, then apply elementary row operations until the left block reduces to $I_2$; the right block becomes $A^{-1}$.

* **Main steps:**
  * **Initial augmented matrix $[A \mid I_2]$:**

$$\left[\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\\\ 3 & 5 & 0 & 1 \end{array}\right]$$

  * **Step 1 — Eliminate the $(2,1)$ entry below the first pivot:** Apply $R_2 \leftarrow R_2 - 3R_1$:

$$\left[\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\\\ 3 - 3(1) & 5 - 3(2) & 0 - 3(1) & 1 - 3(0) \end{array}\right] = \left[\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\\\ 0 & -1 & -3 & 1 \end{array}\right]$$

  * **Step 2 — Scale Row $2$ to make the $(2,2)$ pivot equal to $1$:** Apply $R_2 \leftarrow -R_2$:

$$\left[\begin{array}{cc\|cc} 1 & 2 & 1 & 0 \\\\ 0 & 1 & 3 & -1 \end{array}\right]$$

  * **Step 3 — Eliminate the $(1,2)$ entry above the second pivot:** Apply $R_1 \leftarrow R_1 - 2R_2$:

$$\left[\begin{array}{cc\|cc} 1 - 2(0) & 2 - 2(1) & 1 - 2(3) & 0 - 2(-1) \\\\ 0 & 1 & 3 & -1 \end{array}\right] = \left[\begin{array}{cc\|cc} 1 & 0 & -5 & 2 \\\\ 0 & 1 & 3 & -1 \end{array}\right] = [I_2 \mid A^{-1}]$$

* **Result:**

$$A^{-1} = \begin{pmatrix} -5 & 2 \\\\ 3 & -1 \end{pmatrix}$$

* **Verification:** Check using the explicit $2 \times 2$ inverse formula ($\det(A) = (1)(5) - (2)(3) = 5 - 6 = -1$):

$$A^{-1} = \frac{1}{-1}\begin{pmatrix} 5 & -2 \\\\ -3 & 1 \end{pmatrix} = \begin{pmatrix} -5 & 2 \\\\ 3 & -1 \end{pmatrix}$$

  And verify by multiplication:

$$A A^{-1} = \begin{pmatrix} 1 & 2 \\\\ 3 & 5 \end{pmatrix}\begin{pmatrix} -5 & 2 \\\\ 3 & -1 \end{pmatrix} = \begin{pmatrix} -5 + 6 & 2 - 2 \\\\ -15 + 15 & 6 - 5 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

---

### 2. Explain Why Obtaining $I$ on the Left Yields the Inverse of $A$ on the Right.

* **Explanation and Method Used:**
  * Every elementary row operation corresponds to left-multiplying the augmented matrix $[A \mid I]$ by an invertible **elementary matrix** $E_k$.
  * Applying a sequence of row operations $E_1, E_2, \dots, E_m$ simultaneously to both blocks transforms $[A \mid I]$ into $[E A \mid E I] = [E A \mid E]$, where $E = E_m \cdots E_2 E_1$ is the product of all elementary matrices.
  * Equivalently, solving $[A \mid I]$ solves two linear systems $A x^{(1)} = e_1$ and $A x^{(2)} = e_2$ at once, whose solution columns form $X = \begin{pmatrix} x^{(1)} & x^{(2)} \end{pmatrix}$ satisfying $A X = I$.
  * Therefore, when the left block becomes $E A = I$, the accumulated transformation matrix $E$ on the right block satisfies $E A = I$ (and for square matrices, $A E = I$), which by definition means $E = A^{-1}$.

* **Result:** Because the same sequence of row operations (left-multiplication by $E$) turns $A$ into $E A = I_2$, it turns $I_2$ into $E I_2 = E = A^{-1}$.

* **Verification:** Forming $E = E_3 E_2 E_1$ from the three elementary
