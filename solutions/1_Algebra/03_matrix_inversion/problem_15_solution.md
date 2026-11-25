# Exercise 15. Two Methods for Solving the Same System

## Question

We are given the linear system $Ax = b$, where:

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}, \quad b = \begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

We need to:
1. Solve $Ax = b$ in two ways:
   - Using $x = A^{-1}b$.
   - Using Gaussian elimination.
2. Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

### 1. Solving via $x = A^{-1}b$

First, compute the determinant of $A$:

$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
$$

Since $\det(A) = 5 \neq 0$, $A$ is invertible. Using the $2 \times 2$ inverse formula:

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

Now compute $x = A^{-1}b$:

$$
x = \begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5} \\
\end{pmatrix} \begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

Computing each entry of $x$:

$$
x_1 = \frac{3}{5}(7) + \left(-\frac{1}{5}\right)(8) = \frac{21}{5} - \frac{8}{5} = \frac{13}{5}
$$

$$
x_2 = \left(-\frac{1}{5}\right)(7) + \frac{2}{5}(8) = -\frac{7}{5} + \frac{16}{5} = \frac{9}{5}
$$

Thus, the inverse-matrix method gives:

$$
x = \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

### 2. Solving via Gaussian Elimination

Write the augmented matrix $[A \mid b]$ for the system $Ax = b$:

$$
[A \mid b] = \left(\begin{array}{cc|c}
2 & 1 & 7 \\
1 & 3 & 8 \\
\end{array}\right)
$$

Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) so the leading entry in column $1$ is $1$:

$$
\left(\begin{array}{cc|c}
1 & 3 & 8 \\
2 & 1 & 7 \\
\end{array}\right)
$$

Eliminate the entry below the pivot by applying $R_2 \leftarrow R_2 - 2R_1$:

$$
\left(\begin{array}{cc|c}
1 & 3 & 8 \\
0 & -5 & -9 \\
\end{array}\right)
$$

From the second row, $-5x_2 = -9$, so:

$$
x_2 = \frac{9}{5}
$$

Substitute $x_2 = \frac{9}{5}$ into the first equation $x_1 + 3x_2 = 8$ (back-substitution):

$$
x_1 + 3\left(\frac{9}{5}\right) = 8 \quad \Longrightarrow \quad x_1 = 8 - \frac{27}{5} = \frac{40}{5} - \frac{27}{5} = \frac{13}{5}
$$

Thus, Gaussian elimination gives the same solution:

$$
x = \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

### 3. Comparison of Solutions, Steps, and Simplicity

- **Solutions:** Both methods yield the exact same solution vector, with $x_1 = \frac{13}{5}$ and $x_2 = \frac{9}{5}$.
- **Number of essential steps:** Using $x = A^{-1}b$ requires computing $\det(A)$, constructing the adjugate/inverse matrix $A^{-1}$ with fractions, and then multiplying $A^{-1}$ by $b$. Gaussian elimination requires fewer overhead steps here: one row swap, one row elimination, and direct back-substitution (with fractions appearing only at the end).
- **Which method was simpler:** Gaussian elimination was simpler in this example because it avoids finding and storing the full inverse matrix $A^{-1}$ first and reaches the answer more directly for a single right-hand side vector $b$. (By contrast, $x = A^{-1}b$ becomes more advantageous when solving $Ax = b$ for many different right-hand side vectors $b$ with the same matrix $A$.)
