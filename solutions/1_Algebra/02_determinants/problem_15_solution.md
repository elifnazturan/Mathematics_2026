# Exercise 15. Combining Determinant Properties

## Question

We are given two invertible $2 \times 2$ matrices $A$ and $B$ such that:

$$
\det(A) = -2, \quad \det(B) = 3
$$

We need to:
1. Compute $\det(B^{-1} A^T B)$ without finding the entries of $A$ and $B$.
2. State the determinant properties used in order and explain why the factors involving $B$ cancel out.

## Solution

### 1. Computing $\det(B^{-1} A^T B)$ Step by Step

First, apply the product rule for determinants ($\det(XY) = \det(X)\det(Y)$ for square matrices of the same size):

$$
\det(B^{-1} A^T B) = \det(B^{-1}) \det(A^T) \det(B)
$$

Second, use the determinant property of an inverse matrix ($\det(B^{-1}) = \frac{1}{\det(B)}$) and the transpose property ($\det(A^T) = \det(A)$):

$$
\det(B^{-1} A^T B) = \frac{1}{\det(B)} \cdot \det(A) \cdot \det(B)
$$

Third, substitute $\det(A) = -2$ and $\det(B) = 3$:

$$
\det(B^{-1} A^T B) = \frac{1}{3} \cdot (-2) \cdot 3 = -2
$$

### 2. Why the Factors Involving $B$ Cancel

Although matrix multiplication is not commutative in general, determinants map matrices to real numbers, and real-number multiplication is commutative. Because $B$ is invertible with $\det(B) = 3 \neq 0$, the product brings in both $\det(B^{-1}) = \frac{1}{\det(B)}$ and $\det(B)$. Reordering the scalar factors gives:

$$
\frac{1}{\det(B)} \cdot \det(A) \cdot \det(B) = \det(A) \cdot \left(\frac{1}{\det(B)} \cdot \det(B)\right) = \det(A) \cdot 1 = \det(A) = -2
$$

Thus, the $\det(B)$ and $\frac{1}{\det(B)}$ factors multiply to $1$ and cancel out completely.
