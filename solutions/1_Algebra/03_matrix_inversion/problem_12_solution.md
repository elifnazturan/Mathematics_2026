# Exercise 12. Finding Inverses Without Starting from Scratch

## Question

It is known that for an invertible matrix $A$ (of the same size as the given inverse):

$$
A^{-1} = \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
$$

Without finding $A$, we need to:
1. Compute $(3A)^{-1}$ and justify the result using the appropriate inverse property.
2. Compute $(A^T)^{-1}$ and justify the result using the appropriate inverse property.
3. Compute $(A^2)^{-1}$ and justify the result using the appropriate inverse property.

## Solution

### 1. Computing $(3A)^{-1}$

For any nonzero scalar $c \neq 0$ and invertible $n \times n$ matrix $A$, the inverse of a scalar multiple satisfies:

$$
(cA)^{-1} = \frac{1}{c} A^{-1}
$$

Applying this property with $c = 3$:

$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3} \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} = \begin{pmatrix}
\frac{2}{3} & -\frac{1}{3} \\
-1 & \frac{2}{3} \\
\end{pmatrix}
$$

### 2. Computing $(A^T)^{-1}$

For any invertible matrix $A$, taking the inverse and taking the transpose commute:

$$
(A^T)^{-1} = (A^{-1})^T
$$

Transposing $A^{-1}$ swaps its off-diagonal entries while keeping the diagonal entries unchanged:

$$
(A^T)^{-1} = \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}^T = \begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}
$$

### 3. Computing $(A^2)^{-1}$

For any invertible matrix $A$ and positive integer $k$, the inverse of a power is the power of the inverse:

$$
(A^k)^{-1} = (A^{-1})^k
$$

With $k = 2$, we compute $(A^2)^{-1} = (A^{-1})^2 = A^{-1} A^{-1}$:

$$
(A^2)^{-1} = \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} \begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} = \begin{pmatrix}
(2)(2) + (-1)(-3) & (2)(-1) + (-1)(2) \\
(-3)(2) + (2)(-3) & (-3)(-1) + (2)(2) \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
(A^2)^{-1} = \begin{pmatrix}
4 + 3 & -2 - 2 \\
-6 - 6 & 3 + 4 \\
\end{pmatrix} = \begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}
$$
