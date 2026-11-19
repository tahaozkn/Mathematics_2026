### Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

For

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI, \quad IA, \quad A + 0, \quad A^2, \quad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

1. **Identify the $2 \times 2$ Identity and Zero Matrices:**
   Since $A$ is a $2 \times 2$ matrix, the corresponding identity matrix $I$ and zero matrix $0$ have dimensions $2 \times 2$:

$$
I = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad
0 = \begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

2. **Compute $AI$, $IA$, and $A + 0$:**
   - **Right multiplication by $I$ ($AI$):**

$$
\begin{aligned}
AI &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
   &= \begin{pmatrix}
2(1) + 1(0) & 2(0) + 1(1) \\
0(1) + 2(0) & 0(0) + 2(1) \\
\end{pmatrix} \\
   &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
   &= A
\end{aligned}
$$

   - **Left multiplication by $I$ ($IA$):**

$$
\begin{aligned}
IA &= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
   &= \begin{pmatrix}
1(2) + 0(0) & 1(1) + 0(2) \\
0(2) + 1(0) & 0(1) + 1(2) \\
\end{pmatrix} \\
   &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
   &= A
\end{aligned}
$$

   - **Addition with the zero matrix ($A + 0$):**

$$
\begin{aligned}
A + 0 &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
+ \begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix} \\
      &= \begin{pmatrix}
2 + 0 & 1 + 0 \\
0 + 0 & 2 + 0 \\
\end{pmatrix} \\
      &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
      &= A
\end{aligned}
$$

3. **Compute $A^2$ and $A^3$:**
   - **Second power ($A^2 = AA$):**

$$
\begin{aligned}
A^2 &= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
    &= \begin{pmatrix}
2(2) + 1(0) & 2(1) + 1(2) \\
0(2) + 2(0) & 0(1) + 2(2) \\
\end{pmatrix} \\
    &= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\end{aligned}
$$

   - **Third power ($A^3 = A^2A$):**

$$
\begin{aligned}
A^3 &= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
    &= \begin{pmatrix}
4(2) + 4(0) & 4(1) + 4(2) \\
0(2) + 4(0) & 0(1) + 4(2) \\
\end{pmatrix} \\
    &= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
\end{aligned}
$$

4. **Roles of the Matrices $I$ and $0$:**
   - **Identity Matrix ($I$):** Acts as the **multiplicative identity (neutral element)** for matrix multiplication, analogous to the scalar $1$ in real arithmetic. Multiplying any compatible matrix $A$ by $I$ on either the left or the right leaves $A$ completely unchanged ($AI = IA = A$).
   - **Zero Matrix ($0$):** Acts as the **additive identity (neutral element)** for matrix addition, analogous to the scalar $0$ in real arithmetic. Adding $0$ to any matrix $A$ of the same dimensions leaves every entry unchanged ($A + 0 = A$).

5. **Pattern in Successive Powers of $A$:**
   Comparing the first three powers of $A$:

$$
A^1 = \begin{pmatrix}
2^1 & 1 \cdot 2^0 \\
0 & 2^1 \\
\end{pmatrix}
= \begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}, \quad
A^2 = \begin{pmatrix}
2^2 & 2 \cdot 2^1 \\
0 & 2^2 \\
\end{pmatrix}
= \begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}, \quad
A^3 = \begin{pmatrix}
2^3 & 3 \cdot 2^2 \\
0 & 2^3 \\
\end{pmatrix}
= \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

   For any positive integer $n \geq 1$:
   - The **diagonal entries** both equal $2^n$.
   - The **bottom-left entry** remains strictly $0$ because $A$ is upper triangular, and products of upper triangular matrices remain upper triangular.
   - The **top-right entry** equals $n \cdot 2^{n-1}$.

   In general, the $n$-th power of $A$ follows the closed-form formula:

$$
A^n = \begin{pmatrix}
2^n & n \cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$

## Verification

We can verify the general formula for $n = 3$ and test the inductive step for $n = 4$:

- **Check $n = 3$:**

$$
\begin{pmatrix}
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

  This matches the direct computation of $A^3$.

- **Check $n = 4$ (Direct Multiplication vs. Formula):**
  Using direct multiplication $A^4 = A^3 A$:

$$
A^4 = \begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= \begin{pmatrix}
16 & 8 + 24 \\
0 & 16 \\
\end{pmatrix}
= \begin{pmatrix}
16 & 32 \\
0 & 16 \\
\end{pmatrix}
$$

  Using the pattern formula for $n = 4$:

$$
\begin{pmatrix}
2^4 & 4 \cdot 2^3 \\
0 & 2^4 \\
\end{pmatrix}
= \begin{pmatrix}
16 & 4 \cdot 8 \\
0 & 16 \\
\end{pmatrix}
= \begin{pmatrix}
16 & 32 \\
0 & 16 \\
\end{pmatrix}
$$

Both methods yield the exact same matrix, confirming the observed pattern.
