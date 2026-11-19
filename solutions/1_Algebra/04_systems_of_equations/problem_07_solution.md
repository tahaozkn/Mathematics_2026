### Exercise 7. Choosing a Method Deliberately

## Question

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x - y = 3, \\
4y = 8;
\end{cases}
$$

2. three systems $A\mathbf{x} = \mathbf{b}_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3 \times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## Solution

### Case 1: Triangular Coefficient Matrix

- **Chosen Method:** Direct back-substitution.
- **Justification:** In matrix form, the system is

$$
\begin{pmatrix}
2 & -1 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
= \begin{pmatrix}
3 \\
8 \\
\end{pmatrix}
$$

  Because the coefficient matrix is already upper triangular, forward elimination is completely unnecessary. With only a single right-hand side and no entries to eliminate below the main diagonal, solving directly from the bottom equation upward requires the minimum possible number of arithmetic operations.

- **Complete Execution:**
  From the second equation:

$$
4y = 8 \implies y = 2
$$

  Substitute $y = 2$ into the first equation:

$$
\begin{aligned}
2x - 2 &= 3 \\
2x &= 5 \\
x &= \frac{5}{2}
\end{aligned}
$$

  The unique solution vector is:

$$
\mathbf{x} = \begin{pmatrix}
\frac{5}{2} \\
2 \\
\end{pmatrix}
$$

---

### Case 2: Three Systems $A\mathbf{x} = \mathbf{b}_i$ with Known $A^{-1}$

- **Chosen Method:** Direct matrix-vector multiplication using the precomputed inverse ($\mathbf{x}_i = A^{-1}\mathbf{b}_i$).
- **Justification:** There are multiple right-hand sides ($k = 3$ vectors: $\mathbf{b}_1, \mathbf{b}_2, \mathbf{b}_3$) sharing the exact same coefficient matrix $A$, and the inverse $A^{-1}$ is already provided. Computing $A^{-1}$ from scratch is usually computationally expensive, but since it is already available, applying it directly avoids performing three separate Gaussian eliminations.
- **Execution Plan and Reusability:**
  1. Multiply the known inverse matrix $A^{-1}$ by each right-hand side vector separately: $\mathbf{x}_1 = A^{-1}\mathbf{b}_1$, $\mathbf{x}_2 = A^{-1}\mathbf{b}_2$, and $\mathbf{x}_3 = A^{-1}\mathbf{b}_3$ (or compute them simultaneously via the block matrix product $A^{-1}\begin{pmatrix} \mathbf{b}_1 & \mathbf{b}_2 & \mathbf{b}_3 \end{pmatrix}$).
  2. **Reusable part:** The matrix $A^{-1}$ itself is fully reused across all three systems.
  3. **Unnecessary part:** Setting up augmented matrices, performing row reductions, or recomputing row operations for each individual $\mathbf{b}_i$ is completely unnecessary.

---

### Case 3: One $3 \times 3$ System Without Known Inverse

- **Chosen Method:** Gaussian elimination on the augmented matrix $\begin{pmatrix} A & \mid & \mathbf{b} \end{pmatrix}$ followed by back-substitution.
- **Justification:** There is only a single right-hand side vector $\mathbf{b}$ and a general $3 \times 3$ matrix $A$ without special triangular structure or a precomputed inverse. Solving by computing $A^{-1}$ first would require reducing a $3 \times 6$ augmented matrix $\begin{pmatrix} A & \mid & I_3 \end{pmatrix}$ to find all three columns of $A^{-1}$, which does roughly three times as much work on the right-hand side as needed for one vector $\mathbf{b}$.
- **Execution Plan and Reusability:**
  1. Form the single $3 \times 4$ augmented matrix $\begin{pmatrix} A & \mid & \mathbf{b} \end{pmatrix}$, apply elementary row operations to transform $A$ into upper triangular (row echelon) form, and recover $\mathbf{x}$ via back-substitution.
  2. **Reusable part:** Because there is only one right-hand side and no subsequent systems to solve, there is no need to store row multipliers or keep $A^{-1}$ for future reuse.
  3. **Unnecessary part:** Computing the full inverse matrix $A^{-1}$ (or reducing the matrix all the way to reduced row echelon form above the pivots) is unnecessary work since only one solution vector $\mathbf{x}$ is required.

## Verification

For Case 1, substitute $x = \frac{5}{2}$ and $y = 2$ back into the original system:

- **First equation:** $2\left(\frac{5}{2}\right) - 2 = 5 - 2 = 3$ (Matches $3$)
- **Second equation:** $4(2) = 8$ (Matches $8$)

Both equations are satisfied identically, confirming the back-substitution result.
