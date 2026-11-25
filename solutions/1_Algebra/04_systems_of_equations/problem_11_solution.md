# Exercise 11. A Parameter in a System of Three Equations

## Question

We are given the linear system in three unknowns $(x, y, z)$ depending on the real parameter $t$:

$$
\begin{cases}
x + y + z = 1, \\
x + ty + z = 2, \\
x + y + tz = 3.
\end{cases}
$$

We need to:
1. Analyze the number of solutions depending on the parameter $t$ using elimination.
2. Separately analyze the parameter values for which a standard calculation or division step ceases to be valid.

## Solution

### 1. Elimination and Number of Solutions

Write the augmented matrix for the system:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}
$$

Eliminate $x$ from the second and third rows using the first pivot in row 1 by applying $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t - 1 & 0 & \mid & 1 \\
0 & 0 & t - 1 & \mid & 2 \\
\end{pmatrix}
$$

From the second and third rows, the corresponding equations are:

$$
(t - 1)y = 1, \qquad (t - 1)z = 2.
$$

We examine the possible values of $t \in \mathbb{R}$:

- **Case $t \neq 1$:** Here $t - 1 \neq 0$, so both equations can be divided by $t - 1$:

$$
y = \frac{1}{t - 1}, \qquad z = \frac{2}{t - 1}.
$$

Substituting $y$ and $z$ into the first equation $x + y + z = 1$ gives:

$$
x = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 4}{t - 1}.
$$

Thus, for every $t \neq 1$, the system has **exactly one solution**:

$$
(x, y, z) = \left(\frac{t - 4}{t - 1},\; \frac{1}{t - 1},\; \frac{2}{t - 1}\right).
$$

- **Case $t = 1$:** Substituting $t = 1$ into the eliminated matrix gives:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}
$$

The second row reads $0 = 1$ (and the third reads $0 = 2$), which is a contradiction. Therefore, for $t = 1$, the system is inconsistent and has **no solution**.

### 2. Where a Standard Step Ceases to Be Valid

Dividing by $t - 1$ to solve for $y$ and $z$ from $(t - 1)y = 1$ and $(t - 1)z = 2$ is valid only when the coefficient $t - 1$ is nonzero. At **$t = 1$**, we have $t - 1 = 0$, so division by $t - 1$ is undefined and $y$ and $z$ do not appear as pivot variables in the row-echelon matrix; instead, zero rows with nonzero right-hand sides appear, yielding no solution.
