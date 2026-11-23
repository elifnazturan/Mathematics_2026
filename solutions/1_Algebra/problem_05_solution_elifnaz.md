# Exercise 5. Matrix Times Vector

**Given:**

$$A = \begin{pmatrix} 2 & -1 \\\\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\\\ 2 \end{pmatrix}$$

---

### 1. Compute $Ax$.

* **Method and Property Used:** Since $A$ is $2 \times 2$ and $x$ is $2 \times 1$, the inner dimensions match ($2 = 2$), so the matrix-vector product $Ax$ is defined and yields a $2 \times 1$ column vector. Each entry of $Ax$ is the dot product of the corresponding row of $A$ with the column vector $x$.
* **Main steps:**

$$Ax = \begin{pmatrix} 2(4) + (-1)(2) \\\\ 1(4) + 3(2) \end{pmatrix} = \begin{pmatrix} 8 - 2 \\\\ 4 + 6 \end{pmatrix}$$

* **Result:**

$$Ax = \begin{pmatrix} 6 \\\\ 10 \end{pmatrix}$$

* **Verification:** Checking each row dot product separately: row $1$ of $A$ is $(2, -1)$, so $(2, -1) \cdot \binom{4}{2} = 2\cdot 4 + (-1)\cdot 2 = 6$; row $2$ of $A$ is $(1, 3)$, so $(1, 3) \cdot \binom{4}{2} = 1\cdot 4 + 3\cdot 2 = 10$.

---

### 2. Express $Ax$ as a Linear Combination of the Columns of $A$.

* **Explanation and Method Used:** Multiplying a matrix $A$ by a column vector $x = \binom{x_1}{x_2}$ is equivalent to taking a **linear combination of the columns of $A$** weighted by the entries of $x$:

$$Ax = x_1 a_1 + x_2 a_2$$

  where $a_1$ and $a_2$ are the first and second columns of $A$.
* **Main steps:** Identify the columns of $A$, $a_1 = \begin{pmatrix} 2 \\\\ 1 \end{pmatrix}$ and $a_2 = \begin{pmatrix} -1 \\\\ 3 \end{pmatrix}$, and weight them by $x_1 = 4$ and $x_2 = 2$:

$$Ax = 4\begin{pmatrix} 2 \\\\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\\\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\\\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\\\ 6 \end{pmatrix}$$

* **Result:**

$$Ax = 4\begin{pmatrix} 2 \\\\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\\\ 3 \end{pmatrix} = \begin{pmatrix} 6 \\\\ 10 \end{pmatrix}$$

* **Verification:** Adding the scaled column vectors entrywise gives $\begin{pmatrix} 8 + (-2) \\\\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\\\ 10 \end{pmatrix}$, matching the row-by-column dot product result from part 1.

---

> **Purpose of this exercise:** to show that matrix-vector multiplication can be viewed both as row-column dot products and as a linear combination of the columns of the matrix.
