# Exercise 6. Transpose

## Question

We are given two matrices:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
$$

$$
B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

We need to compute $A^T$, $B^T$, and $AB$, and then verify for these matrices that $(AB)^T = B^T A^T$. The purpose of this exercise is to practice matrix transposition and verify the property that transposing a product reverses the order of multiplication.
## Solution

### 1. Transposes of $A$ and $B$

The transpose of a matrix is obtained by swapping its rows and columns so that the $(i, j)$ entry becomes the $(j, i)$ entry. Matrix $A$ has size $2 \times 3$, so $A^T$ has size $3 \times 2$:

$$
A^T = \begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

Matrix $B$ has size $3 \times 2$, so $B^T$ has size $2 \times 3$:

$$
B^T = \begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

### 2. Product $AB$

Matrix $A$ has size $2 \times 3$ and matrix $B$ has size $3 \times 2$. Since the inner dimension is $3$ in both cases, the product $AB$ is defined and has size $2 \times 2$. Each entry $(AB)_{ij}$ is the dot product of row $i$ of $A$ and column $j$ of $B$:

$$
AB = \begin{pmatrix}
1 \cdot 1 + 2 \cdot 2 + 3 \cdot (-1) & 1 \cdot 0 + 2 \cdot 1 + 3 \cdot 3 \\
4 \cdot 1 + 5 \cdot 2 + 6 \cdot (-1) & 4 \cdot 0 + 5 \cdot 1 + 6 \cdot 3 \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
AB = \begin{pmatrix}
1 + 4 - 3 & 0 + 2 + 9 \\
4 + 10 - 6 & 0 + 5 + 18 \\
\end{pmatrix}
$$

$$
AB = \begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
$$

### 3. Verification of $(AB)^T = B^T A^T$

Transposing the $2 \times 2$ matrix $AB$ gives:

$$
(AB)^T = \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

Now we compute $B^T A^T$, where $B^T$ has size $2 \times 3$ and $A^T$ has size $3 \times 2$, producing a $2 \times 2$ result:

$$
B^T A^T = \begin{pmatrix}
1 \cdot 1 + 2 \cdot 2 + (-1) \cdot 3 & 1 \cdot 4 + 2 \cdot 5 + (-1) \cdot 6 \\
0 \cdot 1 + 1 \cdot 2 + 3 \cdot 3 & 0 \cdot 4 + 1 \cdot 5 + 3 \cdot 6 \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
B^T A^T = \begin{pmatrix}
1 + 4 - 3 & 4 + 10 - 6 \\
0 + 2 + 9 & 0 + 5 + 18 \\
\end{pmatrix}
$$

$$
B^T A^T = \begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

Since both expressions yield the exact same $2 \times 2$ matrix, $(AB)^T = B^T A^T$ is verified for this example.
