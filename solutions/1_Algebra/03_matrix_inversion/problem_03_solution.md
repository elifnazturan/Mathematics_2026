# Exercise 3. When Does the Inverse Not Exist?

## Question

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

We need to:
1. Explain why $A^{-1}$ does not exist using the determinant.
2. Explain why $A^{-1}$ does not exist using dependence between the rows.

## Solution

### 1. Explanation Using the Determinant

For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \\ \end{pmatrix}$, the determinant is $\det(A) = ad - bc$. Computing $\det(A)$ for the given matrix:

$$
\det(A) = (2)(2) - (4)(1) = 4 - 4 = 0
$$

A square matrix is invertible if and only if its determinant is nonzero ($\det(A) \neq 0$). Because $\det(A) = 0$, the inverse matrix $A^{-1}$ does not exist.

### 2. Explanation Using Dependence Between the Rows

Let $r_1 = (2, 4)$ and $r_2 = (1, 2)$ denote the first and second rows of $A$. The first row is twice the second row:

$$
r_1 = 2r_2 \quad \Longleftrightarrow \quad r_1 - 2r_2 = (0, 0)
$$

Because one row is a scalar multiple of the other, the rows of $A$ are linearly dependent. A square matrix with linearly dependent rows cannot have full rank or be inverted via row reduction to the identity matrix, so $A^{-1}$ does not exist. Connecting both views: linear dependence of the rows forces $\det(A) = 0$, which means $A$ is singular and noninvertible.
