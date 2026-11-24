# Exercise 9. Matrix Equation

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 3 & 1 \\\\ 2 & 4 \end{pmatrix}$$

---

### Decide Which Side of $AX = B$ Must Be Multiplied by $A^{-1}$, Solve for $X$, and Check the Result by Computing $AX$.

* **Method and Property Used:**
  * **Order of Matrix Multiplication (Left-Cancellation):** Matrix multiplication is **not commutative** in general. Because $A$ stands on the **left** of $X$ in $AX = B$, we must multiply both sides on the **left** by $A^{-1}$ so that $A^{-1}$ sits directly adjacent to $A$:

$$A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies I_2 X = A^{-1}B \implies X = A^{-1}B$$

    *(Multiplying on the right instead would yield $AXA^{-1} = BA^{-1}$, which does not isolate $X$.)*
  * **Explicit $2 \times 2$ Inverse Formula:** For $A = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$ with $\det(A) = ad - bc \neq 0$, $A^{-1} = \frac{1}{ad - bc}\begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$.

* **Main steps:**
  * **Step 1 — State the side for $A^{-1}$:** Multiply both sides of $AX = B$ on the **left** by $A^{-1}$ to obtain $X = A^{-1}B$.
  * **Step 2 — Compute $\det(A)$ and find $A^{-1}$:**

$$\det(A) = (1)(1) - (2)(0) = 1 - 0 = 1 \neq 0$$

$$A^{-1} = \frac{1}{1}\begin{pmatrix} 1 & -2 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\\\ 0 & 1 \end{pmatrix}$$

  * **Step 3 — Compute $X = A^{-1}B$:**

$$X = A^{-1}B = \begin{pmatrix} 1 & -2 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 3 & 1 \\\\ 2 & 4 \end{pmatrix} = \begin{pmatrix} (1)(3) + (-2)(2) & (1)(1) + (-2)(4) \\\\ (0)(3) + (1)(2) & (0)(1) + (1)(4) \end{pmatrix} = \begin{pmatrix} 3 - 4 & 1 - 8 \\\\ 0 + 2 & 0 + 4 \end{pmatrix} = \begin{pmatrix} -1 & -7 \\\\ 2 & 4 \end{pmatrix}$$

* **Result:**
  * **Side of application:** Multiply on the **left** by $A^{-1}$ ($X = A^{-1}B$).
  * **Solution matrix:**

$$X = \begin{pmatrix} -1 & -7 \\\\ 2 & 4 \end{pmatrix}$$

* **Verification:** Compute the product $AX$ directly and compare it with $B$:

$$AX = \begin{pmatrix} 1 & 2 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} -1 & -7 \\\\ 2 & 4 \end{pmatrix} = \begin{pmatrix} (1)(-1) + (2)(2) & (1)(-7) + (2)(4) \\\\ (0)(-1) + (1)(2) & (0)(-7) + (1)(4) \end{pmatrix} = \begin{pmatrix} -1 + 4 & -7 + 8 \\\\ 0 + 2 & 0 + 4 \end{pmatrix} = \begin{pmatrix} 3 & 1 \\\\ 2 & 4 \end{pmatrix} = B$$

  Since $AX = B$ holds identically, $X$ is confirmed to be the exact solution.
