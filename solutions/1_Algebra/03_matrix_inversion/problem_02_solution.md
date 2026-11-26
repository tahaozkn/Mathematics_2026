### Exercise 2. Formula for a $2 \times 2$ Matrix

## Question

Find the inverse of

$$
A = \begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2 \times 2$ matrix. At the end, check the result by computing one product with $A$.

## Solution

1. **Recall the $2 \times 2$ Inverse Formula:**
   For a general $2 \times 2$ matrix

$$
M = \begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

   the inverse $M^{-1}$ exists if and only if $\det M = ad - bc \neq 0$, and is given by:

$$
M^{-1} = \frac{1}{ad - bc} \begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

2. **Compute the Determinant of $A$:**
   Identify the entries $a = 3$, $b = 2$, $c = 5$, and $d = 4$, and calculate $\det A$:

$$
\det A = (3)(4) - (2)(5) = 12 - 10 = 2
$$

   Since $\det A = 2 \neq 0$, the matrix $A$ is invertible.

3. **Apply the Inverse Formula:**
   Swap the main diagonal entries ($3$ and $4$), negate the off-diagonal entries ($2$ and $5$), and multiply by $\frac{1}{\det A} = \frac{1}{2}$:

$$
\begin{aligned}
A^{-1} &= \frac{1}{2} \begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{4}{2} & \frac{-2}{2} \\
\frac{-5}{2} & \frac{3}{2} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
\end{aligned}
$$

## Verification

Check the result by computing the product $AA^{-1}$:

$$
\begin{aligned}
AA^{-1} &= \begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix} \\
&= \begin{pmatrix}
3(2) + 2\left(-\frac{5}{2}\right) & 3(-1) + 2\left(\frac{3}{2}\right) \\
5(2) + 4\left(-\frac{5}{2}\right) & 5(-1) + 4\left(\frac{3}{2}\right) \\
\end{pmatrix} \\
&= \begin{pmatrix}
6 - 5 & -3 + 3 \\
10 - 10 & -5 + 6 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

Since $AA^{-1} = I$, the computed inverse matrix $A^{-1}$ is verified.
