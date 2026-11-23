# Exercise 6. Transpose

**Given:**

$$A = \begin{pmatrix} 1 & 2 & 3 \\\\ 4 & 5 & 6 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\\\ 2 & 1 \\\\ -1 & 3 \end{pmatrix}$$

---

### 1. Compute $A^T$, $B^T$, and $AB$.

* **Method and Property Used:** Taking the **transpose** of an $m \times n$ matrix swaps its rows and columns to produce an $n \times m$ matrix, with entry $(i, j)$ of $M^T$ equal to entry $(j, i)$ of $M$. Here $A$ is $2 \times 3$ and $B$ is $3 \times 2$, so the inner dimensions of $AB$ match ($3 = 3$) and $AB$ is a $2 \times 2$ matrix whose entries are row-by-column dot products.

* **Compute $A^T$ ($3 \times 2$):**
  * *Main steps:* Turn row $1$ $(1, 2, 3)$ and row $2$ $(4, 5, 6)$ of $A$ into column $1$ and column $2$ of $A^T$:

$$A^T = \begin{pmatrix} 1 & 4 \\\\ 2 & 5 \\\\ 3 & 6 \end{pmatrix}$$

  * *Result:*

$$A^T = \begin{pmatrix} 1 & 4 \\\\ 2 & 5 \\\\ 3 & 6 \end{pmatrix}$$

  * *Verification:* Entry $(3, 2)$ of $A^T$ equals entry $(2, 3)$ of $A$, which is $6$, and the size changes from $2 \times 3$ to $3 \times 2$.

* **Compute $B^T$ ($2 \times 3$):**
  * *Main steps:* Turn the three rows of $B$ into the three columns of $B^T$:

$$B^T = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 1 & 3 \end{pmatrix}$$

  * *Result:*

$$B^T = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 1 & 3 \end{pmatrix}$$

  * *Verification:* Entry $(2, 3)$ of $B^T$ equals entry $(3, 2)$ of $B$, which is $3$, and the size changes from $3 \times 2$ to $2 \times 3$.

* **Compute $AB$ ($2 \times 2$):**
  * *Main steps:* Compute dot products of rows of $A$ with columns of $B$:

$$AB = \begin{pmatrix} 1(1) + 2(2) + 3(-1) & 1(0) + 2(1) + 3(3) \\\\ 4(1) + 5(2) + 6(-1) & 4(0) + 5(1) + 6(3) \end{pmatrix} = \begin{pmatrix} 1 + 4 - 3 & 0 + 2 + 9 \\\\ 4 + 10 - 6 & 0 + 5 + 18 \end{pmatrix}$$

  * *Result:*

$$AB = \begin{pmatrix} 2 & 11 \\\\ 8 & 23 \end{pmatrix}$$

  * *Verification:* Checking entry $(2, 2)$ directly: row $2$ of $A$, $(4, 5, 6)$, dotted with column $2$ of $B$, $\begin{pmatrix} 0 \\\\ 1 \\\\ 3 \end{pmatrix}$, gives $4(0) + 5(1) + 6(3) = 23$.

---

### 2. Verify that $(AB)^T = B^T A^T$.

* **Method and Property Used:** A fundamental property of matrix transposition is the **reverse-order law**, $(AB)^T = B^T A^T$: transposing a product reverses the order of the factors. Since $B^T$ is $2 \times 3$ and $A^T$ is $3 \times 2$, $B^T A^T$ is defined and yields a $2 \times 2$ matrix.

* **Main steps:**
  * Transpose $AB$ to get $(AB)^T$:

$$(AB)^T = \begin{pmatrix} 2 & 8 \\\\ 11 & 23 \end{pmatrix}$$

  * Multiply $B^T$ ($2 \times 3$) by $A^T$ ($3 \times 2$):

$$B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\\\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\\\ 2 & 5 \\\\ 3 & 6 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(2) + (-1)(3) & 1(4) + 2(5) + (-1)(6) \\\\ 0(1) + 1(2) + 3(3) & 0(4) + 1(5) + 3(6) \end{pmatrix}$$

$$B^T A^T = \begin{pmatrix} 1 + 4 - 3 & 4 + 10 - 6 \\\\ 0 + 2 + 9 & 0 + 5 + 18 \end{pmatrix} = \begin{pmatrix} 2 & 8 \\\\ 11 & 23 \end{pmatrix}$$

* **Result:**

$$(AB)^T = \begin{pmatrix} 2 & 8 \\\\ 11 & 23 \end{pmatrix} = B^T A^T$$

* **Verification:** Every corresponding entry of $(AB)^T$ and $B^T A^T$ matches ($2 = 2$, $8 = 8$, $11 = 11$, $23 = 23$), confirming $(AB)^T = B^T A^T$ in this example.

---

> **Purpose of this exercise:** to practice transposing matrices and vectors and verify how transposition reverses multiplication order in $(AB)^T = B^T A^T$.
