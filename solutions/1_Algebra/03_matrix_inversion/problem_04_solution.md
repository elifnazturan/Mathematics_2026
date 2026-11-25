# Exercise 4. Gauss--Jordan

## Question

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
$$

We need to:
1. Find $A^{-1}$ using the Gauss--Jordan method.
2. Show the augmented matrix $[A \mid I]$ after successive row operations.
3. Explain why obtaining $I$ on the left side of the augmented matrix gives $A^{-1}$ on the right side.

## Solution

### 1. Gauss--Jordan Elimination on $[A \mid I_2]$

We form the augmented matrix $[A \mid I_2]$ by placing the $2 \times 2$ identity matrix $I_2$ next to $A$:

$$
[A \mid I_2] = \left(\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1 \\
\end{array}\right)
$$

First, eliminate the entry below the leading $1$ in the first column by applying $R_2 \leftarrow R_2 - 3R_1$:

$$
\left(\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1 \\
\end{array}\right)
$$

Next, scale the second row by $-1$ ($R_2 \leftarrow -1 \cdot R_2$) so the second pivot becomes $1$:

$$
\left(\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1 \\
\end{array}\right)
$$

Finally, eliminate the entry above the second pivot by applying $R_1 \leftarrow R_1 - 2R_2$:

$$
\left(\begin{array}{cc|cc}
1 & 0 & -5 & 2 \\
0 & 1 & 3 & -1 \\
\end{array}\right)
$$

Now the left block is $I_2$ and the right block is $A^{-1}$:

$$
A^{-1} = \begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

### 2. Why Reaching $[I_2 \mid A^{-1}]$ Yields the Inverse on the Right

Each elementary row operation on a matrix is equivalent to multiplying on the left by an invertible elementary matrix $E_k$. Performing $m$ successive row operations on $[A \mid I_n]$ multiplies both blocks on the left by the product of elementary matrices $E = E_m \cdots E_2 E_1$:

$$
E[A \mid I_n] = [EA \mid EI_n] = [EA \mid E]
$$

When the row operations reduce the left side to the identity matrix $I_n$, we have:

$$
EA = I_n
$$

For a square matrix $A$, the left-inverse condition $EA = I_n$ implies $E = A^{-1}$ (and $AE = I_n$ as well). Since the right side started as $I_n$ and underwent the exact same left-multiplications, it becomes $EI_n = E = A^{-1}$.
