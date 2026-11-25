# Exercise 13. Determinant by Elimination

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ using elimination (row operations).
2. Record the effect of every row operation used on the value of the determinant.

## Solution

### 1. Elimination Steps and Effect on the Determinant

Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + k R_j$ with $i \neq j$) does not change the value of the determinant. We use this operation to eliminate entries below the main diagonal and record each step's effect.

First, apply $R_2 \leftarrow R_2 - 2R_1$:

$$
R_2^{\mathrm{new}} = (2, 5, 7) - 2(1, 2, 3) = (0, 1, 1)
$$

- **Effect on determinant:** Unchanged (adding $-2$ times row $1$ to row $2$ preserves the determinant).

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

Second, apply $R_3 \leftarrow R_3 - R_1$:

$$
R_3^{\mathrm{new}} = (1, 0, 2) - (1, 2, 3) = (0, -2, -1)
$$

- **Effect on determinant:** Unchanged (adding $-1$ times row $1$ to row $3$ preserves the determinant).

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

Third, apply $R_3 \leftarrow R_3 + 2R_2$:

$$
R_3^{\mathrm{new}} = (0, -2, -1) + 2(0, 1, 1) = (0, 0, 1)
$$

- **Effect on determinant:** Unchanged (adding $2$ times row $2$ to row $3$ preserves the determinant).

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

### 2. Computing the Determinant

The resulting matrix is upper triangular, so its determinant is the product of its main diagonal entries:

$$
\det(A) = 1 \cdot 1 \cdot 1 = 1
$$
