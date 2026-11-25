# Exercise 13. A Recurrence Written in Matrix Form

## Question

We are given the $2 \times 2$ matrix:

$$
F = \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

We need to:
1. Compute $F^2$, $F^3$, $F^4$, and $F^5$.
2. Compare the entries of these matrices with the Fibonacci sequence $0, 1, 1, 2, 3, 5, 8, \dots$ and describe the relationship observed.
3. Compute the product of $F$ with the column vector $(a, b)^T$ and explain how this multiplication performs one recurrence step by producing the sum of two consecutive terms while keeping one of them for the next step.

## Solution

### 1. Computing $F^2$, $F^3$, $F^4$, and $F^5$

First, we compute $F^2 = F \cdot F$:

$$
F^2 = \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot 1 + 1 \cdot 1 & 1 \cdot 1 + 1 \cdot 0 \\
1 \cdot 1 + 0 \cdot 1 & 1 \cdot 1 + 0 \cdot 0 \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
$$

Next, we compute $F^3 = F^2 \cdot F$:

$$
F^3 = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot 1 + 1 \cdot 1 & 2 \cdot 1 + 1 \cdot 0 \\
1 \cdot 1 + 1 \cdot 1 & 1 \cdot 1 + 1 \cdot 0 \\
\end{pmatrix} = \begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

Next, we compute $F^4 = F^3 \cdot F$:

$$
F^4 = \begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} = \begin{pmatrix}
3 \cdot 1 + 2 \cdot 1 & 3 \cdot 1 + 2 \cdot 0 \\
2 \cdot 1 + 1 \cdot 1 & 2 \cdot 1 + 1 \cdot 0 \\
\end{pmatrix} = \begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
$$

Finally, we compute $F^5 = F^4 \cdot F$:

$$
F^5 = \begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} = \begin{pmatrix}
5 \cdot 1 + 3 \cdot 1 & 5 \cdot 1 + 3 \cdot 0 \\
3 \cdot 1 + 2 \cdot 1 & 3 \cdot 1 + 2 \cdot 0 \\
\end{pmatrix} = \begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
$$

### 2. Relationship with the Sequence $0, 1, 1, 2, 3, 5, 8, \dots$

Let $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8, \dots$ denote the terms of the sequence, where each term is the sum of the two preceding terms ($f_{n+1} = f_n + f_{n-1}$).

Comparing the powers of $F$ with the terms of this sequence:

$$
F^1 = \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} = \begin{pmatrix}
f_2 & f_1 \\
f_1 & f_0 \\
\end{pmatrix}, \quad F^2 = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} = \begin{pmatrix}
f_3 & f_2 \\
f_2 & f_1 \\
\end{pmatrix}
$$

$$
F^3 = \begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix} = \begin{pmatrix}
f_4 & f_3 \\
f_3 & f_2 \\
\end{pmatrix}, \quad F^4 = \begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix} = \begin{pmatrix}
f_5 & f_4 \\
f_4 & f_3 \\
\end{pmatrix}, \quad F^5 = \begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix} = \begin{pmatrix}
f_6 & f_5 \\
f_5 & f_4 \\
\end{pmatrix}
$$

We observe that every entry of $F^n$ is a consecutive term from the sequence:
- The $(1,1)$ entry equals $f_{n+1}$.
- Both the $(1,2)$ and $(2,1)$ entries equal $f_n$.
- The $(2,2)$ entry equals $f_{n-1}$.

In general, for any integer $n \ge 1$:

$$
F^n = \begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix}
$$

### 3. Matrix-Vector Multiplication as a Recurrence Step

Now we multiply $F$ by the column vector with entries $a$ and $b$:

$$
F \begin{pmatrix}
a \\
b \\
\end{pmatrix} = \begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \begin{pmatrix}
a \\
b \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot a + 1 \cdot b \\
1 \cdot a + 0 \cdot b \\
\end{pmatrix} = \begin{pmatrix}
a + b \\
a \\
\end{pmatrix}
$$

This multiplication performs one step of the recurrence relation:
- The first row of $F$ is $(1, 1)$, so multiplying it by the vector computes $a + b$, which is the sum of the two consecutive terms $a$ and $b$.
- The second row of $F$ is $(1, 0)$, so multiplying it by the vector selects $a$ and discards $b$, keeping the more recent term $a$ for the next step.

Thus, setting $a = f_n$ and $b = f_{n-1}$ transforms the pair $(f_n, f_{n-1})^T$ into $(f_{n+1}, f_n)^T$, advancing the recurrence by one step.
