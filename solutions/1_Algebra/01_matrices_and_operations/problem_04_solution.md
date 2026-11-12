### Exercise 4. Matrix Multiplication and Noncommutativity

## Question

For

$$
A = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB = BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

1. **Compute the product $AB$:**

$$
AB = \begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(2) + (2)(3) & (1)(0) + (2)(1) \\
(0)(2) + (1)(3) & (0)(0) + (1)(1) \\
\end{pmatrix}
= \begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

2. **Compute the product $BA$:**

$$
BA = \begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
(2)(1) + (0)(0) & (2)(2) + (0)(1) \\
(3)(1) + (1)(0) & (3)(2) + (1)(1) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

3. **Comparison ($AB$ vs $BA$):**
Comparing the two resulting products:

$$
AB = \begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix} \quad \text{and} \quad BA = \begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

Clearly, $AB \neq BA$.

## Explanation of Noncommutativity

In ordinary algebra with real numbers, multiplication is commutative, meaning that $ab = ba$ for any numbers $a$ and $b$ (for instance, $2 \times 3 = 3 \times 2 = 6$). 

However, matrix multiplication is **noncommutative**. As demonstrated by this example, changing the order of multiplication generally changes the result. In many cases, reversing the order can even result in matrices of incompatible dimensions where the product cannot be calculated at all. This highlights one of the fundamental differences between the algebra of matrices and the algebra of real numbers.
