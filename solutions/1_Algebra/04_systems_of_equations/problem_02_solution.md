# Exercise 2. Gaussian Elimination - One Solution

## Question

We are given the linear system of three equations in three unknowns:

$$
\begin{cases}
x + y + z = 6, \\
2x - y + z = 3, \\
x + 2y - z = 2.
\end{cases}
$$

We need to:
1. Solve the system using Gaussian elimination.
2. Substitute the resulting values into all equations and check consistency.

## Solution

### 1. Gaussian Elimination

Write the augmented matrix for the system:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

Eliminate $x$ from the second and third rows using the first pivot entry in row 1 by applying $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

Swap the second and third rows ($R_2 \leftrightarrow R_3$) to place a unit entry in the second pivot position:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

Eliminate $y$ from the third row by applying $R_3 \leftarrow R_3 + 3R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

The row-echelon system is

$$
\begin{cases}
x + y + z = 6, \\
y - 2z = -4, \\
-7z = -21.
\end{cases}
$$

From the third equation, divide by $-7$:

$$
z = \frac{-21}{-7} = 3
$$

Substitute $z = 3$ into the second equation:

$$
y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
$$

Substitute $y = 2$ and $z = 3$ into the first equation:

$$
x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1
$$

The unique solution is

$$
(x, y, z)^T = (1, 2, 3)^T
$$

### 2. Substitution and Consistency Check

Substitute $(x, y, z) = (1, 2, 3)$ into each original equation:

- **First equation:** $1 + 2 + 3 = 6$, which matches the right-hand side $6$.
- **Second equation:** $2(1) - 2 + 3 = 2 - 2 + 3 = 3$, which matches the right-hand side $3$.
- **Third equation:** $1 + 2(2) - 3 = 1 + 4 - 3 = 2$, which matches the right-hand side $2$.

All three equations are satisfied simultaneously, so the system is consistent and the solution $(x, y, z) = (1, 2, 3)$ is verified.
