# Exercise 10. Columns of a Matrix Product

## Question

We are given a $2 \times 3$ matrix $A$ and a $3 \times 2$ matrix $B$:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

$$
B = \begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Denoting the columns of $B$ by $b_1$ and $b_2$, we need to:
1. Compute $Ab_1$ and $Ab_2$.
2. Compute the product matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are equal to the vectors $Ab_1$ and $Ab_2$.

## Solution

### 1. Computing $Ab_1$ and $Ab_2$

The columns of $B$ are the $3 \times 1$ vectors:

$$
b_1 = \begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}, \quad b_2 = \begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

Multiplying $A$ ($2 \times 3$) by $b_1$ ($3 \times 1$) gives a $2 \times 1$ vector:

$$
Ab_1 = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 2 \cdot (-1) + 0 \cdot 3 \\
0 \cdot 1 + 1 \cdot (-1) + 1 \cdot 3 \\
\end{pmatrix} = \begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix} = \begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
$$

Multiplying $A$ ($2 \times 3$) by $b_2$ ($3 \times 1$) gives a $2 \times 1$ vector:

$$
Ab_2 = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 2 + 2 \cdot 0 + 0 \cdot 1 \\
0 \cdot 2 + 1 \cdot 0 + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix} = \begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

### 2. Computing the Matrix Product $AB$

Since $A$ has size $2 \times 3$ and $B$ has size $3 \times 2$, the product $AB$ has size $2 \times 2$:

$$
AB = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 2 \cdot (-1) + 0 \cdot 3 & 1 \cdot 2 + 2 \cdot 0 + 0 \cdot 1 \\
0 \cdot 1 + 1 \cdot (-1) + 1 \cdot 3 & 0 \cdot 2 + 1 \cdot 0 + 1 \cdot 1 \\
\end{pmatrix}
$$

Simplifying each entry gives:

$$
AB = \begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

### 3. Comparison and Explanation

Placing $Ab_1$ and $Ab_2$ side by side as columns forms the matrix:

$$
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix} = \begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix} = AB
$$

Each column $j$ of the product $AB$ is obtained by taking the dot products of the rows of $A$ with the $j$-th column of $B$. By definition of matrix-vector multiplication, taking the dot products of the rows of $A$ with column $b_j$ of $B$ is identical to computing the vector $Ab_j$. Therefore, $AB$ can be written column by column as:

$$
AB = \begin{pmatrix}
Ab_1 & Ab_2 & \cdots & Ab_k \\
\end{pmatrix}
$$

which in this case gives:

$$
AB = \begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}
$$
