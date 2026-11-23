# Exercise 2. Addition and Scalar Multiplication

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\\\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\\\ 0 & 5 \end{pmatrix}$$

---

### 1. Compute A + B, A - B, and 3A - 2B.

* **Method and Properties Used:** Matrix addition, subtraction, and scalar multiplication are performed **entry-by-entry** (elementwise) on matrices of the same size ($2 \times 2$). Scalar multiplication multiplies each entry by the scalar, and subtraction equals adding the additive inverse ($A - B = A + (-1)B$).

* **A + B:**
  * *Main steps:* Add corresponding entries at each position $(i, j)$:

$$A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\\\ -1 + 0 & 3 + 5 \end{pmatrix}$$

  * *Result:*

$$A + B = \begin{pmatrix} 5 & 0 \\\\ -1 & 8 \end{pmatrix}$$

  * *Verification:* By commutativity ($A + B = B + A$), adding $B$ to $A$ gives:

$$\begin{pmatrix} 4 + 1 & -2 + 2 \\\\ 0 + (-1) & 5 + 3 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\\\ -1 & 8 \end{pmatrix}$$

* **A - B:**
  * *Main steps:* Subtract each entry of $B$ from the corresponding entry of $A$:

$$A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\\\ -1 - 0 & 3 - 5 \end{pmatrix}$$

  * *Result:*

$$A - B = \begin{pmatrix} -3 & 4 \\\\ -1 & -2 \end{pmatrix}$$

  * *Verification:* Adding the result back to $B$ gives:

$$(A - B) + B = \begin{pmatrix} -3 + 4 & 4 + (-2) \\\\ -1 + 0 & -2 + 5 \end{pmatrix} = \begin{pmatrix} 1 & 2 \\\\ -1 & 3 \end{pmatrix} = A$$

* **3A - 2B:**
  * *Main steps:* First multiply each matrix by its scalar ($3A$ and $2B$), then subtract entrywise:

$$3A - 2B = 3\begin{pmatrix} 1 & 2 \\\\ -1 & 3 \end{pmatrix} - 2\begin{pmatrix} 4 & -2 \\\\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\\\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\\\ 0 & 10 \end{pmatrix}$$

  * *Result:*

$$3A - 2B = \begin{pmatrix} -5 & 10 \\\\ -3 & -1 \end{pmatrix}$$

  * *Verification:* Checking entry $(1, 2)$ directly gives $3(2) - 2(-2) = 10$, and checking entry $(2, 1)$ gives $3(-1) - 2(0) = -3$, matching the $2 \times 2$ result.

---

### 2. Explain why addition of matrices is only possible for matrices of the same size.

* **Explanation and Method Used:** Matrix addition is defined **entry-by-entry** (elementwise), so the entry in row $i$ and column $j$ of the sum comes from adding entry $(i, j)$ of the first matrix to entry $(i, j)$ of the second matrix.
* **Dimension Requirement and Verification:** Both matrices must have the **same number of rows and columns** so every entry has a matching position. If their sizes differ, some entries lack a counterpart and the sum is undefined; here both $A$ and $B$ are $2 \times 2$, so every position $(i, j)$ exists in both.

---

> **Purpose of this exercise:** to practice entrywise operations, scalar multiplication, result verification, and the requirement of matching matrix dimensions.
