# Exercise 7. Inverse of a Product

## Question

We are given two invertible $2 \times 2$ matrices:

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

We need to:
1. Compute $(AB)^{-1}$ and $B^{-1}A^{-1}$.
2. Check that the two resulting matrices are the same.
3. Explain the meaning of the reversed order in $(AB)^{-1} = B^{-1}A^{-1}$.

## Solution

### 1. Computing $(AB)^{-1}$

First, compute the product $AB$:

$$
AB = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} = \begin{pmatrix}
2 + 0 & 0 + 3 \\
0 + 0 & 0 + 3 \\
\end{pmatrix} = \begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
$$

Next, find the determinant of $AB$:

$$
\det(AB) = (2)(3) - (3)(0) = 6
$$

Since $\det(AB) = 6 \neq 0$, the product $AB$ is invertible. Applying the $2 \times 2$ inverse formula to $AB$ gives:

$$
(AB)^{-1} = \frac{1}{6} \begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

### 2. Computing $B^{-1}A^{-1}$ and Checking Equality

First, find $A^{-1}$. Since $\det(A) = (1)(1) - (1)(0) = 1$, the $2 \times 2$ inverse formula yields:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

Second, find $B^{-1}$. Since $\det(B) = (2)(3) - (0)(0) = 6$, the $2 \times 2$ inverse formula yields:

$$
B^{-1} = \frac{1}{6} \begin{pmatrix}
3 & 0 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

Now multiply $B^{-1}$ and $A^{-1}$ in that order:

$$
B^{-1}A^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} + 0 & -\frac{1}{2} + 0 \\
0 + 0 & 0 + \frac{1}{3} \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

Comparing the two results, we see that $(AB)^{-1} = B^{-1}A^{-1}$, as both equal the same matrix.

### 3. Meaning of the Reversed Order

In the product $AB$ acting on a vector $x$ as $(AB)x = A(Bx)$, transformation $B$ is applied first and transformation $A$ is applied second. To undo this combined process, we must first undo the last action ($A$) using $A^{-1}$ and then undo the first action ($B$) using $B^{-1}$. That corresponds to applying $B^{-1}(A^{-1}x) = (B^{-1}A^{-1})x$, which explains why the order of multiplication reverses.
