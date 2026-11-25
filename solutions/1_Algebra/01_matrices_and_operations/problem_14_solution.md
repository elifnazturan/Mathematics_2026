# Exercise 14. Rotation Matrices

## Question

We are given the $2 \times 2$ rotation matrix for a counterclockwise rotation through an angle $\theta$:

$$
R(\theta) = \begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{pmatrix}
$$

We need to:
1. Compute the matrix product $R(\alpha)R(\beta)$ for two angles $\alpha$ and $\beta$.
2. Use the trigonometric angle-sum identities for sine and cosine to show that $R(\alpha)R(\beta) = R(\alpha + \beta)$.
3. Explain the geometric meaning of this identity.

## Solution

### 1. Computing $R(\alpha)R(\beta)$

Writing out $R(\alpha)$ and $R(\beta)$ using the definition of $R(\theta)$:

$$
R(\alpha) = \begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{pmatrix}, \quad R(\beta) = \begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Multiplying $R(\alpha)$ by $R(\beta)$ gives:

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha
\end{pmatrix} \begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta
\end{pmatrix}
$$

Computing each entry of the $2 \times 2$ product matrix:

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\
\sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta
\end{pmatrix}
$$

Factoring $-1$ out of the $(1,2)$ entry and reordering terms in the $(2,2)$ entry:

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\
\sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta
\end{pmatrix}
$$

### 2. Applying the Angle-Sum Identities

Recall the trigonometric angle-sum formulas:

$$
\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

$$
\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta
$$

Substituting these two identities directly into the entries of $R(\alpha)R(\beta)$ yields:

$$
R(\alpha)R(\beta) = \begin{pmatrix}
\cos(\alpha + \beta) & -\sin(\alpha + \beta) \\
\sin(\alpha + \beta) & \cos(\alpha + \beta)
\end{pmatrix}
$$

By definition of the rotation matrix $R(\theta)$ with $\theta = \alpha + \beta$, the right-hand side is equal to $R(\alpha + \beta)$. Therefore,

$$
R(\alpha)R(\beta) = R(\alpha + \beta)
$$

### 3. Geometric Explanation

Applying the product $R(\alpha)R(\beta)$ to a vector $v$ means first rotating $v$ counterclockwise around the origin by an angle $\beta$ (giving $R(\beta)v$), and then rotating the resulting vector counterclockwise around the origin by an additional angle $\alpha$, which yields $R(\alpha)(R(\beta)v)$. Performing two consecutive counterclockwise rotations in the plane by $\beta$ and then by $\alpha$ produces the exact same final position as performing a single counterclockwise rotation through the total angle $\alpha + \beta$, which is represented by $R(\alpha + \beta)$. Furthermore, since $\alpha + \beta = \beta + \alpha$, planar rotations commute, meaning $R(\alpha)R(\beta) = R(\beta)R(\alpha)$.
