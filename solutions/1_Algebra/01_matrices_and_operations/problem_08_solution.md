# Exercise 8. Row Operations and Their Reversibility

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

We need to perform the following three elementary row operations in order:
1. $R_2 \leftarrow R_2 - 2R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. Interchange $R_2$ and $R_3$.

After performing these operations, we must write the resulting matrix after each step and state the inverse row operation that reverses each of the three steps.

## Solution

### 1. Performing the Row Operations

Let $A_0 = A$ denote the initial matrix before any operations are applied.

#### Step 1: $R_2 \leftarrow R_2 - 2R_1$

We subtract $2$ times the first row from the second row:

$$
R_2^{\mathrm{new}} = (2, 4, 1) - 2(1, 2, -1) = (2 - 2, 4 - 4, 1 - (-2)) = (0, 0, 3)
$$

Rows $R_1$ and $R_3$ remain unchanged, so the matrix after Step 1 is:

$$
A_1 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

#### Step 2: $R_3 \leftarrow R_3 + R_1$

Using $A_1$, we add the first row to the third row:

$$
R_3^{\mathrm{new}} = (-1, 1, 3) + (1, 2, -1) = (-1 + 1, 1 + 2, 3 + (-1)) = (0, 3, 2)
$$

Rows $R_1$ and $R_2$ remain unchanged, so the matrix after Step 2 is:

$$
A_2 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

#### Step 3: Interchange $R_2$ and $R_3$

Using $A_2$, we swap the second and third rows ($R_2 \leftrightarrow R_3$), while $R_1$ stays unchanged. The matrix after Step 3 is:

$$
A_3 = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

### 2. Reversing Each Row Operation

Every elementary row operation is invertible and can be undone by a corresponding inverse row operation:

- **Reversing Step 1 ($R_2 \leftarrow R_2 - 2R_1$):** Since $2R_1$ was subtracted from $R_2$ while $R_1$ stayed fixed, we add $2R_1$ back to $R_2$:

$$
R_2 \leftarrow R_2 + 2R_1
$$

- **Reversing Step 2 ($R_3 \leftarrow R_3 + R_1$):** Since $R_1$ was added to $R_3$ while $R_1$ stayed fixed, we subtract $R_1$ from $R_3$:

$$
R_3 \leftarrow R_3 - R_1
$$

- **Reversing Step 3 ($R_2 \leftrightarrow R_3$):** Swapping two rows is its own inverse, so we interchange $R_2$ and $R_3$ again:

$$
R_2 \leftrightarrow R_3
$$

Applying these inverse operations in reverse order (Step 3 inverse, then Step 2 inverse, then Step 1 inverse) transforms $A_3$ back to the original matrix $A$.
