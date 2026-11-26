### Exercise 1. Definition of the Inverse

## Question

For

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}, \quad
B = \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

1. **Definition of the Inverse Matrix:**
   An $n \times n$ square matrix $B$ is the inverse of a square matrix $A$ (written $B = A^{-1}$) if and only if multiplying them in both orders yields the $n \times n$ identity matrix $I$:

$$
AB = I \quad \text{and} \quad BA = I
$$

   For $2 \times 2$ matrices, the identity matrix is:

$$
I = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

2. **Compute $AB$:**
   Multiply $A$ on the right by $B$:

$$
\begin{aligned}
AB &= \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
2(1) + 1(-1) & 2(-1) + 1(2) \\
1(1) + 1(-1) & 1(-1) + 1(2) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 - 1 & -2 + 2 \\
1 - 1 & -1 + 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

   Thus, $AB = I$.

3. **Compute $BA$:**
   Multiply $A$ on the left by $B$:

$$
\begin{aligned}
BA &= \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(2) + (-1)(1) & 1(1) + (-1)(1) \\
(-1)(2) + 2(1) & (-1)(1) + 2(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 - 1 & 1 - 1 \\
-2 + 2 & -1 + 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

   Thus, $BA = I$.

4. **Conclusion:**
   Because both products $AB$ and $BA$ equal the $2 \times 2$ identity matrix $I$, matrix $B$ satisfies the exact definition of the multiplicative inverse of $A$. Therefore, **$B = A^{-1}$**.

## Verification

We can verify that $B$ undoes the action of $A$ on an arbitrary test vector, such as:

$$
\mathbf{x} = \begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
$$

- **First apply $A$ to $\mathbf{x}$:**

$$
\mathbf{y} = A\mathbf{x} = \begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
= \begin{pmatrix}
2(3) + 1(4) \\
1(3) + 1(4) \\
\end{pmatrix}
= \begin{pmatrix}
10 \\
7 \\
\end{pmatrix}
$$

- **Next apply $B$ to $\mathbf{y}$:**

$$
B\mathbf{y} = \begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
10 \\
7 \\
\end{pmatrix}
= \begin{pmatrix}
1(10) + (-1)(7) \\
(-1)(10) + 2(7) \\
\end{pmatrix}
= \begin{pmatrix}
10 - 7 \\
-10 + 14 \\
\end{pmatrix}
= \begin{pmatrix}
3 \\
4 \\
\end{pmatrix}
= \mathbf{x}
$$

Applying $B$ after $A$ recovers the original vector $\mathbf{x}$ identically, confirming that $B = A^{-1}$.
