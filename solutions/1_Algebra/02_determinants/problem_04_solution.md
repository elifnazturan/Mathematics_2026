# Exercise 4. Triangular Matrix

## Question

We are given the $3 \times 3$ upper triangular matrix:

$$
A = \begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ without expanding the determinant.
2. State the rule for the determinant of an arbitrary triangular matrix and explain it using this example.

## Solution

### 1. Computing $\det(A)$ Without Expansion

Matrix $A$ is upper triangular because all entries strictly below the main diagonal are equal to $0$. For a triangular matrix, the determinant equals the product of its main diagonal entries:

$$
\det(A) = 2 \cdot (-3) \cdot 7 = -42
$$

### 2. General Rule and Explanation via This Example

For any $n \times n$ triangular matrix (either upper triangular or lower triangular), the determinant is equal to the product of the entries on the main diagonal:

$$
\det(T) = t_{11} t_{22} \cdots t_{nn}
$$

In this example, the zeros below the main diagonal make row reduction and cofactor expansion unnecessary. Because the entries below $(1,1)$ and $(2,2)$ are already zero, expanding along the first column only keeps the top-left term $2$ times its $2 \times 2$ submatrix, and then the bottom-right $2 \times 2$ block is already triangular with diagonal entries $-3$ and $7$, giving:

$$
\det(A) = 2 \cdot \det \begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix} = 2 \cdot (-3) \cdot 7 = -42
$$

Thus, the determinant is simply the product of the diagonal entries $2$, $-3$, and $7$, which equals $-42$.
