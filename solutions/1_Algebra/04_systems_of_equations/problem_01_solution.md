# Exercise 1. From a System to a Matrix

## Question

We are given the linear system of three equations in three unknowns:

$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

We need to:
1. Write the system in the form $Ax = b$.
2. Identify the coefficient matrix $A$, the vector of unknowns $x$, and the right-hand side vector $b$.
3. Explain how each row of the matrix equation corresponds to one equation of the system.

## Solution

### 1. System in Matrix Form $Ax = b$

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix} =
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

### 2. Identification of $A$, $x$, and $b$

The coefficient matrix $A$ is

$$
A =
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
$$

The vector of unknowns $x$ is

$$
x =
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
$$

The right-hand side vector $b$ is

$$
b =
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

### 3. Correspondence Between Rows and Equations

By the definition of matrix-vector multiplication, the $i$-th entry of the product $Ax$ is the dot product of the $i$-th row of $A$ with the column vector $x$, and setting this equal to the $i$-th entry of $b$ yields the $i$-th equation:

- **Row 1:** Multiplying $(2, -1, 1)$ by $(x, y, z)^T$ gives $2x - y + z$, and equating it to the first entry of $b$ produces the first equation $2x - y + z = 4$.
- **Row 2:** Multiplying $(1, 3, -2)$ by $(x, y, z)^T$ gives $x + 3y - 2z$, and equating it to the second entry of $b$ produces the second equation $x + 3y - 2z = 1$.
- **Row 3:** Multiplying $(3, 1, 1)$ by $(x, y, z)^T$ gives $3x + y + z$, and equating it to the third entry of $b$ produces the third equation $3x + y + z = 7$.
