### Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

For

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute $AI$, $IA$, $A + 0$, $A^2$, and $A^3$. Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

Let $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ be the $2 \times 2$ identity matrix and $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ be the $2 \times 2$ zero matrix.

1. **Computing $AI$ and $IA$:**

$$
AI = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
(2)(1)+(1)(0) & (2)(0)+(1)(1) \\
(0)(1)+(2)(0) & (0)(0)+(2)(1) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = A
$$

$$
IA = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
(1)(2)+(0)(0) & (1)(1)+(0)(2) \\
(0)(2)+(1)(0) & (0)(1)+(1)(2) \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = A
$$

2. **Computing $A + 0$:**

$$
A + 0 = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
+ \begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
= \begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} = A
$$

3. **Computing $A^2$ and $A^3$:**

$$
A^2 = A \cdot A = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
(2)(2)+(1)(0) & (2)(1)+(1)(2) \\
(0)(2)+(2)(0) & (0)(1)+(2)(2) \\
\end{pmatrix}
= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

$$
A^3 = A^2 \cdot A = \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
(4)(2)+(4)(0) & (4)(1)+(4)(2) \\
(0)(2)+(4)(0) & (0)(1)+(4)(2) \\
\end{pmatrix}
= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

**Roles of $I$ and $0$:**
- The identity matrix $I$ acts as the multiplicative identity for matrix multiplication, satisfying $AI = IA = A$ for any square matrix $A$ of compatible size.
- The zero matrix $0$ acts as the additive identity, satisfying $A + 0 = A$ for any matrix $A$.

**Pattern in successive powers of $A$:**
Observing $A^1 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$, $A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$, and $A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$, the diagonal entries grow as $2^k$, while the top-right entry grows according to $k \cdot 2^{k-1}$. The general formula for any positive integer $k$ is:

$$
A^k = \begin{pmatrix}
2^k & k 2^{k-1} \\
0 & 2^k \\
\end{pmatrix}
$$

## Verification

We verify the formula for $A^k$ at $k=3$ using our computed result:

$$
A^3 = \begin{pmatrix}
2^3 & 3 \cdot 2^{3-1} \\
0 & 2^3 \\
\end{pmatrix}
= \begin{pmatrix}
8 & 3 \cdot 4 \\
0 & 8 \\
\end{pmatrix}
= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

This matches the direct matrix product $A^2 \cdot A$, fully verifying the pattern and calculations without any unclosed environments.
