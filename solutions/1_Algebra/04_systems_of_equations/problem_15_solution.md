### Exercise 15. Classifying Three Systems

## Question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x + y = 2, \\
x - y = 0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## Solution

### System 1

1. **Minimal Elimination:**
   Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}
$$

   Eliminate $x$ from the second row using the row operation $R_2 \leftarrow R_2 - R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}
$$

2. **Classification and Justification:**
   - **Type:** **One solution** (consistent and determined).
   - **Justification:** Every column of the coefficient matrix contains a non-zero pivot ($1$ in the first column and $-2$ in the second column). Because the number of pivots ($r = 2$) equals the number of unknowns ($n = 2$), there are no free variables and no contradictory rows. Back-substitution yields a unique pair $(x, y) = (1, 1)$.

---

### System 2

1. **Minimal Elimination:**
   Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}
$$

   Eliminate $x$ from the second row using the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

2. **Classification and Justification:**
   - **Type:** **Infinitely many solutions** (consistent and underdetermined).
   - **Justification:** The second row reduces entirely to $\begin{pmatrix} 0 & 0 & \mid & 0 \end{pmatrix}$, representing the identity $0 = 0$, so the system is consistent. However, there is only $r = 1$ pivot (in column 1) for $n = 2$ variables. Column 2 has no pivot, leaving $y = t$ ($t \in \mathbb{R}$) as a free variable and producing infinitely many solutions of the form $(x, y) = (2 - t, t)$.

---

### System 3

1. **Minimal Elimination:**
   Set up the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}
$$

   Eliminate $x$ from the second row using the row operation $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

2. **Classification and Justification:**
   - **Type:** **No solution** (inconsistent).
   - **Justification:** The second row has all zeros on the coefficient side and a non-zero constant $1$ on the right-hand side, representing the impossible equation $0x + 0y = 1$, or $0 = 1$. Because no values of $x$ and $y$ can satisfy this contradiction, the solution set is empty.

## Verification

- **System 1:** Substituting $(x, y) = (1, 1)$ gives $1 + 1 = 2$ and $1 - 1 = 0$, confirming the unique intersection point.
- **System 2:** Choosing $t = 0$ gives $(2, 0)$ ($2 + 0 = 2$ and $2(2) + 2(0) = 4$), while choosing $t = 1$ gives $(1, 1)$ ($1 + 1 = 2$ and $2(1) + 2(1) = 4$), confirming multiple solutions.
- **System 3:** Multiplying the first equation $x + y = 2$ by $2$ yields $2x + 2y = 4$, which directly conflicts with the second equation $2x + 2y = 5$, confirming inconsistency.
