# Exercise 5. $3 \times 3$ Matrix

**Given:**

$$A = \begin{pmatrix} 1 & 1 & 0 \\\\ 0 & 1 & 1 \\\\ 1 & 0 & 1 \end{pmatrix}$$

---

### Find the Inverse of $A$ Using Gauss-Jordan Elimination and Check the Result by Multiplication.

* **Method and Property Used:**
  * **Gauss-Jordan Elimination on $[A \mid I_3]$:** Form the $3 \times 6$ augmented matrix $[A \mid I_3]$ and apply elementary row operations to transform the left $3 \times 3$ block into the identity matrix $I_3$. Because row operations correspond to left-multiplying by an invertible matrix $E$, reducing $EA = I_3$ transforms the right block into $E I_3 = A^{-1}$.
  * **Inverse Verification Property:** A square matrix $B$ is the inverse of $A$ if and only if $A B = I_3$ and $B A = I_3$.

* **Main steps:**
  * **Initial augmented matrix $[A \mid I_3]$:**

$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\\ 0 & 1 & 1 & 0 & 1 & 0 \\\\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right]$$

  * **Step 1 — Eliminate the $(3,1)$ entry below the $(1,1)$ pivot:** Apply $R_3 \leftarrow R_3 - R_1$:

$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\\ 0 & 1 & 1 & 0 & 1 & 0 \\\\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right]$$

  * **Step 2 — Eliminate the $(3,2)$ entry below the $(2,2)$ pivot:** Apply $R_3 \leftarrow R_3 + R_2$:

$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\\ 0 & 1 & 1 & 0 & 1 & 0 \\\\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right]$$

  * **Step 3 — Scale Row $3$ to make the $(3,3)$ pivot equal to $1$:** Apply $R_3 \leftarrow \frac{1}{2} R_3$:

$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\\ 0 & 1 & 1 & 0 & 1 & 0 \\\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right]$$

  * **Step 4 — Eliminate the $(2,3)$ entry above the $(3,3)$ pivot:** Apply $R_2 \leftarrow R_2 - R_3$:

$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\\\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right]$$

  * **Step 5 — Eliminate the $(1,2)$ entry above the $(2,2)$ pivot:** Apply $R_1 \leftarrow R_1 - R_2$:

$$\left[\begin{array}{ccc|ccc} 1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\\\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right] = [I_3 \mid A^{-1}]$$

* **Result:**

$$A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\\\ \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\\\ -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\\\ 1 & 1 & -1 \\\\ -1 & 1 & 1 \end{pmatrix}$$

* **Verification:** Check by computing both products $A A^{-1}$ and $A^{-1} A$:
  * Compute $A A^{-1}$:

$$A A^{-1} = \frac{1}{2}\begin{pmatrix} 1 & 1 & 0 \\\\ 0 & 1 & 1 \\\\ 1 & 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 & 1 \\\\ 1 & 1 & -1 \\\\ -1 & 1 & 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 + 1 + 0 & -1 + 1 + 0 & 1 - 1 + 0 \\\\ 0 + 1 - 1 & 0 + 1 + 1 & 0 - 1 + 1 \\\\ 1 + 0 - 1 & -1 + 0 + 1 & 1 + 0 + 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 \\\\ 0 & 2 & 0 \\\\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix} = I_3$$

  * Compute $A^{-1} A$:

$$A^{-1} A = \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\\\ 1 & 1 & -1 \\\\ -1 & 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 & 0 \\\\ 0 & 1 & 1 \\\\ 1 & 0 & 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 + 0 + 1 & 1 - 1 + 0 & 0 - 1 + 1 \\\\ 1 + 0 - 1 & 1 + 1 + 0 & 0 + 1 - 1 \\\\ -1 + 0 + 1 & -1 + 1 + 0 & 0 + 1 + 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 \\\\ 0 & 2 & 0 \\\\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix} = I_3$$

  Both products equal $I_3$, confirming $A^{-1}$ is exact.
