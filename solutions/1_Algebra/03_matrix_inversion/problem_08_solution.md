### Exercise 8. Inverse of a Transformation

## Question

The matrix

$$
S = \begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S, S^{-1}$ on one simple vector.

## Solution

1. **Compute the Determinant of $S$:**
   Using the $2 \times 2$ determinant formula $\det S = ad - bc$:

$$
\det S = (2)\left(\frac{1}{2}\right) - (0)(0) = 1 - 0 = 1
$$

   Since $\det S = 1 \neq 0$, the scaling matrix $S$ is invertible.

2. **Find the Inverse Matrix $S^{-1}$:**
   Apply the $2 \times 2$ inverse formula (or take the reciprocals of the non-zero diagonal entries of a diagonal matrix):

$$
\begin{aligned}
S^{-1} &= \frac{1}{1} \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

3. **Geometric Explanation of the Inverse Transformation:**
   - **Action of $S$:** Multiplying a vector $\begin{pmatrix} x \\ y \end{pmatrix}$ by $S$ produces $\begin{pmatrix} 2x \\ \frac{1}{2}y \end{pmatrix}$, which stretches the plane horizontally along the $x$-axis by a factor of $2$ and compresses it vertically along the $y$-axis by a factor of $\frac{1}{2}$.
   - **Action of $S^{-1}$:** Multiplying a vector $\begin{pmatrix} x \\ y \end{pmatrix}$ by $S^{-1}$ produces $\begin{pmatrix} \frac{1}{2}x \\ 2y \end{pmatrix}$, which **compresses the plane horizontally along the $x$-axis by a factor of $\frac{1}{2}$** (halving the $x$-coordinate) and **stretches it vertically along the $y$-axis by a factor of $2$** (doubling the $y$-coordinate).
   - **Summary:** Geometrically, $S^{-1}$ performs the exact opposite scaling along each coordinate axis to undo the distortion caused by $S$ and restore every point in the plane to its original position.

4. **Check the Action on a Simple Vector:**
   Choose the simple test vector:

$$
\mathbf{v} = \begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
$$

   - **Apply $S$ to $\mathbf{v}$:**

$$
\mathbf{w} = S\mathbf{v} = \begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
\begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
= \begin{pmatrix}
2(3) + 0(4) \\
0(3) + \frac{1}{2}(4) \\
\end{pmatrix}
= \begin{pmatrix}
6 \\
2 \\
\end{pmatrix}
$$

   - **Apply $S^{-1}$ to the transformed vector $\mathbf{w}$:**

$$
S^{-1}\mathbf{w} = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
6 \\
2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(6) + 0(2) \\
0(6) + 2(2) \\
\end{pmatrix}
= \begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
= \mathbf{v}
$$

   Applying $S^{-1}$ after $S$ returns $\mathbf{w}$ back to the original vector $\mathbf{v}$.

## Verification

We can verify algebraically that $S^{-1}$ is the true two-sided inverse of $S$ by computing both products $SS^{-1}$ and $S^{-1}S$:

- **Right inverse check ($SS^{-1}$):**

$$
SS^{-1} = \begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
2\left(\frac{1}{2}\right) + 0(0) & 2(0) + 0(2) \\
0\left(\frac{1}{2}\right) + \frac{1}{2}(0) & 0(0) + \frac{1}{2}(2) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I
$$

- **Left inverse check ($S^{-1}S$):**

$$
S^{-1}S = \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2}(2) + 0(0) & \frac{1}{2}(0) + 0\left(\frac{1}{2}\right) \\
0(2) + 2(0) & 0(0) + 2\left(\frac{1}{2}\right) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= I
$$

Both products equal the identity matrix $I$, confirming that $S^{-1}$ accurately inverts $S$.
