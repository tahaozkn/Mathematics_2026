### Exercise 6. Solving a System Using the Inverse

## Question

Solve

$$
A\mathbf{x} = \mathbf{b},
$$

where

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}, \quad
\mathbf{b} = \begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $\mathbf{x} = A^{-1}\mathbf{b}$. Then substitute the resulting vector back into the equation and check the result.

## Solution

1. **Compute the Determinant of $A$:**
   Using the $2 \times 2$ determinant formula $\det A = ad - bc$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5
$$

   Since $\det A = 5 \neq 0$, the matrix $A$ is invertible.

2. **Find the Inverse Matrix $A^{-1}$:**
   Apply the $2 \times 2$ inverse formula by swapping the main diagonal entries ($2$ and $3$), negating the off-diagonal entries ($1$ and $1$), and dividing by $\det A = 5$:

$$
A^{-1} = \frac{1}{5} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{3}{5} & -\frac{1}{5} \\
-\frac{1}{5} & \frac{2}{5} \\
\end{pmatrix}
$$

3. **Compute the Solution Vector $\mathbf{x} = A^{-1}\mathbf{b}$:**
   Multiply $A^{-1}$ by the right-hand side vector $\mathbf{b}$:

$$
\begin{aligned}
\mathbf{x} &= \frac{1}{5} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
3(5) + (-1)(7) \\
(-1)(5) + 2(7) \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
15 - 7 \\
-5 + 14 \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
8 \\
9 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
\end{aligned}
$$

   Thus, the unique solution vector is:

$$
\mathbf{x} = \begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

## Verification

Substitute $\mathbf{x} = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}$ back into the original equation $A\mathbf{x} = \mathbf{b}$:

$$
\begin{aligned}
A\mathbf{x} &= \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\
1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{16}{5} + \frac{9}{5} \\
\frac{8}{5} + \frac{27}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
&= \mathbf{b}
\end{aligned}
$$

Since $A\mathbf{x} = \mathbf{b}$, the solution vector $\mathbf{x}$ is confirmed.
