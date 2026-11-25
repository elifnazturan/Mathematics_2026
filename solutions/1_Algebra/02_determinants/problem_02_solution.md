# Exercise 2. Determinant of a 3x3 Matrix

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ using Sarrus' rule.
2. Perform one simple check using a chosen property of the determinant.

## Solution

### 1. Computing $\det(A)$ Using Sarrus' Rule

For a $3 \times 3$ matrix, Sarrus' rule sums the products of the three downward-right diagonals and subtracts the sum of the products of the three upward-right diagonals.

First, we compute the products along the downward-right diagonals:

$$
1 \cdot 3 \cdot 5 = 15
$$

$$
2 \cdot 4 \cdot 2 = 16
$$

$$
(-1) \cdot 0 \cdot 1 = 0
$$

Their sum is:

$$
15 + 16 + 0 = 31
$$

Next, we compute the products along the upward-right diagonals:

$$
2 \cdot 3 \cdot (-1) = -6
$$

$$
1 \cdot 4 \cdot 1 = 4
$$

$$
5 \cdot 0 \cdot 2 = 0
$$

Their sum is:

$$
-6 + 4 + 0 = -2
$$

Subtracting the upward-right sum from the downward-right sum gives:

$$
\det(A) = 31 - (-2) = 33
$$

### 2. Checking the Result Using Determinant Properties

We can verify this value using the property that adding a scalar multiple of one row to another row does not change the determinant, and the determinant of an upper triangular matrix equals the product of its main diagonal entries.

First, perform the row operation $R_3 \leftarrow R_3 - 2R_1$:

$$
R_3^{\mathrm{new}} = (2, 1, 5) - 2(1, 2, -1) = (0, -3, 7)
$$

This gives an equivalent matrix with the same determinant:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}
$$

Next, perform the row operation $R_3 \leftarrow R_3 + R_2$:

$$
R_3^{\mathrm{new}} = (0, -3, 7) + (0, 3, 4) = (0, 0, 11)
$$

This yields an upper triangular matrix:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & 0 & 11 \\
\end{pmatrix}
$$

Multiplying the diagonal entries gives:

$$
\det(A) = 1 \cdot 3 \cdot 11 = 33
$$

Both methods give $\det(A) = 33$, confirming that the calculation is consistent.
