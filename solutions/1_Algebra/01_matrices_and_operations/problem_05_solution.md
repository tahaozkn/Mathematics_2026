### Exercise 5. Matrix Times Vector

## Question

Let

$$
A =
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
$$

and

$$
x =
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

Computing the matrix-vector product $Ax$ by taking the dot product of each row of $A$ with $x$ gives:

$$
\begin{aligned}
Ax &=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot 4 + (-1)\cdot 2 \\
1\cdot 4 + 3\cdot 2 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
\end{aligned}
$$

Let $a_1$ and $a_2$ denote the first and second columns of $A$:

$$
a_1 =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},
\qquad
a_2 =
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

Using the entries of $x$ ($x_1 = 4$ and $x_2 = 2$) as scalar weights, $Ax$ as a linear combination of the columns of $A$ is:

$$
Ax = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

## Verification

Evaluating the linear combination directly by performing scalar multiplication and vector addition confirms that it produces the same vector as the row-by-column product:

$$
4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

Both perspectives yield the identical result $Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix}$.
