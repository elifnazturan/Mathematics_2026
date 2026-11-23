# Exercise 2. Addition and Scalar Multiplication

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix}, \qquad B = \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix}$$

---

### 1. Compute $A + B$, $A - B$, and $3A - 2B$.

* **$A + B$:**

$$A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\ -1 + 0 & 3 + 5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}$$

* **$A - B$:**

$$A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\ -1 - 0 & 3 - 5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}$$

* **$3A - 2B$:**

$$3A - 2B = 3\begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - 2\begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}$$

---

### 2. Explain why addition of matrices is only possible for matrices of the same size.

Matrix addition is performed **entry-by-entry** (elementwise), meaning each entry $(i, j)$ of the first matrix is added to the entry in the exact same row $i$ and column $j$ of the second matrix. For every entry in one matrix to have a matching counterpart in the other matrix, both matrices must have the **same number of rows and the same number of columns** (the same dimensions). If their sizes differ, some entries will have no corresponding position to pair with, so the sum is undefined.

---

> **Purpose of this exercise:** to reinforce entrywise operations and the importance of compatible dimensions.
