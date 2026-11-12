### Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

For

$$A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix}$$

compute

$$AI, \quad IA, \quad A+0, \quad A^2, \quad A^3.$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

Let $I$ be the $2 \times 2$ identity matrix and $0$ be the $2 \times 2$ zero matrix:

$$I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ \end{pmatrix}, \qquad 0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ \end{pmatrix}$$

Computing the products involving $I$ and the sum involving $0$:

$$AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ \end{pmatrix} = \begin{pmatrix} 2\cdot 1 + 1\cdot 0 & 2\cdot 0 + 1\cdot 1 \\ 0\cdot 1 + 2\cdot 0 & 0\cdot 0 + 2\cdot 1 \\ \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = A$$

$$IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = \begin{pmatrix} 1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot 2 \\ 0\cdot 2 + 1\cdot 0 & 0\cdot 1 + 1\cdot 2 \\ \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = A$$

$$A+0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \\ \end{pmatrix} = \begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \\ \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = A$$

Computing the powers $A^2$ and $A^3$:

$$A^2 = A \cdot A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = \begin{pmatrix} 2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot 2 \\ 0\cdot 2 + 2\cdot 0 & 0\cdot 1 + 2\cdot 2 \\ \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \\ \end{pmatrix}$$

$$A^3 = A^2 \cdot A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \\ \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = \begin{pmatrix} 4\cdot 2 + 4\cdot 0 & 4\cdot 1 + 4\cdot 2 \\ 0\cdot 2 + 4\cdot 0 & 0\cdot 1 + 4\cdot 2 \\ \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \\ \end{pmatrix}$$

**Roles of $I$ and $0$:** 
- The identity matrix $I$ acts as the multiplicative neutral element ($AI = IA = A$), playing the role of the number $1$ in matrix algebra.
- The zero matrix $0$ acts as the additive neutral element ($A+0 = A$), playing the role of the number $0$ in matrix addition.

**Pattern in successive powers:** 
For any positive integer $n$, the matrix power $A^n$ follows the general formula:

$$A^n = \begin{pmatrix} 2^n & n 2^{n-1} \\ 0 & 2^n \\ \end{pmatrix}$$

## Verification

We can verify the formula for $A^n$ by checking the step from $A^3$ to $A^4$ using matrix multiplication:

$$A^4 = A^3 \cdot A = \begin{pmatrix} 8 & 12 \\ 0 & 8 \\ \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \\ \end{pmatrix} = \begin{pmatrix} 8\cdot 2 + 12\cdot 0 & 8\cdot 1 + 12\cdot 2 \\ 0\cdot 2 + 8\cdot 0 & 0\cdot 1 + 8\cdot 2 \\ \end{pmatrix} = \begin{pmatrix} 16 & 32 \\ 0 & 16 \\ \end{pmatrix}$$

Evaluating the general formula for $n = 4$ yields:  $$
A^4 =
\begin{pmatrix}
2^4 & 4\cdot 2^{4-1} \\
0 & 2^4 \\
\end{pmatrix}
=
\begin{pmatrix}
16 & 4\cdot 8 \\
0 & 16 \\
\end{pmatrix}
=
\begin{pmatrix}
16 & 32 \\
0 & 16 \\
\end{pmatrix
