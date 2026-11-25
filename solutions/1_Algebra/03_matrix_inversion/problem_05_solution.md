# Exercise 5. A 3x3 Matrix

## Question

We are given the $3 \times 3$ matrix:

$$
A = \begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
$$

We need to:
1. Find $A^{-1}$ using Gauss--Jordan elimination.
2. Check the result by matrix multiplication.

## Solution

### 1. Gauss--Jordan Elimination on $[A \mid I_3]$

We form the augmented matrix $[A \mid I_3]$ with the $3 \times 3$ identity matrix on the right:

$$
[A \mid I_3] = \left(\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1 \\
\end{array}\right)
$$

First, eliminate the entry in row $3$, column $1$ using $R_3 \leftarrow R_3 - R_1$:

$$
\left(\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1 \\
\end{array}\right)
$$

Next, use the pivot $1$ in row $2$, column $2$ to eliminate the entry below it via $R_3 \leftarrow R_3 + R_2$:

$$
\left(\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1 \\
\end{array}\right)
$$

Scale row $3$ by $\frac{1}{2}$ ($R_3 \leftarrow \frac{1}{2} R_3$) to make the third pivot equal to $1$:

$$
\left(\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{array}\right)
$$

Now back-substitute upward using the third pivot. Apply $R_2 \leftarrow R_2 - R_3$:

$$
\left(\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{array}\right)
$$

Finally, eliminate the entry in row $1$, column $2$ via $R_1 \leftarrow R_1 - R_2$:

$$
\left(\begin{array}{ccc|ccc}
1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{array}\right)
$$

Since the left side is $I_3$, the right side is $A^{-1}$:

$$
A^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix} = \frac{1}{2} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
$$

### 2. Checking by Multiplication

We verify that $A A^{-1} = I_3$:

$$
A A^{-1} = \begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix} \cdot \frac{1}{2} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
$$

First, multiply the matrices without the $\frac{1}{2}$ factor:

$$
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 + 1 + 0 & -1 + 1 + 0 & 1 - 1 + 0 \\
0 + 1 - 1 & 0 + 1 + 1 & 0 - 1 + 1 \\
1 + 0 - 1 & -1 + 0 + 1 & 1 + 0 + 1 \\
\end{pmatrix} = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix}
$$

Multiplying every entry by $\frac{1}{2}$ yields:

$$
A A^{-1} = \frac{1}{2} \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} = I_3
$$

Thus, $A A^{-1} = I_3$ confirms that our inverse matrix is correct.
