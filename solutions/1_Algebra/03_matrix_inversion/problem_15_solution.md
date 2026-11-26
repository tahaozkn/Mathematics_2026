### Exercise 15. Two Methods for Solving the Same System

## Question

For

$$
A = \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}, \quad
\mathbf{b} = \begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $A\mathbf{x} = \mathbf{b}$ in two ways:
1. using $A^{-1}\mathbf{b}$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

### Method 1: Using $\mathbf{x} = A^{-1}\mathbf{b}$

1. **Compute the Determinant of $A$:**
   Using the $2 \times 2$ determinant formula $\det A = ad - bc$:

$$
\det A = (2)(3) - (1)(1) = 6 - 1 = 5
$$

   Since $\det A = 5 \neq 0$, $A$ is invertible.

2. **Find the Inverse Matrix $A^{-1}$:**
   Swap the main diagonal entries ($2$ and $3$), negate the off-diagonal entries ($1$ and $1$), and multiply by $\frac{1}{\det A} = \frac{1}{5}$:

$$
A^{-1} = \frac{1}{5} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

3. **Compute $\mathbf{x} = A^{-1}\mathbf{b}$:**
   Multiply $A^{-1}$ by $\mathbf{b}$:

$$
\begin{aligned}
\mathbf{x} &= \frac{1}{5} \begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
3(7) + (-1)(8) \\
(-1)(7) + 2(8) \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
21 - 8 \\
-7 + 16 \\
\end{pmatrix} \\
&= \frac{1}{5} \begin{pmatrix}
13 \\
9 \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
\end{aligned}
$$

---

### Method 2: Using Gaussian Elimination

1. **Set Up the Augmented Matrix $[A \mid \mathbf{b}]$:**

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}
$$

2. **Swap Rows to Avoid Early Fractions:**
   Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) so the top-left pivot is $1$:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}
$$

3. **Forward Elimination (Eliminate Below Pivot 1):**
   Apply the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 - 2(1) & 1 - 2(3) & \mid & 7 - 2(8) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}
$$

4. **Back-Substitution:**
   From the second row, solve for $x_2$:

$$
-5x_2 = -9 \implies x_2 = \frac{9}{5}
$$

   Substitute $x_2 = \frac{9}{5}$ into the first row ($x_1 + 3x_2 = 8$) to solve for $x_1$:

$$
\begin{aligned}
x_1 + 3\left(\frac{9}{5}\right) &= 8 \\
x_1 + \frac{27}{5} &= \frac{40}{5} \\
x_1 &= \frac{40}{5} - \frac{27}{5} = \frac{13}{5}
\end{aligned}
$$

   Thus, the solution vector is:

$$
\mathbf{x} = \begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix}
$$

---

### Comparison of Methods

- **Agreement of Solutions:** Both methods produce the exact same unique solution $\mathbf{x} = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}$.
- **Number of Essential Steps:**
  - **Method 1 ($A^{-1}\mathbf{b}$):** Requires **3 essential steps** (computing $\det A$, writing $A^{-1}$ via the closed-form $2 \times 2$ formula, and multiplying a $2 \times 2$ matrix by a $2 \times 1$ vector). Keeping $\frac{1}{5}$ factored out until the very end keeps all intermediate arithmetic purely in integers.
  - **Method 2 (Gaussian Elimination):** Requires **3–4 essential steps** (forming the augmented matrix, swapping rows, performing one row elimination, and completing two back-substitution equations involving fraction subtraction).
- **Which Method Was Simpler in This Example:**
  For a **single $2 \times 2$ system** with an explicit inverse formula, **Method 1 ($\mathbf{x} = A^{-1}\mathbf{b}$) is slightly simpler and cleaner** because the $2 \times 2$ inverse is immediate and keeping the scalar $\frac{1}{\det A}$ factored out avoids fraction arithmetic until the final step. *(Note: For systems of size $3 \times 3$ or larger, Gaussian elimination is almost always faster and requires fewer operations than computing $A^{-1}$ first, unless the same coefficient matrix $A$ must be solved against many different right-hand side vectors $\mathbf{b}$.)*

## Verification

Substitute $\mathbf{x} = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}$ back into the original matrix equation $A\mathbf{x} = \mathbf{b}$:

$$
\begin{aligned}
A\mathbf{x} &= \begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{13}{5} \\
\frac{9}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
2\left(\frac{13}{5}\right) + 1\left(\frac{9}{5}\right) \\
1\left(\frac{13}{5}\right) + 3\left(\frac{9}{5}\right) \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{26}{5} + \frac{9}{5} \\
\frac{13}{5} + \frac{27}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{35}{5} \\
\frac{40}{5} \\
\end{pmatrix} \\
&= \begin{pmatrix}
7 \\
8 \\
\end{pmatrix} \\
&= \mathbf{b}
\end{aligned}
$$

Since $A\mathbf{x} = \mathbf{b}$, the solution is verified.
