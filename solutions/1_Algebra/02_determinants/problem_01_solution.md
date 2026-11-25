# Exercise 1. Determinant of a 2x2 Matrix

## Question

We are given two $2 \times 2$ matrices:

$$
A = \begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$ and $\det(B)$.
2. Determine which matrix is invertible and justify the answer.

## Solution

### 1. Computing the Determinants

For a $2 \times 2$ matrix of the form:

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

the determinant is given by:

$$
\det \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} = ad - bc
$$

Applying this formula to the first matrix $A$:

$$
\det(A) = \det \begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 22
$$

Applying the same formula to the second matrix $B$:

$$
\det(B) = \det \begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix} = (1)(14) - (7)(2) = 14 - 14 = 0
$$

### 2. Invertibility and Justification

A square matrix is invertible if and only if its determinant is nonzero ($\det \neq 0$):
- **Matrix $A$ is invertible** because $\det(A) = 22 \neq 0$. Its rows and columns are linearly independent, so the matrix has full rank and a unique inverse exists.
- **Matrix $B$ is not invertible (singular)** because $\det(B) = 0$. Notice that the second row of $B$ is a scalar multiple of the first row ($R_2 = 2R_1$), and similarly the second column is $7$ times the first column ($C_2 = 7C_1$), which means its rows and columns are linearly dependent.
