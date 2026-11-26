### Exercise 14. A Matrix That Is Its Own Inverse

## Question

Assume that a square matrix $A$ satisfies

$$
A^2 = I.
$$

Show that

$$
A^{-1} = A.
$$

Then give an example of a $2 \times 2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Solution

1. **Proof that $A^{-1} = A$:**
   By definition, a square matrix $B$ is the inverse of a square matrix $A$ (written $B = A^{-1}$) if and only if $AB = I$ and $BA = I$.

   We are given that $A^2 = I$. Expanding $A^2$ as the product of $A$ with itself gives:

$$
A \cdot A = I
$$

   In this equation, $A$ acts as both the left-hand factor and the right-hand factor that multiplies with $A$ to produce the identity matrix $I$. By the uniqueness of the matrix inverse, $A$ satisfies the exact definition of its own inverse:

$$
A^{-1} = A
$$

   *(Note: Matrices satisfying $A^2 = I$ are called **involutory matrices**.)*

2. **Constructing a $2 \times 2$ Example ($A \neq I, -I$):**
   Geometrically, a reflection across a line through the origin in $\mathbb{R}^2$ is an operation that undoes itself when applied twice. Choosing a reflection across the $x$-axis keeps the $x$-coordinate unchanged and negates the $y$-coordinate, which gives the matrix:

$$
A = \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}
$$

   Clearly, $A \neq I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ \end{pmatrix}$ and $A \neq -I = \begin{pmatrix} -1 & 0 \\ 0 & -1 \\ \end{pmatrix}$.

   *(Other valid $2 \times 2$ examples include reflection across the $y$-axis $\begin{pmatrix} -1 & 0 \\ 0 & 1 \\ \end{pmatrix}$ or reflection across the line $y = x$, which is the permutation matrix $\begin{pmatrix} 0 & 1 \\ 1 & 0 \\ \end{pmatrix}$.)*

## Verification

We verify that our chosen matrix $A = \begin{pmatrix} 1 & 0 \\ 0 & -1 \\ \end{pmatrix}$ satisfies $A^2 = I$ by computing $A \cdot A$ directly:

$$
\begin{aligned}
A^2 &= \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(1) + 0(0) & 1(0) + 0(-1) \\
0(1) + (-1)(0) & 0(0) + (-1)(-1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 + 0 & 0 + 0 \\
0 + 0 & 0 + 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

We can also cross-check using the explicit $2 \times 2$ inverse formula. With $\det A = (1)(-1) - (0)(0) = -1$:

$$
A^{-1} = \frac{1}{-1} \begin{pmatrix}
-1 & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}
= A
$$

Both direct multiplication and the inverse formula confirm that $A^{-1} = A$.
