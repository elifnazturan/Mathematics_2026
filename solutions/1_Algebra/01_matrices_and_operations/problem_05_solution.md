# Exercise 5. Matrix-Vector Product

## Question

We are given a $2 \times 2$ matrix $A$ and a $2 \times 1$ column vector $X$:

$$
A = \begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
$$

$$
X = \begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

We need to compute the product $AX$ and then express $AX$ as a linear combination of the columns of $A$, using the components of $X$ as coefficients.

## Solution

### 1. Direct Matrix-Vector Multiplication

First, we check the dimensions. Matrix $A$ has size $2 \times 2$ and vector $X$ has size $2 \times 1$. Since the number of columns in $A$ equals the number of rows in $X$, the product $AX$ is defined and results in a $2 \times 1$ vector.

Using the definition of matrix-vector multiplication:

$$
AX = \begin{pmatrix}
2 \cdot 4 + (-1) \cdot 2 \\
1 \cdot 4 + 3 \cdot 2 \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
AX = \begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}
$$

$$
AX = \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

### 2. Linear Combination of the Columns of $A$

Let $a_1$ and $a_2$ be the first and second columns of matrix $A$:

$$
a_1 = \begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

$$
a_2 = \begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

Using the entries $x_1 = 4$ and $x_2 = 2$ of vector $X$ as scalar weights, we write $AX$ as a linear combination of $a_1$ and $a_2$:

$$
AX = 4a_1 + 2a_2
$$

Substituting the column vectors:

$$
AX = 4 \begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2 \begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

Multiplying each vector by its scalar coefficient:

$$
AX = \begin{pmatrix}
8 \\
4 \\
\end{pmatrix} + \begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
$$

Adding the resulting vectors component by component:

$$
AX = \begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}
$$

$$
AX = \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

### 3. Verification and Final Answer

Both direct multiplication and the linear combination of columns yield the exact same result, confirming that multiplying a matrix by a vector corresponds to taking a linear combination of its columns.

The product is:

$$
AX = \begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

Written as a linear combination of the columns of $A$:

$$
AX = 4 \begin{pmatrix}
2 \\
1 \\
\end{pmatrix} + 2 \begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$
