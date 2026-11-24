# Exercise 2. Formula for a $2 \times 2$ Matrix

**Given:**

$$A = \begin{pmatrix} 3 & 2 \\\\ 5 & 4 \end{pmatrix}$$

---

### Find the Inverse of $A$ Using the Formula for a $2 \times 2$ Matrix, and Check the Result by Computing a Product.

* **Method and Property Used:**
  * **Explicit $2 \times 2$ Matrix Inverse Formula:** A $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$ is invertible if and only if $\det(A) = ad - bc \neq 0$, in which case its inverse is given by swapping the main diagonal entries, negating the off-diagonal entries, and dividing by $\det(A)$:

$$A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$$

  * **Inverse Verification Property:** A computed matrix $B$ is the true inverse of $A$ if and only if $A B = I_2$ and $B A = I_2$.

* **Main steps:**
  * **Step 1 — Compute $\det(A)$ to confirm invertibility:**

$$\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2 \neq 0$$

    Since $\det(A) = 2 \neq 0$, $A^{-1}$ exists.

  * **Step 2 — Apply the $2 \times 2$ inverse formula** ($a = 3, b = 2, c = 5, d = 4$):

$$A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\\\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}$$

* **Result:**

$$A^{-1} = \begin{pmatrix} 2 & -1 \\\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}$$

* **Verification:** Check by computing both products $A A^{-1}$ and $A^{-1} A$:
  * Compute $A A^{-1}$:

$$A A^{-1} = \begin{pmatrix} 3 & 2 \\\\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix} = \begin{pmatrix} (3)(2) + (2)\left(-\frac{5}{2}\right) & (3)(-1) + (2)\left(\frac{3}{2}\right) \\\\ (5)(2) + (4)\left(-\frac{5}{2}\right) & (5)(-1) + (4)\left(\frac{3}{2}\right) \end{pmatrix} = \begin{pmatrix} 6 - 5 & -3 + 3 \\\\ 10 - 10 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

  * Compute $A^{-1} A$:

$$A^{-1} A = \begin{pmatrix} 2 & -1 \\\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix} \begin{pmatrix} 3 & 2 \\\\ 5 & 4 \end{pmatrix} = \begin{pmatrix} (2)(3) + (-1)(5) & (2)(2) + (-1)(4) \\\\ \left(-\frac{5}{2}\right)(3) + \left(\frac{3}{2}\right)(5) & \left(-\frac{5}{2}\right)(2) + \left(\frac{3}{2}\right)(4) \end{pmatrix} = \begin{pmatrix} 6 - 5 & 4 - 4 \\\\ -\frac{15}{2} + \frac{15}{2} & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

  Both products equal $I_2$, confirming $A^{-1}$ is exact.
