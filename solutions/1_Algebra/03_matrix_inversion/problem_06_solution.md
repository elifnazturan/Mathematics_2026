# Exercise 6. Solving a System Using an Inverse

**Given:**

$$A x = b, \qquad \text{where } A = \begin{pmatrix} 2 & 1 \\\\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 5 \\\\ 7 \end{pmatrix}$$

---

### Solve $Ax = b$ Using $x = A^{-1}b$, Then Substitute the Resulting Vector Back Into the Equation and Check the Result.

* **Method and Property Used:**
  * **Solving a Linear System via Matrix Inversion:** When $A$ is invertible ($\det(A) \neq 0$), left-multiplying both sides of $Ax = b$ by $A^{-1}$ yields the unique solution $x = A^{-1}b$.
  * **Explicit $2 \times 2$ Inverse Formula:** For $A = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$, $A^{-1} = \frac{1}{ad - bc}\begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$.

* **Main steps:**
  * **Step 1 — Compute $\det(A)$ and find $A^{-1}$:**

$$\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0$$

$$A^{-1} = \frac{1}{5}\begin{pmatrix} 3 & -1 \\\\ -1 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\\\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix}$$

  * **Step 2 — Compute $x = A^{-1}b$:**

$$x = A^{-1}b = \frac{1}{5}\begin{pmatrix} 3 & -1 \\\\ -1 & 2 \end{pmatrix}\begin{pmatrix} 5 \\\\ 7 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} (3)(5) + (-1)(7) \\\\ (-1)(5) + (2)(7) \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 15 - 7 \\\\ -5 + 14 \end{pmatrix} = \begin{pmatrix} \frac{8}{5} \\\\ \frac{9}{5} \end{pmatrix}$$

* **Result:**

$$x = \begin{pmatrix} \frac{8}{5} \\\\ \frac{9}{5} \end{pmatrix} \qquad \left(x_1 = \frac{8}{5}, \quad x_2 = \frac{9}{5}\right)$$

* **Verification:** Substitute $x = \begin{pmatrix} \frac{8}{5} \\\\ \frac{9}{5} \end{pmatrix}$ back into the original equation $Ax = b$:

$$A x = \begin{pmatrix} 2 & 1 \\\\ 1 & 3 \end{pmatrix}\begin{pmatrix} \frac{8}{5} \\\\ \frac{9}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\\\ 1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \end{pmatrix} = \begin{pmatrix} \frac{16}{5} + \frac{9}{5} \\\\ \frac{8}{5} + \frac{27}{5} \end{pmatrix} = \begin{pmatrix} \frac{25}{5} \\\\ \frac{35}{5} \end{pmatrix} = \begin{pmatrix} 5 \\\\ 7 \end{pmatrix} = b$$

  Since $Ax = b$ holds identically, the solution vector is verified.
