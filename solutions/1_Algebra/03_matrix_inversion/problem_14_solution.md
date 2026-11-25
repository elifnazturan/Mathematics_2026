# Exercise 14. A Matrix That Is Its Own Inverse

## Question

We assume that a square matrix $A$ (of size $n \times n$) satisfies:

$$
A^2 = I
$$

We need to:
1. Show that $A^{-1} = A$.
2. Give an example of a $2 \times 2$ matrix different from $I$ and $-I$ that satisfies this condition.
3. Verify the example by matrix multiplication.

## Solution

### 1. Showing That $A^{-1} = A$

By definition, the inverse of a square matrix $A$ is the matrix $B$ such that:

$$
AB = I \quad \text{and} \quad BA = I
$$

We are given that $A^2 = I$, which can be written as:

$$
A \cdot A = I
$$

Setting $B = A$ gives both $AB = A^2 = I$ and $BA = A^2 = I$. Therefore, $A$ satisfies the definition of the inverse of $A$, so $A$ is invertible and:

$$
A^{-1} = A
$$

### 2. Example of a $2 \times 2$ Matrix Different From $I$ and $-I$

Consider the $2 \times 2$ reflection matrix across the $x$-axis:

$$
A = \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}
$$

Clearly, $A$ is different from the identity matrix $I$ and from $-I$.

### 3. Verifying the Example by Multiplication

We compute $A^2 = A \cdot A$:

$$
A^2 = \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix} \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix} = \begin{pmatrix}
(1)(1) + (0)(0) & (1)(0) + (0)(-1) \\
(0)(1) + (-1)(0) & (0)(0) + (-1)(-1) \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} = I
$$

Since $A^2 = I$, we have $A^{-1} = A$, which confirms the result.
