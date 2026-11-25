# Exercise 12. A Parameter Revealed by a Row Operation

## Question

We are given the $3 \times 3$ matrix depending on a parameter $t$:

$$
A(t) = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

We need to:
1. First perform the row operation $R_2 \leftarrow R_2 - 2R_1$ before computing the determinant.
2. Use the resulting matrix structure to find all values of $t$ for which $A(t)$ is not invertible.
3. Explain what special happens to the rows of the matrix for the value of $t$ found.

## Solution

### 1. Applying the Row Operation $R_2 \leftarrow R_2 - 2R_1$

Adding $-2$ times the first row to the second row does not change the determinant of $A(t)$:

$$
R_2^{\mathrm{new}} = (2, 4, t) - 2(1, 2, 3) = (0, 0, t - 6)
$$

This gives the equivalent matrix:

$$
A'(t) = \begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

with $\det(A(t)) = \det(A'(t))$.

### 2. Computing the Determinant and Finding Non-Invertible Values of $t$

Expanding $\det(A'(t))$ along the first column (since the entries below $1$ are $0$):

$$
\det(A'(t)) = 1 \cdot \det \begin{pmatrix}
0 & t - 6 \\
1 & 1 \\
\end{pmatrix}
$$

Computing the $2 \times 2$ determinant:

$$
\det \begin{pmatrix}
0 & t - 6 \\
1 & 1 \\
\end{pmatrix} = (0)(1) - (t - 6)(1) = -(t - 6) = 6 - t
$$

Thus:

$$
\det(A(t)) = 6 - t
$$

A square matrix is not invertible if and only if its determinant is zero. Setting $\det(A(t)) = 0$:

$$
6 - t = 0
$$

$$
t = 6
$$

So $A(t)$ is not invertible when $t = 6$ (and is invertible for all $t \neq 6$).

### 3. What Happens to the Rows When $t = 6$

When $t = 6$, the second row of the original matrix $A(6)$ is $(2, 4, 6)$, which is exactly twice the first row $(1, 2, 3)$:

$$
R_2 = 2R_1
$$

In the transformed matrix $A'(6)$, the entire new second row becomes $(0, 0, 0)$ (a zero row). Because the rows are linearly dependent—one row is a scalar multiple of another—the matrix has rank less than $3$, its determinant is $0$, and it is not invertible.
