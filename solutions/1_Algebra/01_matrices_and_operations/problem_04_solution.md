### Exercise 4. Associativity of Matrix Multiplication

## Question

Let

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}, \quad B = \begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix}, \quad C = \begin{pmatrix}
1 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

Compute $(AB)C$ and $A(BC)$ to verify the associativity of matrix multiplication.

## Solution

First, compute the product $AB$:

$$
AB = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(0)+(2)(2) & (1)(1)+(2)(1) \\
(3)(0)+(4)(2) & (3)(1)+(4)(1) \\
\end{pmatrix}
= \begin{pmatrix}
4 & 3 \\
8 & 7 \\
\end{pmatrix}
$$

Next, multiply $AB$ by $C$ to find $(AB)C$:

$$
(AB)C = \begin{pmatrix}
4 & 3 \\
8 & 7 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
(4)(1)+(3)(0) & (4)(1)+(3)(2) \\
(8)(1)+(7)(0) & (8)(1)+(7)(2) \\
\end{pmatrix}
= \begin{pmatrix}
4 & 10 \\
8 & 22 \\
\end{pmatrix}
$$

Now, compute the product $BC$:

$$
BC = \begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
(0)(1)+(1)(0) & (0)(1)+(1)(2) \\
(2)(1)+(1)(0) & (2)(1)+(1)(2) \\
\end{pmatrix}
= \begin{pmatrix}
0 & 2 \\
2 & 4 \\
\end{pmatrix}
$$

Finally, multiply $A$ by $BC$ to find $A(BC)$:

$$
A(BC) = \begin{pmatrix}
1 & 2 \\
3 & 4 \\
\end{pmatrix}
\begin{pmatrix}
0 & 2 \\
2 & 4 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(0)+(2)(2) & (1)(2)+(2)(4) \\
(3)(0)+(4)(2) & (3)(2)+(4)(4) \\
\end{pmatrix}
= \begin{pmatrix}
4 & 10 \\
8 & 22 \\
\end{pmatrix}
$$

## Verification

Both calculation paths yield the exact same resulting matrix:

$$
(AB)C = A(BC) = \begin{pmatrix}
4 & 10 \\
8 & 22 \\
\end{pmatrix}
$$

This completes the verification of both products, confirming the associative property and ensuring all math environments are properly closed.
