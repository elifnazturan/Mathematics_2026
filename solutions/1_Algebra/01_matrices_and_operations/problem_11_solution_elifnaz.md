# Exercise 11. When Do Matrices Commute?

**Given:**

$$A = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$$

---

### 1. Find the Conditions on $a, b, c, d$ Such That $AB = BA$.

* **Method and Property Used:** Unlike multiplication of real numbers, matrix multiplication is generally **noncommutative**. For two $2 \times 2$ matrices to commute ($AB = BA$), every corresponding entry of the product matrices $AB$ and $BA$ must be equal, which yields a system of scalar equations in $a, b, c, d$.

* **Main steps:**
  * Compute both products $AB$ and $BA$:

$$AB = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} a & b \\\\ c & d \end{pmatrix} = \begin{pmatrix} a + c & b + d \\\\ c & d \end{pmatrix}$$

$$BA = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a + b \\\\ c & c + d \end{pmatrix}$$

  * Set $AB = BA$ entry by entry:
    * Entry $(1, 1)$: $a + c = a \implies c = 0$.
    * Entry $(1, 2)$: $b + d = a + b \implies d = a$.
    * Entry $(2, 1)$: $c = c$ (always satisfied).
    * Entry $(2, 2)$: $d = c + d \implies c = 0$ (consistent with above).

* **Result:**

$$c = 0 \qquad \text{and} \qquad d = a$$

  while $a$ and $b$ can be any real numbers.

* **Verification:** Substituting $c = 0$ and $d = a$ into both products gives:

$$AB = \begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix}\begin{pmatrix} a & b \\\\ 0 & a \end{pmatrix} = \begin{pmatrix} a & a + b \\\\ 0 & a \end{pmatrix}$$

$$BA = \begin{pmatrix} a & b \\\\ 0 & a \end{pmatrix}\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a + b \\\\ 0 & a \end{pmatrix}$$

  Since $AB = BA$ holds identically for all $a, b \in \mathbb{R}$ when $c = 0$ and $d = a$, the conditions are necessary and sufficient.

---

### 2. Describe the General Form of $B$ Under These Conditions.

* **Explanation and Method Used:** Substituting $c = 0$ and $d = a$ into $B = \begin{pmatrix} a & b \\\\ c & d \end{pmatrix}$ shows that any $2 \times 2$ matrix commuting with $A$ has equal diagonal entries and a zero below-diagonal entry, and can be decomposed into a scalar multiple of the identity matrix plus a scalar multiple of $A$:

$$B = \begin{pmatrix} a & b \\\\ 0 & a \end{pmatrix} = a\begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} + b\begin{pmatrix} 0 & 1 \\\\ 0 & 0 \end{pmatrix} = (a - b)I + bA$$

* **Result:** Every $2 \times 2$ matrix $B$ commuting with $A$ has the upper-triangular equal-diagonal form:

$$B = \begin{pmatrix} a & b \\\\ 0 & a \end{pmatrix}, \qquad a, b \in \mathbb{R}$$

* **Verification:** Notice that both $I$ and $A$ commute with $A$ ($AI = IA = A$ and $A \cdot A = A \cdot A$), and matrix multiplication is linear, so any linear combination $\alpha I + \beta A$ automatically commutes with $A$. Setting $\alpha = a - b$ and $\beta = b$ gives $(a - b)\begin{pmatrix} 1 & 0 \\\\ 0 & 1 \end{pmatrix} + b\begin{pmatrix} 1 & 1 \\\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & b \\\\ 0 & a \end{pmatrix}$.


