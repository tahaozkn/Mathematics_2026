### Exercise 8. Two Systems with the Same Coefficient Matrix

## Question

Solve by elimination the two systems

**System 1**

$$
\begin{cases}
2x + y = 5, \\
x - y = 1,
\end{cases}
$$

**System 2**

$$
\begin{cases}
2x + y = 1, \\
x - y = 4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## Solution

### Solving System 1

1. **Set up the Augmented Matrix:**

$$
\begin{pmatrix}
2 & 1 & \mid & 5 \\
1 & -1 & \mid & 1 \\
\end{pmatrix}
$$

2. **Elimination Steps:**
   Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) to obtain a leading $1$ in the top-left pivot position:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
2 & 1 & \mid & 5 \\
\end{pmatrix}
$$

   Eliminate $x$ from the second row using $R_2 \leftarrow R_2 - 2R_1$:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 3 & \mid & 3 \\
\end{pmatrix}
$$

   Scale the second row using $R_2 \leftarrow \frac{1}{3}R_2$:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

3. **Back-Substitution:**
   From the second row, $y = 1$. Substituting $y = 1$ into the first row ($x - y = 1$) gives:

$$
x - 1 = 1 \implies x = 2
$$

   The unique solution to System 1 is:

$$
\mathbf{x}_1 = \begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

---

### Solving System 2

1. **Set up the Augmented Matrix:**

$$
\begin{pmatrix}
2 & 1 & \mid & 1 \\
1 & -1 & \mid & 4 \\
\end{pmatrix}
$$

2. **Elimination Steps:**
   Apply the exact same sequence of row operations:
   - Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$):

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
2 & 1 & \mid & 1 \\
\end{pmatrix}
$$

   - Eliminate $x$ from the second row ($R_2 \leftarrow R_2 - 2R_1$):

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 3 & \mid & -7 \\
\end{pmatrix}
$$

   - Scale the second row ($R_2 \leftarrow \frac{1}{3}R_2$):

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 1 & \mid & -\frac{7}{3} \\
\end{pmatrix}
$$

3. **Back-Substitution:**
   From the second row, $y = -\frac{7}{3}$. Substituting $y = -\frac{7}{3}$ into the first row ($x - y = 4$) gives:

$$
x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = \frac{12}{3} \implies x = \frac{5}{3}
$$

   The unique solution to System 2 is:

$$
\mathbf{x}_2 = \begin{pmatrix}
\frac{5}{3} \\
-\frac{7}{3} \\
\end{pmatrix}
$$

---

### Comparison of Elimination Steps

- **What Remains Identical:**
  1. **The sequence of elementary row operations:** Both systems require the exact same operations ($R_1 \leftrightarrow R_2$, followed by $R_2 \leftarrow R_2 - 2R_1$, and finally $R_2 \leftarrow \frac{1}{3}R_2$).
  2. **The left-hand side (coefficient part) of the matrix at every stage:** In both derivations, the coefficient entries transform identically from $\begin{pmatrix} 2 & 1 \\ 1 & -1 \\ \end{pmatrix}$ to $\begin{pmatrix} 1 & -1 \\ 2 & 1 \\ \end{pmatrix}$, then to $\begin{pmatrix} 1 & -1 \\ 0 & 3 \\ \end{pmatrix}$, and finally to $\begin{pmatrix} 1 & -1 \\ 0 & 1 \\ \end{pmatrix}$.

- **Why This Happens:**
  The choice of pivot positions and elimination multipliers depends exclusively on the entries of the coefficient matrix $A$, completely independently of the right-hand side vector $\mathbf{b}$. Performing elementary row operations on an augmented matrix $\begin{pmatrix} A & \mid & \mathbf{b} \end{pmatrix}$ is algebraically equivalent to multiplying both sides of $A\mathbf{x} = \mathbf{b}$ on the left by the same sequence of elementary matrices $E_1, E_2, \dots, E_k$. Because $A$ is identical in both systems, the transformation $E_k \cdots E_2 E_1 A$ produces the exact same echelon matrix on the left, while only the right-hand side vectors transform differently.

## Verification

- **System 1 Check with $(x, y) = (2, 1)$:**
  - $2(2) + 1 = 4 + 1 = 5$ (Matches $5$)
  - $2 - 1 = 1$ (Matches $1$)

- **System 2 Check with $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$:**
  - $2\left(\frac{5}{3}\right) + \left(-\frac{7}{3}\right) = \frac{10}{3} - \frac{7}{3} = \frac{3}{3} = 1$ (Matches $1$)
  - $\frac{5}{3} - \left(-\frac{7}{3}\right) = \frac{5}{3} + \frac{7}{3} = \frac{12}{3} = 4$ (Matches $4$)

Both solutions satisfy their respective original systems identically.
