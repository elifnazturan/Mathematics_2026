# Exercise 4. Infinitely Many Solutions

## Question

We are given the linear system of three equations in three unknowns:

$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

We need to:
1. Solve the system and give the solution in parametric form.
2. Identify a free variable.
3. For one chosen parameter value, check that the resulting point satisfies all equations of the system.

## Solution

### 1. Row Reduction and Parametric Solution

Write the augmented matrix for the system:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

Eliminate $x$ from the second and third rows by applying $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

Swap the second and third rows ($R_2 \leftrightarrow R_3$) to obtain row-echelon form:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The row-echelon system is

$$
\begin{cases}
x + y + z = 2, \\
-2y = -2.
\end{cases}
$$

From the second equation, divide by $-2$:

$$
y = 1
$$

Let $z = t$, where $t \in \mathbb{R}$ is a real parameter. Substitute $y = 1$ and $z = t$ into the first equation:

$$
x + 1 + t = 2 \implies x = 1 - t
$$

Thus, the system has infinitely many solutions, given in parametric form by

$$
\begin{cases}
x = 1 - t, \\
y = 1, \\
z = t, \quad t \in \mathbb{R}.
\end{cases}
$$

### 2. Free Variable

In the row-echelon matrix, the pivot columns correspond to $x$ (row 1, column 1) and $y$ (row 2, column 2), while column 3 has no pivot. Therefore, $z$ is a free variable, which leads to one parameter $t \in \mathbb{R}$ and infinitely many solutions.

### 3. Verification for a Chosen Parameter Value

Choose $t = 2$. The parametric formulas give

$$
x = 1 - 2 = -1, \quad y = 1, \quad z = 2
$$

so the candidate point is $(-1, 1, 2)$. Substitute $(-1, 1, 2)$ into each original equation:

- **First equation:** $-1 + 1 + 2 = 2$, which matches the right-hand side $2$.
- **Second equation:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$, which matches the right-hand side $4$.
- **Third equation:** $-1 - 1 + 2 = 0$, which matches the right-hand side $0$.

All three equations are satisfied, confirming that $(-1, 1, 2)$ is a valid solution.
