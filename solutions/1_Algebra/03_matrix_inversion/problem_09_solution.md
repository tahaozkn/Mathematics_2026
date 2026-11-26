### Exercise 9. Matrix Equation

## Question

Given

$$
A = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad
B = \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX = B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Solution

1. **Decide Which Side to Multiply by $A^{-1}$:**
   In the matrix equation $AX = B$, the unknown matrix $X$ is multiplied by $A$ on the **left**. Because matrix multiplication is non-commutative in general, we must multiply both sides of the equation by $A^{-1}$ on the **left** so that $A^{-1}$ sits directly adjacent to $A$:

$$
\begin{aligned}
A^{-1}(AX) &= A^{-1}B \\
(A^{-1}A)X &= A^{-1}B \\
IX &= A^{-1}B \\
X &= A^{-1}B
\end{aligned}
$$

   Multiplying on the right would yield $AXA^{-1} = BA^{-1}$, which does not isolate $X$.

2. **Compute the Inverse Matrix $A^{-1}$:**
   First find the determinant of $A$:

$$
\det A = (1)(1) - (2)(0) = 1 - 0 = 1
$$

   Since $\det A = 1 \neq 0$, $A$ is invertible. Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
$$

3. **Compute $X = A^{-1}B$:**
   Multiply $B$ on the left by $A^{-1}$:

$$
\begin{aligned}
X &= \begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(3) + (-2)(2) & 1(1) + (-2)(4) \\
0(3) + 1(2) & 0(1) + 1(4) \\
\end{pmatrix} \\
&= \begin{pmatrix}
3 - 4 & 1 - 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} \\
&= \begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
\end{aligned}
$$

## Verification

Check the result by substituting $X$ back into the left-hand side of the original equation and computing $AX$:

$$
\begin{aligned}
AX &= \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(-1) + 2(2) & 1(-7) + 2(4) \\
0(-1) + 1(2) & 0(-7) + 1(4) \\
\end{pmatrix} \\
&= \begin{pmatrix}
-1 + 4 & -7 + 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} \\
&= \begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
&= B
\end{aligned}
$$

Since $AX = B$, the matrix $X$ is confirmed.
