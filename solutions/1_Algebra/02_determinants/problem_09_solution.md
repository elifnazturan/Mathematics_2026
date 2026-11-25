# Exercise 9. Area and the Determinant

## Question

We are given two vectors in $\mathbb{R}^2$ with entries $(3, 1)$ and $(1, 4)$ that span a parallelogram.

We need to:
1. Compute the area of the parallelogram using a determinant.
2. Reverse the order of the two vectors and explain what changes in the determinant and what does not change in the area.

## Solution

### 1. Computing the Area Using a Determinant

Forming a $2 \times 2$ matrix with the given vectors as columns (or rows) gives:

$$
M = \begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}
$$

The determinant of $M$ is:

$$
\det(M) = \det \begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11
$$

In $\mathbb{R}^2$, the area of the parallelogram spanned by two vectors equals the absolute value of the determinant of the matrix they form:

$$
\text{Area} = |\det(M)| = |11| = 11
$$

### 2. Reversing the Order of the Vectors

Reversing the order of the two vectors corresponds to swapping the two columns (or rows) of $M$, which produces the matrix:

$$
M_{\text{rev}} = \begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}
$$

Computing the determinant of $M_{\text{rev}}$:

$$
\det(M_{\text{rev}}) = \det \begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11
$$

What changes and what stays the same:
- **What changes (the determinant):** Swapping two columns (or rows) reverses the sign of the determinant, changing it from $+11$ to $-11$ ($\det(M_{\text{rev}}) = -\det(M)$). This reflects the change in orientation of the ordered pair of vectors.
- **What does not change (the area):** The geometric area of the parallelogram is the same two-dimensional region regardless of vector ordering, and since $|\det(M_{\text{rev}})| = |-11| = 11$, the area remains $11$.
