# Exercise 11. Shortening the Calculation with Row Operations

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ by first performing row operations that create as many zeros as possible.
2. State which row operations do not change the determinant.

## Solution

### 1. Row Operations That Preserve the Determinant

Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + k R_j$ with $i \neq j$) does not change the determinant of a square matrix. Swapping two rows or multiplying a row by a nonzero scalar would change the determinant, so we stick strictly to row-replacement operations of the form $R_i \leftarrow R_i + k R_j$.

### 2. Creating Zeros and Computing $\det(A)$

Because the first entry in all three rows is $1$, we can eliminate the leading $1$ in the second and third rows using the first row.

First, apply the row operation $R_2 \leftarrow R_2 - R_1$:

$$
R_2^{\mathrm{new}} = (1, 3, 4) - (1, 2, 3) = (0, 1, 1)
$$

This operation does not change the determinant:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

Next, apply the row operation $R_3 \leftarrow R_3 - R_1$:

$$
R_3^{\mathrm{new}} = (1, 4, 6) - (1, 2, 3) = (0, 2, 3)
$$

This operation also leaves the determinant unchanged:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

Now the first column has zeros below the pivot $1$, so expanding along the first column gives a $2 \times 2$ determinant:

$$
\det(A) = 1 \cdot \det \begin{pmatrix}
1 & 1 \\
2 & 3 \\
\end{pmatrix}
$$

We can make one more zero in the $2 \times 2$ block by applying $R_2' \leftarrow R_2' - 2R_1'$ to the rows $(1, 1)$ and $(2, 3)$, which again does not change the determinant:

$$
(2, 3) - 2(1, 1) = (0, 1)
$$

This gives a triangular $2 \times 2$ matrix:

$$
\det \begin{pmatrix}
1 & 1 \\
2 & 3 \\
\end{pmatrix} = \det \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} = 1 \cdot 1 = 1
$$

Therefore:

$$
\det(A) = 1
$$
