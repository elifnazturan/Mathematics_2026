
# Exercise 4 – Matrix Multiplication and Noncommutativity

## Question

Given the following matrices:

$$
A =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

The tasks are:

1. Calculate the products $AB$ and $BA$.
2. Determine whether $AB = BA$.
3. Explain what noncommutativity of matrix multiplication means using this example.

## Solution

### 1. Calculating the Product AB

To calculate $AB$, I multiply each row of matrix $A$ by each column of matrix $B$.

$$
AB =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Calculating each entry:

$$
AB =
\begin{pmatrix}
1 \cdot 2 + 2 \cdot 3 & 1 \cdot 0 + 2 \cdot 1 \\
0 \cdot 2 + 1 \cdot 3 & 0 \cdot 0 + 1 \cdot 1 \\
\end{pmatrix}
$$

After performing the calculations:

$$
AB =
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

### 2. Calculating the Product BA

Now I reverse the order and multiply matrix $B$ by matrix $A$.

$$
BA =
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

I multiply each row of $B$ by each column of $A$.

$$
BA =
\begin{pmatrix}
2 \cdot 1 + 0 \cdot 0 & 2 \cdot 2 + 0 \cdot 1 \\
3 \cdot 1 + 1 \cdot 0 & 3 \cdot 2 + 1 \cdot 1 \\
\end{pmatrix}
$$

After performing the calculations:

$$
BA =
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

### 3. Comparing AB and BA

The two results are:

$$
AB =
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

The corresponding entries are different, so:

$$
AB \neq BA
$$

### 4. Explanation of Noncommutativity

Matrix multiplication is not commutative in general. This means that changing the order of two matrices can give a different result.

In this example, both products are defined because both matrices have the same size, but their results are different.

Therefore, this example shows that the order of matrix multiplication matters. Unlike ordinary multiplication of numbers, switching the order of matrices does not necessarily give the same result.

## Final Answer

$$
AB =
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

$$
\boxed{AB \neq BA}
$$

Matrix multiplication is not commutative in this example.
