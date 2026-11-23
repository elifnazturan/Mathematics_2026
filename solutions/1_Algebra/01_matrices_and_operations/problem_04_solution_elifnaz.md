# Exercise 4. Matrix Multiplication and Noncommutativity

**Given:**

$$A = \begin{pmatrix} 1 & 2 \\\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\\\ 3 & 1 \end{pmatrix}$$

---

### 1. Compute $AB$ and $BA$.

* **Method and Property Used:** Both $A$ and $B$ are $2 \times 2$ matrices, so both products $AB$ and $BA$ are defined and produce $2 \times 2$ matrices. Each entry $(i, j)$ of a matrix product is computed as the **dot product** (row-by-column inner product) of row $i$ of the left matrix with column $j$ of the right matrix.

* **Compute $AB$:**
  * *Main steps:* Take dot products of rows of $A$ with columns of $B$:

$$AB = \begin{pmatrix} 1(2) + 2(3) & 1(0) + 2(1) \\\\ 0(2) + 1(3) & 0(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 6 & 0 + 2 \\\\ 0 + 3 & 0 + 1 \end{pmatrix}$$

  * *Result:*

$$AB = \begin{pmatrix} 8 & 2 \\\\ 3 & 1 \end{pmatrix}$$

  * *Verification:* Checking individual entries directly: row $1$ of $A$ is $(1, 2)$; dotted with column $1$ of $B$, $\binom{2}{3}$, gives $1\cdot 2 + 2\cdot 3 = 8$, and dotted with column $2$ of $B$, $\binom{0}{1}$, gives $1\cdot 0 + 2\cdot 1 = 2$. Row $2$ of $A$ is $(0, 1)$, giving $0\cdot 2 + 1\cdot 3 = 3$ and $0\cdot 0 + 1\cdot 1 = 1$, matching $\begin{pmatrix} 8 & 2 \\\\ 3 & 1 \end{pmatrix}$.

* **Compute $BA$:**
  * *Main steps:* Take dot products of rows of $B$ with columns of $A$:

$$BA = \begin{pmatrix} 2(1) + 0(0) & 2(2) + 0(1) \\\\ 3(1) + 1(0) & 3(2) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 & 4 + 0 \\\\ 3 + 0 & 6 + 1 \end{pmatrix}$$

  * *Result:*

$$BA = \begin{pmatrix} 2 & 4 \\\\ 3 & 7 \end{pmatrix}$$

  * *Verification:* Checking entry $(1, 2)$ directly: row $1$ of $B$ is $(2, 0)$ and column $2$ of $A$ is $\binom{2}{1}$, giving $2(2) + 0(1) = 4$. Checking entry $(2, 2)$ directly: row $2$ of $B$ is $(3, 1)$ and column $2$ of $A$ is $\binom{2}{1}$, giving $3(2) + 1(1) = 7$, matching $\begin{pmatrix} 2 & 4 \\\\ 3 & 7 \end{pmatrix}$.

---

### 2. Is $AB = BA$? Meaning of Noncommutativity.

* **Result:** **No, $AB \neq BA$** ($\begin{pmatrix} 8 & 2 \\\\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\\\ 3 & 7 \end{pmatrix}$).
* **Explanation and Method Used:** Unlike ordinary multiplication of real numbers (where $a \cdot b = b \cdot a$), **matrix multiplication is noncommutative**: changing the order of the factors generally changes the result. Because entry $(i, j)$ pairs a row of the first matrix with a column of the second matrix, swapping $A$ and $B$ pairs completely different rows and columns—and in terms of linear transformations, $AB$ applies transformation $B$ first and then $A$, whereas $BA$ applies $A$ first and then $B$.
* **Verification:** Comparing entry $(1, 1)$ shows $8 \neq 2$, and comparing entry $(1, 2)$ shows $2 \neq 4$, confirming that $AB$ and $BA$ are not equal.

---

> **Purpose of this exercise:** to highlight that matrix multiplication depends on factor order (noncommutativity), contrasting it with ordinary numerical multiplication.
