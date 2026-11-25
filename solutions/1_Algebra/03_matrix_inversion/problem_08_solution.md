# Exercise 8. Inverse of a Transformation

## Question

We are given the $2 \times 2$ matrix describing a scaling of the plane:

$$
S = \begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
$$

We need to:
1. Find $S^{-1}$.
2. Explain geometrically what the inverse transformation does.
3. Check the action of the pair $S, S^{-1}$ on one simple vector.

## Solution

### 1. Finding $S^{-1}$

Because $S$ is a diagonal matrix with nonzero diagonal entries ($2 \neq 0$ and $\frac{1}{2} \neq 0$), its inverse is obtained by taking the reciprocals of the diagonal entries:

$$
S^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
$$

### 2. Geometric Meaning of the Inverse Transformation

The matrix $S$ stretches the horizontal ($x$-) coordinate by a factor of $2$ and shrinks the vertical ($y$-) coordinate by a factor of $\frac{1}{2}$. The inverse transformation $S^{-1}$ undoes this scaling: it shrinks the horizontal ($x$-) coordinate by a factor of $\frac{1}{2}$ and stretches the vertical ($y$-) coordinate by a factor of $2$, returning every scaled point back to its original position.

### 3. Checking the Action of $S$ and $S^{-1}$ on a Simple Vector

Take the simple vector $v$ with entries $1$ and $1$.

First, apply $S$ to $v$:

$$
Sv = \begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix} \begin{pmatrix}
1 \\
1 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot 1 + 0 \cdot 1 \\
0 \cdot 1 + \frac{1}{2} \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
2 \\
\frac{1}{2} \\
\end{pmatrix}
$$

Next, apply $S^{-1}$ to the transformed vector $Sv$:

$$
S^{-1}(Sv) = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix} \begin{pmatrix}
2 \\
\frac{1}{2} \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} \cdot 2 + 0 \cdot \frac{1}{2} \\
0 \cdot 2 + 2 \cdot \frac{1}{2} \\
\end{pmatrix} = \begin{pmatrix}
1 \\
1 \\
\end{pmatrix} = v
$$

The pair $S, S^{-1}$ maps $v$ to the vector with entries $2$ and $\frac{1}{2}$ and then back to $v$, confirming that $S^{-1}$ undoes $S$.
