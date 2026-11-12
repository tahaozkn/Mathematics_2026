### Exercise 4. Matrix Multiplication and Noncommutativity

## Question

For

$$A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix}$$

and

$$B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \\ \end{pmatrix}$$

compute $AB$ and $BA$. Is $AB = BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

Each entry $(XY)_{ij}$ of a matrix product is obtained by taking the dot product of row $i$ of $X$ with column $j$ of $Y$.

For $AB$:

$$\begin{aligned} AB &= \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 3 & 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1\cdot 2 + 2\cdot 3 & 1\cdot 0 + 2\cdot 1 \\ 0\cdot 2 + 1\cdot 3 & 0\cdot 0 + 1\cdot 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 8 & 2 \\ 3 & 1 \\ \end{pmatrix} \end{aligned}$$

For $BA$:

$$\begin{aligned} BA &= \begin{pmatrix} 2 & 0 \\ 3 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 2\cdot 1 + 0\cdot 0 & 2\cdot 2 + 0\cdot 1 \\ 3\cdot 1 + 1\cdot 0 & 3\cdot 2 + 1\cdot 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 2 & 4 \\ 3 & 7 \\ \end{pmatrix} \end{aligned}$$

Comparing the two results shows that

$$AB \neq BA.$$

**Meaning of noncommutativity:** Unlike real numbers, where $ab = ba$ holds for all $a$ and $b$, matrix multiplication depends on the order of the factors. Even when both products $AB$ and $BA$ are defined and have the same size, changing the order combines different rows and columns, generally producing two different matrices.

## Verification

We can verify that $AB \neq BA$ using two invariant properties of matrix products: the trace and the determinant.

First, for any two square matrices of the same size, $\mathrm{tr}(AB) = \mathrm{tr}(BA)$ must hold. Computing the traces from our results gives:

$$\mathrm{tr}(AB) = 8 + 1 = 9, \qquad \mathrm{tr}(BA) = 2 + 7 = 9.$$

Both traces equal $9$, confirming consistency in the diagonal entries while still allowing off-diagonal entries to differ.

Second, we verify both products by applying them to the test vector

$$v = \begin{pmatrix} 1 \\ 1 \\ \end{pmatrix}$$

Using associativity, $(AB)v$ must equal $A(Bv)$:

$$(AB)v = \begin{pmatrix} 8 & 2 \\ 3 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 \\ 1 \\ \end{pmatrix} = \begin{pmatrix} 10 \\ 4 \\ \end{pmatrix}, \qquad A(Bv) = \begin{pmatrix} 1 & 2 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 2 \\ 4 \\ \end{pmatrix} = \begin{pmatrix} 10 \\ 4 \\ \end{pmatrix}.$$

Similarly, $(BA)v$must equal$B(Av)$:  $$
(BA)v =
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix},
\qquad
B(Av) =
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix}
=
\begin
