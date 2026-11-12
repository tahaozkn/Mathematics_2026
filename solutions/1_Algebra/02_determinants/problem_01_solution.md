### Exercise 1. Determinant of a $2 \times 2$ Matrix

## Question

Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},
\qquad
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

## Solution

For a general $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is defined as $\det(M) = ad - bc$.

Let $A$ and $B$ denote the two given matrices:

$$
A =
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},
\qquad
B =
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}
$$

Computing the determinant of $A$:

$$
\det(A) = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22
$$

Computing the determinant of $B$:

$$
\det(B) = (1)(14) - (7)(2) = 14 - 14 = 0
$$

**Invertibility:**
A square matrix is invertible if and only if its determinant is nonzero ($\det(M) \neq 0$).
- Since $\det(A) = 22 \neq 0$, matrix **$A$ is invertible**.
- Since $\det(B) = 0$, matrix **$B$ is not invertible** (singular).

## Verification

We can verify invertibility independently using row reduction and the $2 \times 2$ inverse formula.

For matrix $A$, applying the formula $A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$ yields:

$$
A^{-1} = \frac{1}{22}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}
$$

Multiplying $A$ by $A^{-1}$ confirms it produces the identity matrix:

$$
A A^{-1} = \frac{1}{22}
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}
= \frac{1}{22}
\begin{pmatrix}
12 + 10 & 6 - 6 \\
20 - 20 & 10 + 12 \\
\end{pmatrix}
= \frac{1}{22}
\begin{pmatrix}
22 & 0 \\
0 & 22 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

For matrix $B$, performing the row operation $R_2 \leftarrow R_2 - 2R_1$ gives:

$$
\begin{pmatrix}
1 & 7 \\
2 - 2(1) & 14 - 2(7) \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 7 \\
0 & 0 \\
\end{pmatrix}
$$

Because row reduction produces a row of zeros, $B$ has only one pivot instead of two, confirming that it is singular and cannot be inverted.
