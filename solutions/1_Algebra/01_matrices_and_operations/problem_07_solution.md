# Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

We are given a $2 \times 2$ upper triangular matrix:

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

Using the $2 \times 2$ identity matrix $I$ and the $2 \times 2$ zero matrix $0$, we need to:
1. Compute $AI$, $IA$, $A + 0$, $A^2$, and $A^3$.
2. Explain the roles of the matrices $I$ and $0$.
3. Describe the pattern observed in successive powers of $A$.

## Solution

Since $A$ has size $2 \times 2$, the corresponding identity matrix $I$ and zero matrix $0$ are:

$$
I = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

$$
0 = \begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

### 1. Computing $AI$, $IA$, and $A + 0$

Multiplying $A$ on the right by $I$:

$$
AI = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot 1 + 1 \cdot 0 & 2 \cdot 0 + 1 \cdot 1 \\
0 \cdot 1 + 2 \cdot 0 & 0 \cdot 0 + 2 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

Multiplying $A$ on the left by $I$:

$$
IA = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 2 + 0 \cdot 0 & 1 \cdot 1 + 0 \cdot 2 \\
0 \cdot 2 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

Adding the zero matrix $0$ to $A$:

$$
A + 0 = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} + \begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix} = \begin{pmatrix}
2 + 0 & 1 + 0 \\
0 + 0 & 2 + 0 \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

### 2. Computing $A^2$ and $A^3$

For $A^2 = A \cdot A$:

$$
A^2 = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot 2 + 1 \cdot 0 & 2 \cdot 1 + 1 \cdot 2 \\
0 \cdot 2 + 2 \cdot 0 & 0 \cdot 1 + 2 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

For $A^3 = A^2 \cdot A$:

$$
A^3 = \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
4 \cdot 2 + 4 \cdot 0 & 4 \cdot 1 + 4 \cdot 2 \\
0 \cdot 2 + 4 \cdot 0 & 0 \cdot 1 + 4 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

### 3. Roles of $I$ and $0$

- **Identity matrix $I$:** Acts as the multiplicative neutral element for matrices, just like the number $1$ in scalar multiplication. Multiplying $A$ by $I$ from either side leaves $A$ unchanged ($AI = IA = A$).
- **Zero matrix $0$:** Acts as the additive neutral element for matrices, just like the number $0$ in scalar addition. Adding $0$ to $A$ leaves every entry unchanged ($A + 0 = A$).

### 4. Pattern in Successive Powers of $A$

Comparing the powers of $A$:

$$
A^1 = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}, \quad A^2 = \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}, \quad A^3 = \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

We observe a clear pattern for any positive integer $n$:
- The main diagonal entries are equal to $2^n$ ($2^1 = 2$, $2^2 = 4$, $2^3 = 8$).
- The bottom-left entry remains $0$, so the matrix stays upper triangular.
- The top-right entry equals $n \cdot 2^{n-1}$ ($1 \cdot 2^0 = 1$, $2 \cdot 2^1 = 4$, $3 \cdot 2^2 = 12$).

In general, for any integer $n \ge 1$:

$$
A^n = \begin{pmatrix}
2^n & n \cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$
