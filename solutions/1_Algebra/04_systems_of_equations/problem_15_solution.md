# Exercise 15. Classifying Three Systems

## Question

For each of the following three linear systems in two unknowns $(x, y)$, we perform only as much elimination as necessary to recognize its type and justify the classification (**one solution**, **infinitely many solutions**, or **no solution**):

**System 1**

$$
\begin{cases}
x + y = 2, \\
x - y = 0.
\end{cases}
$$

**System 2**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4.
\end{cases}
$$

**System 3**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

## Solution

### 1. System 1 — One Solution

Write the augmented matrix and apply $R_2 \leftarrow R_2 - R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}
$$

The eliminated matrix is in row echelon form with two non-zero pivot entries ($1$ in column 1 and $-2$ in column 2) and no contradiction row. There are $2$ pivots for $2$ unknowns ($0$ free variables), so the system has **one solution** (specifically, $-2y = -2 \implies y = 1$ and $x + 1 = 2 \implies x = 1$, giving $(x, y) = (1, 1)$).

### 2. System 2 — Infinitely Many Solutions

Write the augmented matrix and apply $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The second row becomes $(0 \; 0 \mid 0)$, which corresponds to the tautology $0 = 0$ and adds no new condition. There is $1$ pivot column (for $x$) and $1$ non-pivot column (for $y$, a free variable), so the system is consistent and has **infinitely many solutions** (setting $y = t$ with $t \in \mathbb{R}$ gives $x = 2 - t$).

### 3. System 3 — No Solution

Write the augmented matrix and apply $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

The second row becomes $(0 \; 0 \mid 1)$, which corresponds to the equation $0x + 0y = 1$, i.e., $0 = 1$. Because this is a contradiction, no pair $(x, y)$ satisfies both equations simultaneously, so the system is inconsistent and has **no solution**.
