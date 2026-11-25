# Exercise 8. Determinant of a Product

## Question

We are given two square matrices $A$ and $B$ of the same size such that:

$$
\det(A) = 3, \quad \det(B) = -5
$$

We need to:
1. Compute $\det(AB)$, $\det(BA)$, and (if it exists) $\det(A^{-1}B)$.
2. Explain why $\det(AB) = \det(BA)$ even though matrix multiplication is generally not commutative ($AB \neq BA$).

## Solution

### 1. Computing $\det(AB)$, $\det(BA)$, and $\det(A^{-1}B)$

For any two square matrices $A$ and $B$ of the same size, the determinant of their product equals the product of their determinants:

$$
\det(AB) = \det(A)\det(B)
$$

Substituting $\det(A) = 3$ and $\det(B) = -5$:

$$
\det(AB) = 3 \cdot (-5) = -15
$$

Applying the same product rule in the reverse order gives:

$$
\det(BA) = \det(B)\det(A)
$$

Because scalar multiplication of real numbers is commutative, we get:

$$
\det(BA) = (-5) \cdot 3 = -15
$$

Next, check whether $A^{-1}$ exists. Since $\det(A) = 3 \neq 0$, matrix $A$ is invertible, and its inverse satisfies:

$$
\det(A^{-1}) = \frac{1}{\det(A)} = \frac{1}{3}
$$

Therefore, $A^{-1}B$ is well-defined, and applying the product rule gives:

$$
\det(A^{-1}B) = \det(A^{-1})\det(B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}
$$

### 2. Why $\det(AB) = \det(BA)$ When Usually $AB \neq BA$

In general, matrix multiplication is not commutative, meaning $AB$ and $BA$ are usually different matrices. However, $\det(\cdot)$ maps a square matrix to a single real scalar. Even when the entries and structure of $AB$ and $BA$ differ, their determinants satisfy:

$$
\det(AB) = \det(A)\det(B) = \det(B)\det(A) = \det(BA)
$$

Since $\det(A)$ and $\det(B)$ are ordinary numbers, they commute under multiplication ($\det(A)\det(B) = \det(B)\det(A)$), so the resulting scalar determinants are always equal.
