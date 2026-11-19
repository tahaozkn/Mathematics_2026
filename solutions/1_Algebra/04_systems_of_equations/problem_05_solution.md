### Exercise 5. Row Echelon Form and Number of Solutions

## Question

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## Solution

1. **Number of Solutions:**
   Let the variables corresponding to the three coefficient columns be $x$, $y$, and $z$. 
   - The matrix is already in row echelon form.
   - The third row is $\begin{pmatrix} 0 & 0 & 0 & \mid & 0 \end{pmatrix}$, which represents the identity $0 = 0$. Since there is no row of the form $\begin{pmatrix} 0 & 0 & 0 & \mid & c \end{pmatrix}$ with $c \neq 0$, the system is **consistent**.
   - There are $r = 2$ non-zero rows (pivots in column 1 and column 2) and $n = 3$ unknowns. Because the number of pivots is strictly less than the number of unknowns ($r < n$), the system has **infinitely many solutions**.

2. **Number of Free Variables:**
   The number of variables that can be chosen freely equals the number of non-pivot columns (free variables), given by $n - r = 3 - 2 = 1$. 
   - Columns 1 and 2 contain leading entries (pivots), making $x$ and $y$ **basic (pivot) variables**.
   - Column 3 does not contain a pivot, so **$z$ is the single free variable** and may be assigned any real parameter $t \in \mathbb{R}$.

3. **Parametric Form of the Solutions:**
   Rewriting the non-zero rows as a system of linear equations:

$$
\begin{cases}
x + 2y - z = 3, \\
y + 2z = 1.
\end{cases}
$$

   Set the free variable $z = t$, where $t \in \mathbb{R}$. Solve for the basic variables using back-substitution:
   - From the second equation:

$$
y + 2t = 1 \implies y = 1 - 2t
$$

   - Substitute $y = 1 - 2t$ and $z = t$ into the first equation:

$$
\begin{aligned}
x + 2(1 - 2t) - t &= 3 \\
x + 2 - 4t - t &= 3 \\
x - 5t &= 1 \\
x &= 1 + 5t
\end{aligned}
$$

   Writing the solution set in vector parametric form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t \begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix}, \quad t \in \mathbb{R}
$$

## Verification

Choose a specific parameter value, such as $t = 1$, to obtain a sample solution:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
1 + 5(1) \\
1 - 2(1) \\
1 \\
\end{pmatrix}
= \begin{pmatrix}
6 \\
-1 \\
1 \\
\end{pmatrix}
$$

Substitute $(x, y, z) = (6, -1, 1)$ back into the equations represented by the augmented matrix:

- **Row 1:** $1(6) + 2(-1) - 1(1) = 6 - 2 - 1 = 3$ (Matches $3$)
- **Row 2:** $0(6) + 1(-1) + 2(1) = -1 + 2 = 1$ (Matches $1$)
- **Row 3:** $0(6) + 0(-1) + 0(1) = 0$ (Matches $0$)

All equations are satisfied, confirming the validity of the parametric representation.
