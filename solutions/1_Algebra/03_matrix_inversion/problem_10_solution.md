# Exercise 10. Inverse of a Diagonal Matrix

**Given:**

$$D = \begin{pmatrix} 2 & 0 & 0 \\\\ 0 & -3 & 0 \\\\ 0 & 0 & 5 \end{pmatrix}, \qquad E = \begin{pmatrix} 2 & 0 & 0 \\\\ 0 & 0 & 0 \\\\ 0 & 0 & 5 \end{pmatrix}$$

---

### 1. Determine Without Using Gauss-Jordan Elimination Which Matrix Is Invertible.

* **Method and Property Used:**
  * **Invertibility Criterion for Diagonal Matrices:** For a diagonal matrix $\text{diag}(d_1, d_2, \dots, d_n)$, the determinant equals the product of its main diagonal entries:

$$\det(\text{diag}(d_1, d_2, \dots, d_n)) = d_1 d_2 \cdots d_n$$

  * Therefore, a diagonal matrix is **invertible if and only if every main diagonal entry is nonzero** ($d_i \neq 0$ for all $i$). If any diagonal entry is zero, an entire row and column are zero, forcing $\det = 0$ and making the matrix singular.

* **Main steps:**
  * **Check matrix $D$:** The main diagonal entries are $2$, $-3$, and $5$, all of which are nonzero:

$$\det(D) = (2)(-3)(5) = -30 \neq 0$$

    Thus, **$D$ is invertible**.

  * **Check matrix $E$:** The $(2,2)$ diagonal entry is $0$ (creating an entire zero row $R_2 = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$):

$$\det(E) = (2)(0)(5) = 0$$

    Thus, **$E$ is not invertible** (singular).

* **Result:**

$$D \text{ is invertible } (\det(D) = -30 \neq 0), \qquad E \text{ is not invertible } (\det(E) = 0)$$

* **Verification:** For any matrix $X$, the second row of $EX$ is $R_2(E) X = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix} X = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$, which can never equal the second row $\begin{pmatrix} 0 & 1 & 0 \end{pmatrix}$ of $I_3$, proving $E^{-1}$ does not exist.

---

### 2. For the Invertible Matrix, Compute Its Inverse and Check the Result by Multiplication.

* **Method and Property Used:**
  * **Diagonal Inverse Rule:** The inverse of an invertible diagonal matrix $\text{diag}(d_1, d_2, d_3)$ is obtained directly by taking the reciprocal of each main diagonal entry:

$$\text{diag}(d_1, d_2, d_3)^{-1} = \text{diag}\left(\frac{1}{d_1}, \frac{1}{d_2}, \frac{1}{d_3}\right)$$

* **Main steps:**
  * Replace each diagonal entry of $D = \text{diag}(2, -3, 5)$ with its multiplicative inverse:
    * $(1,1)$ entry: $\frac{1}{2}$
    * $(2,2)$ entry: $\frac{1}{-3} = -\frac{1}{3}$
    * $(3,3)$ entry: $\frac{1}{5}$

$$D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\\ 0 & -\frac{1}{3} & 0 \\\\ 0 & 0 & \frac{1}{5} \end{pmatrix}$$

* **Result:**

$$D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\\ 0 & -\frac{1}{3} & 0 \\\\ 0 & 0 & \frac{1}{5} \end{pmatrix}$$

* **Verification:** Check by computing both products $D D^{-1}$ and $D^{-1} D$:

$$D D^{-1} = \begin{pmatrix} 2 & 0 & 0 \\\\ 0 & -3 & 0 \\\\ 0 & 0 & 5 \end{pmatrix}\begin{pmatrix} \frac{1}{2} & 0 & 0 \\\\ 0 & -\frac{1}{3} & 0 \\\\ 0 & 0 & \frac{1}{5} \end{pmatrix} = \begin{pmatrix} (2)\left(\frac{1}{2}\right) & 0 & 0 \\\\ 0 & (-3)\left(-\frac{1}{3}\right) & 0 \\\\ 0 & 0 & (5)\left(\frac{1}{5}\right) \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix} = I_3$$

$$D^{-1} D = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\\ 0 & -\frac{1}{3} & 0 \\\\ 0 & 0 & \frac{1}{5} \end{pmatrix}\begin{pmatrix} 2 & 0 & 0 \\\\ 0 & -3 & 0 \\\\ 0 & 0 & 5 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix} = I_3$$

  Both products equal $I_3$, confirming $D^{-1}$ is exact.
