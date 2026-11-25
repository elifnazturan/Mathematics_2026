# Exercise 3. Swapping Two Rows

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

We need to:
1. Compute $\det(A)$.
2. Form the matrix $B$ by swapping the first and second rows of $A$.
3. First predict $\det(B)$ using a determinant property, and then verify the prediction by direct calculation.

## Solution

### 1. Computing $\det(A)$

Using Sarrus' rule on matrix $A$, we sum the products along the three downward-right diagonals:

$$
1 \cdot 3 \cdot 1 = 3
$$

$$
2 \cdot 1 \cdot 2 = 4
$$

$$
0 \cdot 0 \cdot 1 = 0
$$

Their sum is:

$$
3 + 4 + 0 = 7
$$

Next, we compute the products along the three upward-right diagonals:

$$
2 \cdot 3 \cdot 0 = 0
$$

$$
1 \cdot 1 \cdot 1 = 1
$$

$$
1 \cdot 0 \cdot 2 = 0
$$

Their sum is:

$$
0 + 1 + 0 = 1
$$

Subtracting the upward-right sum from the downward-right sum gives:

$$
\det(A) = 7 - 1 = 6
$$

### 2. Forming Matrix $B$ and Predicting $\det(B)$

Swapping the first row $(1, 2, 0)$ and the second row $(0, 3, 1)$ of $A$ gives the matrix $B$:

$$
B = \begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

By the determinant property that interchanging two rows of a square matrix changes the sign of its determinant ($\det(B) = -\det(A)$), we predict:

$$
\det(B) = -6
$$

### 3. Verifying $\det(B)$ by Calculation

Now we compute $\det(B)$ directly using Sarrus' rule. First, the downward-right diagonal products are:

$$
0 \cdot 2 \cdot 1 = 0
$$

$$
3 \cdot 0 \cdot 2 = 0
$$

$$
1 \cdot 1 \cdot 1 = 1
$$

Their sum is:

$$
0 + 0 + 1 = 1
$$

Next, the upward-right diagonal products are:

$$
2 \cdot 2 \cdot 1 = 4
$$

$$
1 \cdot 0 \cdot 0 = 0
$$

$$
1 \cdot 1 \cdot 3 = 3
$$

Their sum is:

$$
4 + 0 + 3 = 7
$$

Subtracting the two sums gives:

$$
\det(B) = 1 - 7 = -6
$$

The direct calculation gives $\det(B) = -6$, which matches our prediction from the row-swap property.
