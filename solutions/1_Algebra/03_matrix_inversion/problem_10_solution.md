# Exercise 10. Inverse of a Diagonal Matrix

## Question

We are given two $3 \times 3$ diagonal matrices:

$$
D = \begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}, \quad E = \begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
$$

We need to:
1. Decide, without using Gauss--Jordan elimination, which matrix is invertible.
2. For the invertible matrix, give its inverse $D^{-1}$.
3. Check the result by matrix multiplication.

## Solution

### 1. Deciding Which Matrix Is Invertible

A diagonal matrix is invertible if and only if all of its main diagonal entries are nonzero (equivalently, its determinant, which equals the product of its diagonal entries, is nonzero):

- For $D$, the diagonal entries are $2$, $-3$, and $5$. Since none of them is zero ($\det(D) = 2 \cdot (-3) \cdot 5 = -30 \neq 0$), matrix $D$ is invertible.
- For $E$, the diagonal entries are $2$, $0$, and $5$. Because the $(2, 2)$ diagonal entry is $0$ (and $\det(E) = 2 \cdot 0 \cdot 5 = 0$), matrix $E$ is not invertible.

Thus, only $D$ is invertible.

### 2. Finding $D^{-1}$

Without using Gauss--Jordan elimination, the inverse of an invertible diagonal matrix is obtained simply by taking the reciprocal of each diagonal entry:

$$
D^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
$$

### 3. Checking the Result by Multiplication

By the definition of an inverse matrix, multiplying $D$ and $D^{-1}$ should produce the $3 \times 3$ identity matrix $I_3$:

$$
D D^{-1} = \begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix} \begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot \frac{1}{2} & 0 & 0 \\
0 & (-3) \cdot \left(-\frac{1}{3}\right) & 0 \\
0 & 0 & 5 \cdot \frac{1}{5} \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} = I_3
$$

Since $D D^{-1} = I_3$, the inverse matrix $D^{-1}$ is verified.
