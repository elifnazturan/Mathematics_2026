# Exercise 1. Definition of the Inverse

## Question

We are given two $2 \times 2$ matrices:

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

We need to:
1. Check, without using an inverse formula, whether $B = A^{-1}$.
2. Compute the products $AB$ and $BA$ and relate the results to the definition of the inverse matrix.

## Solution

### 1. Computing $AB$ and $BA$

By the definition of matrix multiplication, the $(i, j)$ entry of a product is the dot product of row $i$ of the first matrix with column $j$ of the second matrix.

First, we compute $AB$:

$$
AB = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} = \begin{pmatrix}
(2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\
(1)(1) + (1)(-1) & (1)(-1) + (1)(2) \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
AB = \begin{pmatrix}
2 - 1 & -2 + 2 \\
1 - 1 & -1 + 2 \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} = I_2
$$

Next, we compute $BA$:

$$
BA = \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} = \begin{pmatrix}
(1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\
(-1)(2) + (2)(1) & (-1)(1) + (2)(1) \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
BA = \begin{pmatrix}
2 - 1 & 1 - 1 \\
-2 + 2 & -1 + 2 \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} = I_2
$$

### 2. Relating the Results to the Definition of the Inverse

By definition, for a square matrix $A$ of size $n \times n$, a matrix $B$ of the same size is the inverse of $A$ (denoted $B = A^{-1}$) if and only if both products equal the $n \times n$ identity matrix:

$$
AB = I_2 \quad \text{and} \quad BA = I_2
$$

Because we found $AB = I_2$ and $BA = I_2$ directly by multiplication without using any formula, we confirm that $B = A^{-1}$ (and equivalently $A = B^{-1}$).
