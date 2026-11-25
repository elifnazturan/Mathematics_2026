# Exercise 11. Parameter and Invertibility

## Question

We are given the $2 \times 2$ matrix depending on a parameter $t$:

$$
A(t) = \begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

We need to:
1. Find all values of $t$ for which the matrix $A(t)$ is invertible.
2. Give a formula for $A(t)^{-1}$ when it exists.
3. Explain what happens to this formula at the excluded values of $t$.

## Solution

### 1. Finding All $t$ for Which $A(t)$ Is Invertible

A $2 \times 2$ matrix is invertible if and only if its determinant is nonzero. Computing the determinant of $A(t)$:

$$
\det(A(t)) = (1)(1) - (t)(t) = 1 - t^2
$$

For $A(t)$ to be invertible, we require $\det(A(t)) \neq 0$:

$$
1 - t^2 \neq 0 \quad \Longleftrightarrow \quad t^2 \neq 1 \quad \Longleftrightarrow \quad t \neq 1 \text{ and } t \neq -1
$$

Thus, $A(t)$ is invertible for all $t \in \mathbb{R} \setminus \{-1, 1\}$.

### 2. Formula for $A(t)^{-1}$

For any $t \neq \pm 1$, we have $\det(A(t)) = 1 - t^2 \neq 0$. Applying the inverse formula for a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \\ \end{pmatrix}$ with $a = 1$, $b = t$, $c = t$, and $d = 1$:

$$
A(t)^{-1} = \frac{1}{\det(A(t))} \begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix} = \frac{1}{1 - t^2} \begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\
-\frac{t}{1 - t^2} & \frac{1}{1 - t^2} \\
\end{pmatrix}
$$

### 3. What Happens at the Excluded Values $t = 1$ and $t = -1$

In the formula for $A(t)^{-1}$, the factor $\frac{1}{1 - t^2}$ has denominator $1 - t^2$:

- When $t = 1$, we have $1 - t^2 = 1 - 1^2 = 0$, so division by zero occurs in $\frac{1}{1 - t^2}$. Geometrically and algebraically, $A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \\ \end{pmatrix}$ has two identical rows, so its rows are linearly dependent and the matrix is singular (noninvertible).
- When $t = -1$, we also have $1 - t^2 = 1 - (-1)^2 = 0$, again causing division by zero in the inverse formula. Here $A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \\ \end{pmatrix}$ has its second row equal to $(-1)$ times its first row, so the rows are linearly dependent and $A(-1)$ is also noninvertible.

Therefore, at $t = \pm 1$, the inverse formula breaks down due to division by zero precisely because $\det(A(\pm 1)) = 0$ and no inverse matrix exists.
