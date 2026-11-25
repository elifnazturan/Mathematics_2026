# Exercise 7. Using Properties Instead of Recomputing

## Question

We are given a $3 \times 3$ matrix $A$ such that:

$$
\det(A) = -4
$$

We need to:
1. Compute $\det(2A)$, $\det(A^T)$, $\det(A^2)$, and $\det(-A)$.
2. Justify each result using the appropriate determinant property.

## Solution

### 1. Computing $\det(2A)$

Multiplying every entry of an $n \times n$ matrix by a scalar $k$ multiplies each of its $n$ rows by $k$, so $\det(kA) = k^n \det(A)$. Since $A$ has size $n = 3$ and $k = 2$:

$$
\det(2A) = 2^3 \det(A) = 8 \cdot (-4) = -32
$$

### 2. Computing $\det(A^T)$

The determinant of the transpose of a square matrix is equal to the determinant of the original matrix ($\det(A^T) = \det(A)$):

$$
\det(A^T) = \det(A) = -4
$$

### 3. Computing $\det(A^2)$

The determinant of a product of two square matrices of the same size is the product of their determinants ($\det(AB) = \det(A)\det(B)$). Taking $B = A$ gives $\det(A^2) = (\det(A))^2$:

$$
\det(A^2) = (\det(A))^2 = (-4)^2 = 16
$$

### 4. Computing $\det(-A)$

Writing $-A = (-1)A$ for the $3 \times 3$ matrix $A$ ($n = 3$) and applying the scalar multiple property $\det(kA) = k^n \det(A)$ with $k = -1$:

$$
\det(-A) = (-1)^3 \det(A) = (-1) \cdot (-4) = 4
$$
