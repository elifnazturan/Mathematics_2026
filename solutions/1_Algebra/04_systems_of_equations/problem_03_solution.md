# Exercise 3. Inconsistent System

## Question

We are given the linear system:

$$
\begin{cases}
x + 2y = 3, \\
2x + 4y = 7.
\end{cases}
$$

We need to:
1. Solve the system or show that it is inconsistent.
2. Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

### 1. Elimination and Contradiction in the Matrix

Write the augmented matrix for the system:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}
$$

Eliminate $x$ from the second row by applying $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

In the resulting matrix, the second row has zeros in all coefficient positions on the left of the vertical bar and a nonzero entry $1$ on the right-hand side.

### 2. Interpretation in Terms of Equations

The second row of the eliminated matrix corresponds to the equation

$$
0x + 0y = 1
$$

which simplifies to

$$
0 = 1
$$

This statement is false for all real numbers $x$ and $y$. Therefore, no pair $(x, y)$ can satisfy both equations simultaneously, so the system is inconsistent and has no solution. Geometrically, the two lines have the same slope but different intercepts, so they are parallel and disjoint.
