# Exercise 9. Matrix Equation

## Question

We are given two $2 \times 2$ matrices:

$$
A = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
$$

We need to:
1. Decide, before calculating, on which side of the equation $AX = B$ the matrix $A^{-1}$ must be used to solve for $X$.
2. Solve the matrix equation $AX = B$ for $X$.
3. Check the result by computing $AX$.

## Solution

### 1. Which Side to Multiply by $A^{-1}$

In the equation $AX = B$, the matrix $A$ multiplies $X$ on the left. Because matrix multiplication is not commutative in general, we must multiply both sides on the left by $A^{-1}$ so that $A^{-1}$ sits directly next to $A$:

$$
A^{-1}(AX) = A^{-1}B \quad \Longrightarrow \quad (A^{-1}A)X = A^{-1}B \quad \Longrightarrow \quad I_2 X = A^{-1}B \quad \Longrightarrow \quad X = A^{-1}B
$$

### 2. Finding $A^{-1}$ and Computing $X = A^{-1}B$

First, compute the determinant of the $2 \times 2$ matrix $A$:

$$
\det(A) = (1)(1) - (2)(0) = 1 - 0 = 1
$$

Since $\det(A) = 1 \neq 0$, $A$ is invertible. Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
$$

Now compute $X = A^{-1}B$:

$$
X = \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} = \begin{pmatrix}
(1)(3) + (-2)(2) & (1)(1) + (-2)(4) \\
(0)(3) + (1)(2) & (0)(1) + (1)(4) \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
X = \begin{pmatrix}
3 - 4 & 1 - 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} = \begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
$$

### 3. Checking the Result by Computing $AX$

We substitute the matrix $X$ back into the left-hand side $AX$:

$$
AX = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} = \begin{pmatrix}
(1)(-1) + (2)(2) & (1)(-7) + (2)(4) \\
(0)(-1) + (1)(2) & (0)(-7) + (1)(4) \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
AX = \begin{pmatrix}
-1 + 4 & -7 + 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} = \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} = B
$$

Since $AX = B$ holds, the solution matrix $X$ is verified.
