# Exercise 7. Using Properties Instead of Recomputing

**Given:**

$$A \text{ is a } 3 \times 3 \text{ matrix with } \det(A) = -4$$

---

### 1. Compute $\det(2A)$.

* **Method and Property Used:** For an $n \times n$ matrix $A$ and any scalar $c$, scaling the entire matrix multiplies every row by $c$, so:

$$\det(cA) = c^n \det(A)$$

  Here $n = 3$ and $c = 2$.

* **Main steps:**

$$\det(2A) = 2^3 \det(A) = 8 \cdot (-4)$$

* **Result:**

$$\det(2A) = -32$$

* **Verification:** Testing with a concrete $3 \times 3$ diagonal matrix having $\det(A) = -4$, such as $A = \begin{pmatrix} -4 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}$, gives $2A = \begin{pmatrix} -8 & 0 & 0 \\\\ 0 & 2 & 0 \\\\ 0 & 0 & 2 \end{pmatrix}$ and $\det(2A) = (-8)(2)(2) = -32$.

---

### 2. Compute $\det(A^T)$.

* **Method and Property Used:** **Transposing a square matrix leaves its determinant unchanged**:

$$\det(A^T) = \det(A)$$

* **Main steps:**

$$\det(A^T) = \det(A) = -4$$

* **Result:**

$$\det(A^T) = -4$$

* **Verification:** For the diagonal test matrix $A = \begin{pmatrix} -4 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}$, $A^T = A$, so $\det(A^T) = -4$.

---

### 3. Compute $\det(A^2)$.

* **Method and Property Used:** By the **multiplicative property of determinants** ($\det(AB) = \det(A)\det(B)$), for any positive integer $k$:

$$\det(A^k) = (\det(A))^k$$

  Here $k = 2$.

* **Main steps:**

$$\det(A^2) = \det(A \cdot A) = \det(A)\det(A) = (\det(A))^2 = (-4)^2$$

* **Result:**

$$\det(A^2) = 16$$

* **Verification:** For $A = \begin{pmatrix} -4 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}$, $A^2 = \begin{pmatrix} 16 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}$, whose diagonal product is $(16)(1)(1) = 16$.

---

### 4. Compute $\det(-A)$.

* **Method and Property Used:** Writing $-A = (-1)A$ and applying the scalar-multiple rule $\det(cA) = c^n \det(A)$ with $c = -1$ and $n = 3$:

$$\det(-A) = (-1)^3 \det(A)$$

* **Main steps:**

$$\det(-A) = (-1)^3 \det(A) = (-1)(-4)$$

* **Result:**

$$\det(-A) = 4$$

* **Verification:** For $A = \begin{pmatrix} -4 & 0 & 0 \\\\ 0 & 1 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}$, $-A = \begin{pmatrix} 4 & 0 & 0 \\\\ 0 & -1 & 0 \\\\ 0 & 0 & -1 \end{pmatrix}$, and $\det(-A) = (4)(-1)(-1) = 4$.
