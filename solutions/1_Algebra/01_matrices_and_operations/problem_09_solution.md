# Exercise 9. Composing Transformations

## Question

We are given two $2 \times 2$ matrices

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix}, \qquad
R = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix},
$$

and the vector $x = (1, 2)^T$, where $S$ represents nonuniform scaling (stretching along the $x$-axis by a factor of $2$ and leaving the $y$-axis unchanged) and $R$ represents a $90^\circ$ counterclockwise rotation in $\mathbb{R}^2$.

We need to:
1. Compute $RSx$ and $SRx$.
2. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

### 1. Computing $RSx$ and $SRx$

First, compute $RSx$ by applying $S$ to $x$ and then applying $R$ to the result:

$$
Sx = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix} (1, 2)^T = (2, 2)^T,
$$

$$
RSx = R(Sx) = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix} (2, 2)^T = (-2, 2)^T.
$$

Next, compute $SRx$ by applying $R$ to $x$ first and then applying $S$ to the result:

$$
Rx = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix} (1, 2)^T = (-2, 1)^T,
$$

$$
SRx = S(Rx) = \begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix} (-2, 1)^T = (-4, 1)^T.
$$

Thus, $RSx = (-2, 2)^T$ and $SRx = (-4, 1)^T$.

### 2. Comparison and Geometric Explanation

The two compositions give different vectors ($RSx \neq SRx$), showing that matrix multiplication is not commutative ($RS \neq SR$) and that the order in which transformations are applied changes the outcome:

- **Scaling then rotating ($RSx$):** Starting at $(1, 2)^T$, scaling doubles the $x$-coordinate to $(2, 2)^T$. Rotating $(2, 2)^T$ by $90^\circ$ counterclockwise sends $(u, v)^T \mapsto (-v, u)^T$, giving $(-2, 2)^T$.
- **Rotating then scaling ($SRx$):** Starting at $(1, 2)^T$, rotating $90^\circ$ counterclockwise first moves the point to $(-2, 1)^T$. Then scaling doubles the new $x$-coordinate $-2$ to $-4$ while keeping the $y$-coordinate at $1$, yielding $(-4, 1)^T$.

Geometrically, scaling stretches only along the horizontal axis rather than uniformly in all directions, so performing it before or after a rotation changes which coordinate gets stretched and where the vector lands.
