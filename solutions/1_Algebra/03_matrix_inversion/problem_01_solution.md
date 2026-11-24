# Exercise 1. Definition of the Inverse

**Given:**

$$A = \begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\\\ -1 & 2 \end{pmatrix}$$

---

### Check Without Using a Formula That $B = A^{-1}$ by Computing $AB$ and $BA$ and Relating the Result to the Definition of the Inverse.

* **Method and Property Used:**
  * **Definition of the Matrix Inverse:** An $n \times n$ square matrix $A$ is invertible with inverse $B = A^{-1}$ if and only if multiplying $A$ and $B$ in **both orders** yields the $n \times n$ identity matrix $I_n$:

$$AB = I_n \qquad \text{and} \qquad BA = I_n$$

  * **Matrix Multiplication:** The $(i, j)$-entry of a product $XY$ is the dot product of row $i$ of $X$ with column $j$ of $Y$.

* **Main steps:**
  * **Step 1 — Compute $AB$:**

$$AB = \begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\\\ -1 & 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\\\ (1)(1) + (1)(-1) & (1)(-1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 - 1 & -2 + 2 \\\\ 1 - 1 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

  * **Step 2 — Compute $BA$:**

$$BA = \begin{pmatrix} 1 & -1 \\\\ -1 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\\\ 1 & 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\\\ (-1)(2) + (2)(1) & (-1)(1) + (2)(1) \end{pmatrix} = \begin{pmatrix} 2 - 1 & 1 - 1 \\\\ -2 + 2 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

  * **Step 3 — Relate to the Definition of the Inverse:** Since both $AB = I_2$ and $BA = I_2$ hold directly by multiplication, $B$ satisfies the exact defining condition of the inverse of $A$ (and symmetrically, $A = B^{-1}$).

* **Result:**

$$AB = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2, \qquad BA = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2 \implies B = A^{-1}$$

* **Verification:** Checking determinants and testing on a vector $x = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix}$ confirms the inverse relationship:
  * $\det(A) = (2)(1) - (1)(1) = 1 \neq 0$, so $A$ is invertible, and $\det(B) = (1)(2) - (-1)(-1) = 1 = \frac{1}{\det(A)}$.
  * Applying $A$ to $x = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix}$ gives $Ax = \begin{pmatrix} 10 \\\\ 7 \end{pmatrix}$, and applying $B$ recovers $B(Ax) = \begin{pmatrix} 10 - 7 \\\\ -10 + 14 \end{pmatrix} = \begin{pmatrix} 3 \\\\ 4 \end{pmatrix} = x$.
