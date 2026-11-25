# Exercise 12. Formula for a Matrix Power

## Question

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

We need to:
1. Compute $A^2$, $A^3$, and $A^4$.
2. Use these results to formulate a general conjecture for $A^n$ (for any positive integer $n$).
3. Prove the conjecture rigorously by assuming the formula holds for $n$, multiplying by $A$, and explaining why the resulting matrix matches the formula for $n + 1$.

## Solution

### 1. Computing $A^2$, $A^3$, and $A^4$

First, we compute $A^2 = A \cdot A$:

$$
A^2 = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 1 \cdot 0 & 1 \cdot 1 + 1 \cdot 1 \\
0 \cdot 1 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

Next, we compute $A^3 = A^2 \cdot A$:

$$
A^3 = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 2 \cdot 0 & 1 \cdot 1 + 2 \cdot 1 \\
0 \cdot 1 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
$$

Next, we compute $A^4 = A^3 \cdot A$:

$$
A^4 = \begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 3 \cdot 0 & 1 \cdot 1 + 3 \cdot 1 \\
0 \cdot 1 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
$$

### 2. Conjecture for $A^n$

Comparing the computed powers:

$$
A^1 = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}, \quad A^2 = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad A^3 = \begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}, \quad A^4 = \begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
$$

In each step, the main diagonal entries stay equal to $1$, the bottom-left entry remains $0$, and the top-right entry equals the exponent $n$. Therefore, we formulate the conjecture that for every integer $n \ge 1$:

$$
A^n = \begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

### 3. Proof by Mathematical Induction

- **Base case ($n = 1$):** Substituting $n = 1$ into the conjectured formula gives:

$$
A^1 = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

which matches the given matrix $A$.

- **Inductive step:** Assume that the formula holds for some positive integer $n$, meaning:

$$
A^n = \begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

To find $A^{n+1}$, we multiply $A^n$ by $A$:

$$
A^{n+1} = A^n \cdot A = \begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Performing the matrix multiplication entry by entry:

$$
A^{n+1} = \begin{pmatrix}
1 \cdot 1 + n \cdot 0 & 1 \cdot 1 + n \cdot 1 \\
0 \cdot 1 + 1 \cdot 0 & 0 \cdot 1 + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & n + 1 \\
0 & 1 \\
\end{pmatrix}
$$

This works because multiplying on the right by $A$ leaves the first column unchanged, while the new top-right entry becomes $1 \cdot 1 + n \cdot 1 = n + 1$, adding $1$ to the previous top-right entry $n$. This is the exact formula for $n + 1$. By mathematical induction, for all integers $n \ge 1$:

$$
A^n = \begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$
