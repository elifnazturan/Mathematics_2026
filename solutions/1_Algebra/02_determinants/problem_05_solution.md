# Exercise 5. Row Operations

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ by simplifying the matrix into an upper triangular form using row operations.
2. At each step, state whether and how the determinant changes.

## Solution

### 1. Reducing the Matrix with Row Operations

Adding a scalar multiple of one row to another row does not change the determinant of a matrix. We use this operation to create zeros below the main diagonal step by step.

First, apply the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
R_2^{\mathrm{new}} = (2, 1, 0) - 2(1, 2, 3) = (0, -3, -6)
$$

Because this adds $-2$ times row $1$ to row $2$, the determinant is **unchanged**:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

Next, apply the row operation $R_3 \leftarrow R_3 + R_1$:

$$
R_3^{\mathrm{new}} = (-1, 4, 2) + (1, 2, 3) = (0, 6, 5)
$$

Because this adds $1$ times row $1$ to row $3$, the determinant is again **unchanged**:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

Finally, to eliminate the $(3,2)$ entry, apply the row operation $R_3 \leftarrow R_3 + 2R_2$:

$$
R_3^{\mathrm{new}} = (0, 6, 5) + 2(0, -3, -6) = (0, 0, -7)
$$

Because this adds $2$ times row $2$ to row $3$, the determinant remains **unchanged**:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

### 2. Computing the Determinant from the Upper Triangular Matrix

The resulting matrix is upper triangular, so its determinant equals the product of its main diagonal entries:

$$
\det(A) = 1 \cdot (-3) \cdot (-7) = 21
$$
