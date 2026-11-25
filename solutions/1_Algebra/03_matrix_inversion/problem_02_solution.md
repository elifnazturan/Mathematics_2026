# Exercise 2. Formula for a 2x2 Matrix

## Question

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

We need to:
1. Find $A^{-1}$ using the inverse formula for a $2 \times 2$ matrix.
2. Check the result at the end by computing one product with $A$.

## Solution

### 1. Finding $A^{-1}$ Using the $2 \times 2$ Formula

For a $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \\ \end{pmatrix}$, its determinant is $\det(M) = ad - bc$. When $\det(M) \neq 0$, the inverse matrix is given by swapping the main diagonal entries, negating the off-diagonal entries, and dividing by $\det(M)$:

$$
M^{-1} = \frac{1}{ad - bc} \begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

For $A = \begin{pmatrix} 3 & 2 \\ 5 & 4 \\ \end{pmatrix}$, we identify $a = 3$, $b = 2$, $c = 5$, and $d = 4$. First, compute the determinant:

$$
\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2
$$

Since $\det(A) = 2 \neq 0$, $A$ is invertible. Applying the $2 \times 2$ formula gives:

$$
A^{-1} = \frac{1}{2} \begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} = \begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
$$

### 2. Checking the Result by Computing $A A^{-1}$

By the definition of an inverse matrix, multiplying $A$ by $A^{-1}$ should yield the $2 \times 2$ identity matrix $I_2$:

$$
A A^{-1} = \begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix} \begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
$$

Computing each entry of the product:

$$
A A^{-1} = \begin{pmatrix}
(3)(2) + (2)\left(-\frac{5}{2}\right) & (3)(-1) + (2)\left(\frac{3}{2}\right) \\
(5)(2) + (4)\left(-\frac{5}{2}\right) & (5)(-1) + (4)\left(\frac{3}{2}\right) \\
\end{pmatrix} = \begin{pmatrix}
6 - 5 & -3 + 3 \\
10 - 10 & -5 + 6 \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} = I_2
$$

Since $A A^{-1} = I_2$, the inverse matrix $A^{-1}$ is verified.
