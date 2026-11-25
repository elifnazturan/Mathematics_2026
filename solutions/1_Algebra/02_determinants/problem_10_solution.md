# Exercise 10. Detecting Dependence

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

We need to:
1. Explain why $\det(A) = 0$ without carrying out a full determinant calculation.
2. Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Solution

### 1. Why $\det(A) = 0$ Without Full Calculation

Looking at the rows of $A$, the second row $(2, 4, 6)$ is twice the first row $(1, 2, 3)$:

$$
R_2 = 2R_1
$$

A fundamental property of determinants states that if one row of a square matrix is a scalar multiple of another row, the determinant of the matrix is zero. Applying the row operation $R_2 \leftarrow R_2 - 2R_1$ does not change the determinant and turns the second row into $(0, 0, 0)$, a row of all zeros. A matrix with a zero row has determinant equal to $0$, so $\det(A) = 0$ immediately without full expansion.

### 2. Row Dependence and Noninvertibility

The specific linear dependence among the rows is:

$$
R_2 - 2R_1 + 0 \cdot R_3 = (0, 0, 0)
$$

Because one row can be written as a scalar multiple of another row, the rows of $A$ are linearly dependent. A square matrix is invertible if and only if its rows are linearly independent (equivalently, $\det(A) \neq 0$). Since $\det(A) = 0$ and the rows are linearly dependent, $A$ is **not invertible** (singular).
