# Exercise 5. Row Echelon Form and Number of Solutions

## Question

We are given the augmented matrix in row echelon form for a linear system in three unknowns $(x, y, z)$:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

We need to:
1. Determine the number of solutions of the corresponding linear system.
2. Write the solutions in parametric form.
3. Explain how to determine how many variables may be chosen freely.

## Solution

### 1. Number of Solutions

The augmented matrix is already in row echelon form and has no contradiction row of the form $(0 \; 0 \; 0 \mid c)$ with $c \neq 0$. The third row corresponds to $0 = 0$, which is always satisfied.

There are $3$ unknowns in total and $2$ pivot columns (column 1 with pivot $1$ in row 1, and column 2 with pivot $1$ in row 2). Since there is at least one free variable and the system is consistent, the system has infinitely many solutions.

### 2. Parametric Form of the Solutions

Write the non-trivial equations corresponding to the first two rows:

$$
\begin{cases}
x + 2y - z = 3, \\
y + 2z = 1.
\end{cases}
$$

Let $z = t$, where $t \in \mathbb{R}$ is a real parameter. From the second equation:

$$
y + 2t = 1 \implies y = 1 - 2t
$$

Substitute $y = 1 - 2t$ and $z = t$ into the first equation:

$$
x + 2(1 - 2t) - t = 3 \implies x + 2 - 5t = 3 \implies x = 1 + 5t
$$

Thus, the solution set in parametric form is

$$
\begin{cases}
x = 1 + 5t, \\
y = 1 - 2t, \\
z = t, \quad t \in \mathbb{R}.
\end{cases}
$$

### 3. Number of Free Variables

In row echelon form, each pivot column corresponds to a basic (pivot) variable, while every non-pivot column in the coefficient part corresponds to a free variable:

$$
\text{Number of free variables} = \text{Number of unknowns} - \text{Number of pivots} = 3 - 2 = 1
$$

Because there is $1$ pivot and $3$ unknowns, exactly $1$ variable ($z$) can be chosen freely as a parameter.
