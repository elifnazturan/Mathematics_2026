# Exercise 12. Homogeneous System

## Question

We are given the homogeneous linear system of three equations in three unknowns $(x, y, z)$:

$$
\begin{cases}
x + 2y - z = 0, \\
2x + 4y - 2z = 0, \\
x - y + 2z = 0.
\end{cases}
$$

We need to:
1. Solve the system and write all solutions in parametric form.
2. Explain why $(0, 0, 0)$ always satisfies a homogeneous system.

## Solution

### 1. Row Reduction and Parametric Solution

Write the augmented matrix for the homogeneous system:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}
$$

Eliminate $x$ from the second and third rows by applying $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}
$$

Swap the second and third rows ($R_2 \leftrightarrow R_3$) to obtain row-echelon form:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The non-trivial equations from the row-echelon matrix are

$$
\begin{cases}
x + 2y - z = 0, \\
-3y + 3z = 0.
\end{cases}
$$

From the second equation, $-3y + 3z = 0$ gives $y = z$. Let $z = t$, where $t \in \mathbb{R}$ is a real parameter; then $y = t$.

Substitute $y = t$ and $z = t$ into the first equation:

$$
x + 2t - t = 0 \implies x + t = 0 \implies x = -t
$$

Thus, all solutions in parametric form are given by

$$
\begin{cases}
x = -t, \\
y = t, \\
z = t, \quad t \in \mathbb{R}.
\end{cases}
$$

### 2. Why $(0, 0, 0)$ Always Satisfies a Homogeneous System

In a homogeneous linear system $Ax = 0$, every equation has zero on the right-hand side and is a linear combination of the unknowns with no constant term. Substituting $(x, y, z) = (0, 0, 0)$ multiplies every unknown by $0$ and adds zeros together, so the left-hand side of every equation evaluates to $0$, matching the right-hand side $0$ (in matrix form, $A \cdot 0 = 0$). Therefore, the trivial solution $(0, 0, 0)$ is always a solution—and here corresponds to choosing the parameter $t = 0$.
