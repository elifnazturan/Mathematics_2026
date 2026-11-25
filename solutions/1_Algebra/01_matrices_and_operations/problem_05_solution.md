
# Exercise 5 – Matrix Times Vector

## Question

Given the matrix and vector:

$$
A =
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
$$

$$
x =
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

The tasks are:

1. Calculate the product $Ax$.
2. Express $Ax$ as a linear combination of the columns of matrix $A$, using the coefficients from vector $x$.

## Solution

### 1. Calculating the Product Ax

To calculate $Ax$, I multiply each row of matrix $A$ by the vector $x$.

$$
Ax =
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

I calculate each entry separately:

$$
Ax =
\begin{pmatrix}
2 \cdot 4 + (-1) \cdot 2 \\
1 \cdot 4 + 3 \cdot 2 \\
\end{pmatrix}
$$

After performing the calculations:

$$
Ax =
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}
$$

Therefore:

$$
Ax =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

### 2. Expressing Ax as a Linear Combination of Columns

First, I write the columns of matrix $A$ separately.

The first column is:

$$
a_1 =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

The second column is:

$$
a_2 =
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

The vector $x$ contains the coefficients 4 and 2. Therefore, I can express the product as:

$$
Ax = 4a_1 + 2a_2
$$

Substituting the column vectors:

$$
Ax =
4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+
2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

Multiplying each vector by its coefficient:

$$
Ax =
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
$$

Adding the vectors:

$$
Ax =
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

### 3. Verification

The result from the linear combination is the same as the result from the matrix multiplication.

$$
Ax =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

Both methods give the same answer, so the calculation is correct.

## Final Answer

$$
Ax =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

The linear combination of the columns of $A$ is:

$$
Ax = 4a_1 + 2a_2
$$

This shows that multiplying a matrix by a vector is equivalent to taking a linear combination of the matrix columns, using the entries of the vector as coefficients.
