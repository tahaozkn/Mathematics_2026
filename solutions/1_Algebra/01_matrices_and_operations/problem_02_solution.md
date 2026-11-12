### Exercise 2. Addition and Scalar Multiplication

## Question

For

$$
A =
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
$$

and

$$
B =
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B, \quad A-B, \quad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

Matrix addition, subtraction, and scalar multiplication are performed entry by entry.

For $A+B$:

$$
\begin{aligned}
A+B &=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
+
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
\end{aligned}
$$

For $A-B$:

$$
\begin{aligned}
A-B &=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
-
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
\end{aligned}
$$

For $3A-2B$, first compute the scalar multiples $3A$ and $2B$:

$$
3A =
\begin{pmatrix}
3\cdot 1 & 3\cdot 2 \\
3\cdot (-1) & 3\cdot 3 \\
\end{pmatrix}
=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}
$$

and

$$
2B =
\begin{pmatrix}
2\cdot 4 & 2\cdot (-2) \\
2\cdot 0 & 2\cdot 5 \\
\end{pmatrix}
=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

Subtracting $2B$ from $3A$ yields:

$$
\begin{aligned}
3A-2B &=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}
-
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
\end{aligned}
$$

**Compatibility condition:** Matrix addition is defined componentwise via $(A+B)_{ij} = a_{ij} + b_{ij}$. For every entry $a_{ij}$ in row $i$ and column $j$ of $A$, there must exist a corresponding entry $b_{ij}$ at the exact same row and column position in $B$. If the matrices have different dimensions, at least one entry in the larger matrix lacks a counterpart in the smaller matrix, leaving the sum undefined.

## Verification

We can check the results using algebraic identities of matrix arithmetic. First, adding the results for $A+B$ and $A-B$ must yield $2A$:

$$
(A+B) + (A-B) =
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
+
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 4 \\
-2 & 6 \\
\end{pmatrix}
= 2A.
$$

Second, decomposing $3A-2B$ as $2(A-B) + A$ provides an independent calculation:

$$
\begin{aligned}
2(A-B) + A &= 2
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
+
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-6 & 8 \\
-2 & -4 \\
\end{pmatrix}
+
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
\end{aligned}
$$

This matches the computed matrix $3A-2B$ entry for entry.
