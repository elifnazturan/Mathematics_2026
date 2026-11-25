# Exercise 13. Undoing a Composite Transformation

## Question

We are given two $2 \times 2$ matrices describing nonuniform scaling and shear:

$$
S = \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad H = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

For the composite transformation $T = HS$, we need to:
1. Find $T^{-1}$ in two ways:
   - First compute $T$, then find its inverse $T^{-1}$.
   - Use the product-inverse rule $(HS)^{-1} = S^{-1}H^{-1}$.
2. Compare the two results.
3. Compute $H^{-1}S^{-1}$ and verify that this incorrect order gives a different matrix.
4. Explain the rule: "when undoing a composition of operations, we undo them from the end."

## Solution

### 1. Finding $T^{-1}$ in Two Ways

#### Way 1: Compute $T = HS$ First, Then Invert

First, we multiply $H$ and $S$ to obtain $T = HS$:

$$
T = HS = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
(1)(2) + (1)(0) & (1)(0) + (1)(1) \\
(0)(2) + (1)(0) & (0)(0) + (1)(1) \\
\end{pmatrix} = \begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Next, we find $T^{-1}$ using the $2 \times 2$ inverse formula. The determinant of $T$ is:

$$
\det(T) = (2)(1) - (1)(0) = 2 \neq 0
$$

Applying the $2 \times 2$ inverse formula gives:

$$
T^{-1} = \frac{1}{2} \begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
$$

#### Way 2: Use $(HS)^{-1} = S^{-1}H^{-1}$

First, we find $S^{-1}$ for the diagonal scaling matrix $S$ by taking the reciprocals of its diagonal entries:

$$
S^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Next, we find $H^{-1}$ for the shear matrix $H$. Since $\det(H) = (1)(1) - (1)(0) = 1$, the $2 \times 2$ formula gives:

$$
H^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

Now we compute $S^{-1}H^{-1}$:

$$
S^{-1}H^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
\left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\
(0)(1) + (1)(0) & (0)(-1) + (1)(1) \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
$$

### 2. Comparing the Results

Both methods yield the exact same inverse matrix:

$$
T^{-1} = S^{-1}H^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix}
$$

### 3. Computing $H^{-1}S^{-1}$ and Verifying It Differs

Reversing the order of $S^{-1}$ and $H^{-1}$ gives:

$$
H^{-1}S^{-1} = \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
(1)\left(\frac{1}{2}\right) + (-1)(0) & (1)(0) + (-1)(1) \\
(0)\left(\frac{1}{2}\right) + (1)(0) & (0)(0) + (1)(1) \\
\end{pmatrix} = \begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix}
$$

Comparing entries, we see that the $(1, 2)$ entry is $-1$ in $H^{-1}S^{-1}$ versus $-\frac{1}{2}$ in $T^{-1}$, so:

$$
H^{-1}S^{-1} \neq T^{-1}
$$

To verify that $H^{-1}S^{-1}$ does not undo $T = HS$:

$$
(H^{-1}S^{-1})(HS) = \begin{pmatrix}
\frac{1}{2} & -1 \\
0 & 1 \\
\end{pmatrix} \begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix} = \begin{pmatrix}
1 & -\frac{1}{2} \\
0 & 1 \\
\end{pmatrix} \neq I_2
$$

### 4. Explaining Why We Undo Operations From the End

In $T = HS$, a vector $x$ is first scaled by $S$ (producing $Sx$) and then sheared by $H$ (producing the sheared vector). Just like putting on socks first and shoes second requires taking off shoes first and socks second, we must undo the last applied operation ($H$) before undoing the first applied operation ($S$). Applying $S^{-1}$ first would act on a sheared vector rather than undoing the scaling directly, which is why $(HS)^{-1} = S^{-1}H^{-1}$.
