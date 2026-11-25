# Exercise 6. Parameter and Invertibility

## Question

We are given a $2 \times 2$ matrix depending on a parameter $t$:

$$
A(t) = \begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

We need to:
1. Find all values of $t$ for which the matrix $A(t)$ is not invertible.
2. Explain how this result is connected to the condition $\det(A(t)) = 0$.

## Solution

### 1. Computing the Determinant and Finding Non-Invertible Values of $t$

Using the determinant formula for a $2 \times 2$ matrix, we compute $\det(A(t))$:

$$
\det(A(t)) = \det \begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix} = t \cdot t - 1 \cdot 2 = t^2 - 2
$$

A square matrix is not invertible (singular) precisely when its determinant is zero. Setting $\det(A(t)) = 0$ gives:

$$
t^2 - 2 = 0
$$

Solving for $t$:

$$
t^2 = 2
$$

$$
t = \sqrt{2}, \quad t = -\sqrt{2}
$$

Therefore, $A(t)$ is not invertible for $t = -\sqrt{2}$ and $t = \sqrt{2}$ (equivalently, $t = \pm\sqrt{2}$).

### 2. Connection Between Non-Invertibility and $\det(A(t)) = 0$

For any square matrix, invertibility is directly equivalent to having a nonzero determinant ($\det \neq 0$). When $\det(A(t)) = t^2 - 2 = 0$, the determinant vanishes, so $A(t)$ has no inverse matrix. When $t = \pm\sqrt{2}$, the rows (and columns) of $A(t)$ become linearly dependent—specifically, the first row $(t, 1)$ is a scalar multiple of the second row $(2, t)$ by the factor $\frac{t}{2} = \pm\frac{\sqrt{2}}{2}$. Because the rows are linearly dependent, $A(t)$ is singular for $t = \pm\sqrt{2}$, whereas for all $t \neq \pm\sqrt{2}$ we have $\det(A(t)) \neq 0$ and $A(t)$ is invertible.
