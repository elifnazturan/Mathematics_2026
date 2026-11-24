# Exercise 9. Area and Determinant

**Given:**

$$u = \begin{pmatrix} 3 \\\\ 1 \end{pmatrix}, \qquad v = \begin{pmatrix} 1 \\\\ 4 \end{pmatrix}$$

---

### 1. Sketch the Parallelogram and Compute Its Area Using a Determinant.

* **Method and Property Used:** In $\mathbb{R}^2$, the area of the parallelogram spanned by two vectors $u = \begin{pmatrix} u_1 \\\\ u_2 \end{pmatrix}$ and $v = \begin{pmatrix} v_1 \\\\ v_2 \end{pmatrix}$ equals the **absolute value of the determinant** of the $2 \times 2$ matrix formed by placing $u$ and $v$ as columns (or rows):

$$\text{Area} = \left|\det \begin{pmatrix} u & v \end{pmatrix}\right| = |u_1 v_2 - u_2 v_1|$$

* **Geometric Sketch (Vertices in $\mathbb{R}^2$):**
  * The parallelogram has four vertices starting at the origin:
    * $O = (0, 0)$
    * $A = u = (3, 1)$
    * $B = v = (1, 4)$
    * $C = u + v = (3 + 1, 1 + 4) = (4, 5)$
  * Two adjacent sides go from $(0, 0)$ to $(3, 1)$ and from $(0, 0)$ to $(1, 4)$, and the opposite parallel sides meet at $(4, 5)$.

* **Main steps:**
  * Form the matrix $M = \begin{pmatrix} u & v \end{pmatrix} = \begin{pmatrix} 3 & 1 \\\\ 1 & 4 \end{pmatrix}$ and compute its determinant:

$$\det\begin{pmatrix} 3 & 1 \\\\ 1 & 4 \end{pmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11$$

  * Take the absolute value to get the area:

$$\text{Area} = |11| = 11$$

* **Result:**

$$\text{Area} = 11$$

* **Verification:** Enclose the parallelogram inside the axis-aligned rectangle $[0, 4] \times [0, 5]$ of area $4 \times 5 = 20$, and subtract the surrounding right triangles and rectangles outside the parallelogram:
  * Two triangles of base $3$, height $1$: $2 \times \frac{1}{2}(3)(1) = 3$
  * Two triangles of base $1$, height $4$: $2 \times \frac{1}{2}(1)(4) = 4$
  * Two corner rectangles of size $1 \times 1$: $2 \times (1)(1) = 2$
  * $\text{Area} = 20 - (3 + 4 + 2) = 20 - 9 = 11$, confirming the determinant result.

---

### 2. Reverse the Order of the Vectors and Explain What Changes in the Determinant and What Does Not Change in the Area.

* **Method and Property Used:** Swapping the two columns of a $2 \times 2$ matrix **multiplies the determinant by $-1$** ($\det\begin{pmatrix} v & u \end{pmatrix} = -\det\begin{pmatrix} u & v \end{pmatrix}$), whereas the absolute value $|\det|$ remains invariant ($|-x| = |x|$).

* **Main steps:**
  * Reverse the order of $u$ and $v$ to form $M_{\text{rev}} = \begin{pmatrix} v & u \end{pmatrix} = \begin{pmatrix} 1 & 3 \\\\ 4 & 1 \end{pmatrix}$:

$$\det\begin{pmatrix} 1 & 3 \\\\ 4 & 1 \end{pmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11$$

  * Compute the area from the reversed-order determinant:

$$\text{Area} = |-11| = 11$$

* **Result:**
  * **Determinant:** Changes sign from $+11$ to $-11$.
  * **Area:** Remains unchanged at $11$.

* **Explanation and Verification:**
  * **What changes in the determinant:** The determinant tracks **orientation** (signed area). Moving from $u = (3, 1)$ to $v = (1, 4)$ turns counterclockwise ($\det = +11 > 0$), whereas moving from $v = (1, 4)$ to $u = (3, 1)$ turns clockwise ($\det = -11 < 0$). Swapping the two columns reverses orientation and flips the sign of the determinant.
  * **What does not change in the area:** Geometric area is always non-negative and depends only on the magnitude $|\det|$. Since $|-11| = |11| = 11$ and both pairs $(u, v)$ and $(v, u)$ span the exact same parallelogram with vertices $(0,0), (3,1), (1,4), (4,5)$, the area stays $11$.
