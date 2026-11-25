# Exercise 11. When Do Matrices Commute?

## Question

We are given two $2 \times 2$ matrices:

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

$$
B = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

We need to:
1. Find the conditions on $a, b, c, d$ under which $AB = BA$.
2. Describe the general form of all such matrices $B$ that commute with $A$.

## Solution

### 1. Computing $AB$ and $BA$

First, we compute the product $AB$:

$$
AB = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} = \begin{pmatrix}
1 \cdot a + 1 \cdot c & 1 \cdot b + 1 \cdot d \\
0 \cdot a + 1 \cdot c & 0 \cdot b + 1 \cdot d \\
\end{pmatrix} = \begin{pmatrix}
a + c & b + d \\
c & d \\
\end{pmatrix}
$$

Next, we compute the product $BA$:

$$
BA = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
a \cdot 1 + b \cdot 0 & a \cdot 1 + b \cdot 1 \\
c \cdot 1 + d \cdot 0 & c \cdot 1 + d \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
a & a + b \\
c & c + d \\
\end{pmatrix}
$$

### 2. Equating $AB = BA$ to Find the Conditions

For $AB = BA$ to hold, every corresponding entry of the two matrices must be equal:

$$
\begin{pmatrix}
a + c & b + d \\
c & d \\
\end{pmatrix} = \begin{pmatrix}
a & a + b \\
c & c + d \\
\end{pmatrix}
$$

Comparing entry by entry gives four equations:
- $(1,1)$ entry: $a + c = a \implies c = 0$
- $(1,2)$ entry: $b + d = a + b \implies d = a$
- $(2,1)$ entry: $c = c$ (always satisfied)
- $(2,2)$ entry: $d = c + d \implies c = 0$

Thus, the necessary and sufficient conditions on the entries of $B$ are $c = 0$ and $a = d$, while $b$ can be any scalar.

### 3. General Form of All Such Matrices $B$

Substituting $c = 0$ and $d = a$ back into $B$, every matrix $B$ that commutes with $A$ has the general upper triangular form:

$$
B = \begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

where $a, b \in \mathbb{R}$ are arbitrary real numbers. Equivalently, $B$ can be written as a linear combination:

$$
B = a \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} + b \begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}
$$
