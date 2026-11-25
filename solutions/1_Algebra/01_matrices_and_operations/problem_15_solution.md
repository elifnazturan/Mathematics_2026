# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

We are given three matrices with sizes $2 \times 3$, $3 \times 2$, and $2 \times 2$:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}, \quad C = \begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}
$$

We need to:
1. Compute $(AB)C$ and $A(BC)$.
2. Compare the resulting matrices and the number of intermediate operations required along each calculation path.
3. Explain what associativity of matrix multiplication means in this example.

## Solution

### 1. Computing $(AB)C$

First, we compute $AB$, where $A$ is $2 \times 3$ and $B$ is $3 \times 2$, yielding a $2 \times 2$ matrix:

$$
AB = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 2 \cdot 2 + 0 \cdot (-1) & 1 \cdot 0 + 2 \cdot 1 + 0 \cdot 3 \\
0 \cdot 1 + 1 \cdot 2 + 1 \cdot (-1) & 0 \cdot 0 + 1 \cdot 1 + 1 \cdot 3 \\
\end{pmatrix} = \begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
$$

Next, we multiply $(AB)$ ($2 \times 2$) on the right by $C$ ($2 \times 2$):

$$
(AB)C = \begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix} = \begin{pmatrix}
5 \cdot 2 + 2 \cdot 0 & 5 \cdot 1 + 2 \cdot (-1) \\
1 \cdot 2 + 4 \cdot 0 & 1 \cdot 1 + 4 \cdot (-1) \\
\end{pmatrix} = \begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

### 2. Computing $A(BC)$

First, we compute $BC$, where $B$ is $3 \times 2$ and $C$ is $2 \times 2$, yielding a $3 \times 2$ matrix:

$$
BC = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 2 + 0 \cdot 0 & 1 \cdot 1 + 0 \cdot (-1) \\
2 \cdot 2 + 1 \cdot 0 & 2 \cdot 1 + 1 \cdot (-1) \\
(-1) \cdot 2 + 3 \cdot 0 & (-1) \cdot 1 + 3 \cdot (-1) \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}
$$

Next, we multiply $A$ ($2 \times 3$) on the left by $(BC)$ ($3 \times 2$), yielding a $2 \times 2$ matrix:

$$
A(BC) = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 2 + 2 \cdot 4 + 0 \cdot (-2) & 1 \cdot 1 + 2 \cdot 1 + 0 \cdot (-4) \\
0 \cdot 2 + 1 \cdot 4 + 1 \cdot (-2) & 0 \cdot 1 + 1 \cdot 1 + 1 \cdot (-4) \\
\end{pmatrix} = \begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

### 3. Comparison of Results, Intermediate Operations, and Meaning of Associativity

Both paths produce the exact same final $2 \times 2$ matrix:

$$
(AB)C = A(BC) = \begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

Counting the scalar multiplications and additions along each path:
- **Path 1 — $(AB)C$:** Computing $AB$ ($2 \times 3$ times $3 \times 2$, giving $2 \times 2$) requires $2 \times 2 \times 3 = 12$ scalar multiplications and $2 \times 2 \times 2 = 8$ additions. Multiplying the resulting $2 \times 2$ matrix by $C$ ($2 \times 2$) requires $2 \times 2 \times 2 = 8$ scalar multiplications and $2 \times 2 \times 1 = 4$ additions. In total, $(AB)C$ uses $20$ multiplications and $12$ additions.
- **Path 2 — $A(BC)$:** Computing $BC$ ($3 \times 2$ times $2 \times 2$, giving $3 \times 2$) requires $3 \times 2 \times 2 = 12$ scalar multiplications and $3 \times 2 \times 1 = 6$ additions. Multiplying $A$ ($2 \times 3$) by $(BC)$ ($3 \times 2$) requires $2 \times 2 \times 3 = 12$ scalar multiplications and $2 \times 2 \times 2 = 8$ additions. In total, $A(BC)$ uses $24$ multiplications and $14$ additions.

In this example, $(AB)C$ takes fewer intermediate arithmetic operations than $A(BC)$ because the intermediate matrix $AB$ is smaller ($2 \times 2$) than $BC$ ($3 \times 2$). Associativity of matrix multiplication means that changing the grouping (parentheses) of factors in a product does not change the final result—the order of matrices stays $A$, then $B$, then $C$, while the evaluation order and computational cost can differ.
