### Exercise 12. Formula for a Matrix Power

## Question

Let

$$
A =
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

First, compute the successive powers of $A$:

$$
A^2 = A \cdot A =
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1\cdot 1 + 1\cdot 0 & 1\cdot 1 + 1\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^3 = A^2 \cdot A =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1\cdot 1 + 2\cdot 0 & 1\cdot 1 + 2\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^4 = A^3 \cdot A =
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1\cdot 1 + 3\cdot 0 & 1\cdot 1 + 3\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
$$

**Conjecture:** 
Based on the pattern observed for $n = 2, 3, 4$, the general formula for the $n$-th power of $A$ (for any positive integer $n$) is:

$$
A^n =
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
$$

**Inductive step:**
Assume the formula holds for a given positive integer $n$, so that $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$. To find $A^{n+1}$, we multiply $A^n$ by $A$:

$$
\begin{aligned}
A^{n+1} &= A^n \cdot A \\
&=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 1 + n\cdot 0 & 1\cdot 1 + n\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

This matches the conjectured formula with $n$ replaced by $n+1$, completing the justification.

## Verification

We can verify the formula for $n=5$ by multiplying our known result for $A^4$ by $A$ once more:

$$
A^5 = A^4 \cdot A =
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1\cdot 1 + 4\cdot 0 & 1\cdot 1 + 4\cdot 1 \\
0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 5 \\
0 & 1 \\
\end{pmatrix}
$$

Evaluating the conjectured formula directly for $n = 5$ gives:

$$
A^5 =
\begin{pmatrix}
1 & 5 \\
0 & 1 \\
\end{pmatrix}
$$

Both results are identical, confirming the correctness of the pattern and the inductive derivation.
