### Exercise 11. A Parameter in a System of Three Equations

## Question

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x + y + z = 1, \\
x + ty + z = 2, \\
x + y + tz = 3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## Solution

1. **Set up the Augmented Matrix and Perform Initial Elimination:**
   Write the system in augmented matrix form:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}
$$

   Eliminate $x$ from the second and third rows using the row operations $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t - 1 & 0 & \mid & 1 \\
0 & 0 & t - 1 & \mid & 2 \\
\end{pmatrix}
$$

2. **Identify Where the Standard Division Step Becomes Invalid:**
   To normalize the pivots in rows 2 and 3 (or to solve for $y$ and $z$ by dividing by $t - 1$), we require $t - 1 \neq 0$, meaning $t \neq 1$. When $t = 1$, division by $t - 1$ is undefined and ceases to be valid. Therefore, we separate the analysis into two cases: $t = 1$ and $t \neq 1$.

3. **Case Analysis:**

   - **Case 1: $t = 1$**
     Substitute $t = 1$ directly into the reduced augmented matrix:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}
$$

     The second row corresponds to $0x + 0y + 0z = 1$, and the third row corresponds to $0x + 0y + 0z = 2$. Both statements ($0 = 1$ and $0 = 2$) are mathematical contradictions. Thus, for $t = 1$, the system is inconsistent and has **no solution**.

   - **Case 2: $t \neq 1$**
     Since $t - 1 \neq 0$, we may divide the second and third rows by $t - 1$ ($R_2 \leftarrow \frac{1}{t - 1}R_2$ and $R_3 \leftarrow \frac{1}{t - 1}R_3$):

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 1 & 0 & \mid & \frac{1}{t - 1} \\
0 & 0 & 1 & \mid & \frac{2}{t - 1} \\
\end{pmatrix}
$$

     There are $r = 3$ non-zero pivot rows matching the $n = 3$ unknowns, so the system has **exactly one unique solution** for every $t \neq 1$. Using back-substitution:

$$
z = \frac{2}{t - 1}, \quad y = \frac{1}{t - 1}
$$

     Substitute $y$ and $z$ into the first row equation $x + y + z = 1$:

$$
\begin{aligned}
x &= 1 - \frac{1}{t - 1} - \frac{2}{t - 1} \\
  &= \frac{t - 1 - 3}{t - 1} \\
  &= \frac{t - 4}{t - 1}
\end{aligned}
$$

     The unique solution vector for $t \neq 1$ is:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= \begin{pmatrix}
\frac{t - 4}{t - 1} \\
\frac{1}{t - 1} \\
\frac{2}{t - 1} \\
\end{pmatrix}
$$

4. **Summary of Number of Solutions:**
   - For $t = 1$: **no solution**.
   - For $t \neq 1$: **exactly one solution**.
   - The case of infinitely many solutions never occurs for any $t \in \mathbb{R}$.

## Verification

- **Test $t = 1$:** Substituting $t = 1$ into the original equations gives $x + y + z = 1$, $x + y + z = 2$, and $x + y + z = 3$. Because the same expression $x + y + z$ cannot equal $1$, $2$, and $3$ simultaneously, no solution exists.
- **Test $t = 2$ ($t \neq 1$):** The formula yields $(x, y, z) = (-2, 1, 2)$. Substituting into the original equations:
  - $x + y + z = -2 + 1 + 2 = 1$ (Matches $1$)
  - $x + 2y + z = -2 + 2(1) + 2 = 2$ (Matches $2$)
  - $x + y + 2z = -2 + 1 + 2(2) = 3$ (Matches $3$)

All three equations hold identically, confirming the parametric solution.
