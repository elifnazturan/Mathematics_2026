# Exercise 7. Inverse of a Product

**Given:**

$$A = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\\\ 0 & 3 \end{pmatrix}$$

---

### 1. Compute $(AB)^{-1}$ and $B^{-1}A^{-1}$, and Check Whether the Results Are the Same.

* **Method and Property Used:**
  * **Explicit $2 \times 2$ Matrix Inverse Formula:** For an invertible matrix $M = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$ ($\det(M) = ad - bc \neq 0$), $M^{-1} = \frac{1}{ad - bc}\begin{pmatrix} d & -b \\\\ -c & a \end{pmatrix}$.
  * **Inverse of a Matrix Product ("Socks-and-Shoes" Property):** If $A$ and $B$ are invertible matrices of the same size, then $AB$ is invertible and $(AB)^{-1} = B^{-1}A^{-1}$.

* **Main steps:**
  * **Part A — Compute $(AB)^{-1}$:**
    * First compute the product $AB$:

$$AB = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\\\ 0 & 3 \end{pmatrix} = \begin{pmatrix} (1)(2) + (1)(0) & (1)(0) + (1)(3) \\\\ (0)(2) + (1)(0) & (0)(0) + (1)(3) \end{pmatrix} = \begin{pmatrix} 2 & 3 \\\\ 0 & 3 \end{pmatrix}$$

    * Compute $\det(AB) = (2)(3) - (3)(0) = 6 \neq 0$, and apply the $2 \times 2$ inverse formula:

$$(AB)^{-1} = \frac{1}{6}\begin{pmatrix} 3 & -3 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix}$$

  * **Part B — Compute $B^{-1}A^{-1}$:**
    * Find $A^{-1}$ ($\det(A) = (1)(1) - (1)(0) = 1$):

$$A^{-1} = \frac{1}{1}\begin{pmatrix} 1 & -1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\\\ 0 & 1 \end{pmatrix}$$

    * Find $B^{-1}$ ($\det(B) = (2)(3) - (0)(0) = 6$):

$$B^{-1} = \frac{1}{6}\begin{pmatrix} 3 & 0 \\\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & \frac{1}{3} \end{pmatrix}$$

    * Multiply $B^{-1}$ by $A^{-1}$ in reverse order:

$$B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & \frac{1}{3} \end{pmatrix}\begin{pmatrix} 1 & -1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\\\ (0)(1) + \left(\frac{1}{3}\right)(0) & (0)(-1) + \left(\frac{1}{3}\right)(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix}$$

  * **Comparison:** Both calculations produce the exact same matrix, so $(AB)^{-1} = B^{-1}A^{-1}$.

* **Result:**

$$(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix}$$

* **Verification:** Multiply $(AB)$ by the common result $C = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix}$ to verify $(AB)C = I_2$:

$$(AB)C = \begin{pmatrix} 2 & 3 \\\\ 0 & 3 \end{pmatrix}\begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix} = \begin{pmatrix} 1 + 0 & -1 + 1 \\\\ 0 + 0 & 0 + 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} = I_2$$

---

### 2. Explain the Meaning of the Reversed Order $(AB)^{-1} = B^{-1}A^{-1}$.

* **Explanation and Method Used:**
  * **Operational / Geometric Meaning:** Applying the product $AB$ to a vector $x$ means **first** applying transformation $B$ to $x$, and **then** applying transformation $A$ to $Bx$:

$$(AB)x = A(Bx)$$

  * To undo this two-step process and return to $x$, you must undo the operations in **reverse (last-in, first-out) order**: **first** undo $A$ by applying $A^{-1}$, and **then** undo $B$ by applying $B^{-1}$:

$$(B^{-1}A^{-1})(AB)x = B^{-1}(A^{-1}A)Bx = B^{-1}I_2Bx = B^{-1}Bx = x$$

  * Because matrix multiplication is **not commutative** in general, applying $A^{-1}B^{-1}$ instead would put $B^{-1}$ next to $A$ instead of $B$, failing to cancel adjacent inverses.

* **Result:** The reversed order $B^{-1}A^{-1}$ reflects that undoing a composition of transformations $A(Bx)$ requires undoing the outer (last) transformation $A$ first via $A^{-1}$, and the inner (first) transformation $B$ second via $B^{-1}$.

* **Verification:** Computing $A^{-1}B^{-1}$ for these matrices gives:

$$A^{-1}B^{-1} = \begin{pmatrix} 1 & -1 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} \frac{1}{2} & 0 \\\\ 0 & \frac{1}{3} \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{3} \\\\ 0 & \frac{1}{3} \end{pmatrix} \neq \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\\ 0 & \frac{1}{3} \end{pmatrix} = (AB)^{-1}$$

  This confirms that order reversal is essential whenever $A$ and $B$ do not commute.
