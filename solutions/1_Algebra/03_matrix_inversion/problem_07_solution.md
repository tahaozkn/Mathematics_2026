### Exercise 7. Inverse of a Product

## Question

For

$$
A = \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}, \quad
B = \begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Solution

1. **Compute $(AB)^{-1}$:**
   - **First compute the matrix product $AB$:**

$$
\begin{aligned}
AB &= \begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(2) + 1(0) & 1(0) + 1(3) \\
0(2) + 1(0) & 0(0) + 1(3) \\
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\end{aligned}
$$

   - **Find the determinant of $AB$:**

$$
\det(AB) = (2)(3) - (3)(0) = 6 - 0 = 6
$$

   - **Apply the $2 \times 2$ inverse formula to $AB$:**

$$
\begin{aligned}
(AB)^{-1} &= \frac{1}{6} \begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{3}{6} & -\frac{3}{6} \\
0 & \frac{2}{6} \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

2. **Compute $B^{-1}A^{-1}$:**
   - **Find $A^{-1}$:**
     Since $\det A = (1)(1) - (1)(0) = 1$:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

   - **Find $B^{-1}$:**
     Since $\det B = (2)(3) - (0)(0) = 6$:

$$
B^{-1} = \frac{1}{6} \begin{pmatrix}
3 & 0 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

   - **Multiply $B^{-1}$ on the right by $A^{-1}$:**

$$
\begin{aligned}
B^{-1}A^{-1} &= \begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\
0(1) + \frac{1}{3}(0) & 0(-1) + \frac{1}{3}(1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

3. **Comparison and Meaning of the Reversed Order:**
   - **Comparison:** Both computations yield the exact same matrix:

$$
(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

   - **Meaning of the Reversed Order ("Socks-and-Shoes" Principle):**
     When applying the product $AB$ to a vector $\mathbf{x}$, we compute $A(B\mathbf{x})$: transformation $B$ acts on $\mathbf{x}$ **first**, and transformation $A$ acts on the result **second**. To undo the combined operation and recover $\mathbf{x}$, we must undo the operations in the **exact reverse order** of how they were applied—first undoing $A$ by multiplying by $A^{-1}$, and then undoing $B$ by multiplying by $B^{-1}$:

$$
(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I
$$

     Because matrix multiplication is non-commutative in general, reversing the order of the inverses is strictly required so that inner adjacent matrices cancel cleanly into the identity matrix $I$.

## Verification

We can verify both that $B^{-1}A^{-1}$ is the true inverse of $AB$ and that multiplying in the non-reversed order ($A^{-1}B^{-1}$) does not yield the identity matrix:

- **Verify $(AB)(B^{-1}A^{-1}) = I$:**

$$
\begin{aligned}
(AB)(B^{-1}A^{-1}) &= \begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\left(\frac{1}{2}\right) + 3(0) & 2\left(-\frac{1}{2}\right) + 3\left(\frac{1}{3}\right) \\
0\left(\frac{1}{2}\right) + 3(0) & 0\left(-\frac{1}{2}\right) + 3\left(\frac{1}{3}\right) \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 + 0 & -1 + 1 \\
0 + 0 & 0 + 1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

- **Contrast with Non-Reversed Order ($A^{-1}B^{-1}$):**

$$
A^{-1}B^{-1} = \begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{2} & -\frac{1}{3} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\neq (AB)^{-1}
$$

This confirms that $(AB)^{-1} = B^{-1}A^{-1}$ and demonstrates why the reversed order is essential.
