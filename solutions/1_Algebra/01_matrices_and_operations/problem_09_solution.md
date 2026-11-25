# Exercise 9. Composing Transformations

## Question

We are given two $2 \times 2$ transformation matrices and a $2 \times 1$ vector:

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad R = \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
$$

$$
x = \begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

Here, $S$ represents nonuniform scaling (scaling the first coordinate by $2$ and keeping the second coordinate unchanged), and $R$ represents a $90^\circ$ counterclockwise rotation in the plane[cite: 8]. We need to:
1. Compute $RSx$ and $SRx$.
2. Compare the two resulting vectors.
3. Explain geometrically why the order of applying these transformations matters[cite: 8].

## Solution

### 1. Computing $RSx$

In $RSx$, transformation $S$ is applied to $x$ first, and then $R$ is applied to the result $Sx$. First, we compute $Sx$:

$$
Sx = \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 \\
2 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot 1 + 0 \cdot 2 \\
0 \cdot 1 + 1 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
$$

Next, we apply $R$ to $Sx$:

$$
RSx = \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix} \begin{pmatrix}
2 \\
2 \\
\end{pmatrix} = \begin{pmatrix}
0 \cdot 2 + (-1) \cdot 2 \\
1 \cdot 2 + 0 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

### 2. Computing $SRx$

In $SRx$, transformation $R$ is applied to $x$ first, and then $S$ is applied to the result $Rx$. First, we compute $Rx$:

$$
Rx = \begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix} \begin{pmatrix}
1 \\
2 \\
\end{pmatrix} = \begin{pmatrix}
0 \cdot 1 + (-1) \cdot 2 \\
1 \cdot 1 + 0 \cdot 2 \\
\end{pmatrix} = \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
$$

Next, we apply $S$ to $Rx$:

$$
SRx = \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
-2 \\
1 \\
\end{pmatrix} = \begin{pmatrix}
2 \cdot (-2) + 0 \cdot 1 \\
0 \cdot (-2) + 1 \cdot 1 \\
\end{pmatrix} = \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

### 3. Comparison and Geometric Explanation

Comparing the two results gives:

$$
RSx = \begin{pmatrix}
-2 \\
2 \\
\end{pmatrix} \neq \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix} = SRx
$$

The two vectors differ because matrix multiplication and transformation composition are not commutative ($RS \neq SR$)[cite: 8]. Geometrically:
- In $RSx$, scaling along the horizontal axis happens before rotation. The vector $x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ first stretches horizontally to $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$, and then rotating $\begin{pmatrix} 2 \\ 2 \end{pmatrix}$ counterclockwise by $90^\circ$ maps $(u, v)$ to $(-v, u)$, giving $\begin{pmatrix} -2 \\ 2 \end{pmatrix}$.
- In $SRx$, rotation happens before horizontal scaling. Rotating $\begin{pmatrix} 1 \\ 2 \end{pmatrix}$ counterclockwise by $90^\circ$ first produces $\begin{pmatrix} -2 \\ 1 \end{pmatrix}$, and then doubling only the first coordinate scales $-2$ to $-4$ while keeping the second coordinate at $1$, giving $\begin{pmatrix} -4 \\ 1 \end{pmatrix}$.

Because $S$ acts only on the first coordinate while $R$ mixes the first and second coordinates through a $90^\circ$ turn, performing them in opposite orders changes which coordinate is stretched.
