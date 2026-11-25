# Exercise 6. Solving a System Using the Inverse

## Question

We are given the linear system $Ax = b$, where:

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}, \quad b = \begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
$$

We need to:
1. Solve $Ax = b$ using $x = A^{-1}b$.
2. Substitute the resulting vector $x$ back into the equation $Ax = b$ and check the result.

## Solution

### 1. Finding $A^{-1}$ and Computing $x = A^{-1}b$

First, compute the determinant of the $2 \times 2$ matrix $A$:

$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
$$

Since $\det(A) = 5 \neq 0$, matrix $A$ is invertible. Using the inverse formula for a $2 \times 2$ matrix:

$$
A^{-1} = \frac{1}{\det(A)} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix} = \frac{1}{5} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix} = \begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5} \\
\end{pmatrix}
$$

Multiplying both sides of $Ax = b$ on the left by $A^{-1}$ gives $x = A^{-1}b$:

$$
x = \begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5} \\
\end{pmatrix} \begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
$$

Computing each component of $x$:

$$
x_1 = \frac{3}{5}(5) + \left(-\frac{1}{5}\right)(7) = 3 - \frac{7}{5} = \frac{8}{5}
$$

$$
x_2 = \left(-\frac{1}{5}\right)(5) + \frac{2}{5}(7) = -1 + \frac{14}{5} = \frac{9}{5}
$$

Thus, the solution vector is:

$$
x = \begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

### 2. Substituting Back into $Ax = b$ to Check

We substitute $x$ with entries $\frac{8}{5}$ and $\frac{9}{5}$ into the left-hand side $Ax$:

$$
Ax = \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix} \begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot \frac{8}{5} + 1 \cdot \frac{9}{5} \\
1 \cdot \frac{8}{5} + 3 \cdot \frac{9}{5} \\
\end{pmatrix}
$$

Simplifying each entry:

$$
Ax = \begin{pmatrix}
\frac{16}{5} + \frac{9}{5} \\
\frac{8}{5} + \frac{27}{5} \\
\end{pmatrix} = \begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix} = \begin{pmatrix}
5 \\
7 \\
\end{pmatrix} = b
$$

Since $Ax = b$ holds, the solution vector $x$ is verified.
