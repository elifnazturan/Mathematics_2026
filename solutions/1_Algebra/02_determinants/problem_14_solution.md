# Exercise 14. A System of Equations and the Determinant

## Question

We are given the linear system $Ax = b$, where the coefficient matrix is:

$$
A = \begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}
$$

We need to:
1. Find all values of $k$ for which the system $Ax = b$ has a unique solution for every right-hand side vector $b$.
2. For the remaining value of $k$, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example of $b$ for which it has no solution.

## Solution

### 1. Unique Solution Condition via the Determinant

A linear system $Ax = b$ with an $n \times n$ matrix $A$ has a unique solution for every right-hand side $b$ if and only if $A$ is invertible, which is equivalent to $\det(A) \neq 0$.

Computing $\det(A)$:

$$
\det(A) = \det \begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix} = (1)(4) - (2)(k) = 4 - 2k
$$

For a unique solution for every $b$, we require $\det(A) \neq 0$:

$$
4 - 2k \neq 0
$$

$$
2k \neq 4
$$

$$
k \neq 2
$$

Thus, the system has a unique solution for every $b$ when $k \neq 2$.

### 2. Exceptional Case ($k = 2$): Infinitely Many Solutions vs. No Solution

When $k = 2$, we have $\det(A) = 4 - 2(2) = 0$, so $A$ is singular:

$$
A = \begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
$$

Notice that the second row of $A$ is twice the first row, so the system corresponds to two equations:

$$
x_1 + 2x_2 = b_1
$$

$$
2x_1 + 4x_2 = b_2
$$

- **Infinitely many solutions:** Choose $b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$. The second equation $2x_1 + 4x_2 = 2$ is simply $2$ times the first equation $x_1 + 2x_2 = 1$, so both equations represent the same line and every point $(x_1, x_2)$ with $x_1 + 2x_2 = 1$ (for instance, $x_2 = t$, $x_1 = 1 - 2t$ for $t \in \mathbb{R}$) is a solution.
- **No solution:** Choose $b = \begin{pmatrix} 1 \\ 3 \end{pmatrix}$. Multiplying the first equation $x_1 + 2x_2 = 1$ by $2$ gives $2x_1 + 4x_2 = 2$, which contradicts the second equation $2x_1 + 4x_2 = 3$ ($2 = 3$ is impossible), so the system is inconsistent and has no solution.
