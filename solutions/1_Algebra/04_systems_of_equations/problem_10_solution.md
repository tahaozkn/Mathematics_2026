### Exercise 10. A Polynomial Through Three Points

## Question

Find a polynomial $p(x) = ax^2 + bx + c$ whose graph passes through $(0, 1)$, $(1, 3)$, and $(2, 9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## Solution

1. **Formulate the Linear System:**
   For the graph of $p(x) = ax^2 + bx + c$ to pass through each given point $(x_i, y_i)$, the polynomial must satisfy $p(x_i) = y_i$:
   - At $(0, 1)$: $a(0)^2 + b(0) + c = 1 \implies c = 1$
   - At $(1, 3)$: $a(1)^2 + b(1) + c = 3 \implies a + b + c = 3$
   - At $(2, 9)$: $a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9$

   This yields a system of three linear equations in the unknown coefficients $a$, $b$, and $c$:

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

2. **Solve the System via Augmented Matrix Elimination:**
   Ordering the columns as $(a, b, c)$, write the augmented matrix:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
4 & 2 & 1 & \mid & 9 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

   Eliminate $a$ from the second row using $R_2 \leftarrow R_2 - 4R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & -2 & -3 & \mid & -3 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

   Scale the second row using $R_2 \leftarrow -\frac{1}{2}R_2$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & 1 & \frac{3}{2} & \mid & \frac{3}{2} \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

3. **Back-Substitution:**
   - From the third row:

$$
c = 1
$$

   - Substitute $c = 1$ into the second row equation $b + \frac{3}{2}c = \frac{3}{2}$:

$$
b + \frac{3}{2}(1) = \frac{3}{2} \implies b = 0
$$

   - Substitute $b = 0$ and $c = 1$ into the first row equation $a + b + c = 3$:

$$
a + 0 + 1 = 3 \implies a = 2
$$

4. **Resulting Polynomial:**
   Substituting $a = 2$, $b = 0$, and $c = 1$ into $p(x) = ax^2 + bx + c$ gives:

$$
p(x) = 2x^2 + 1
$$

## Verification

Evaluate $p(x) = 2x^2 + 1$ at each of the three given $x$-coordinates:

- **At $x = 0$:**

$$
p(0) = 2(0)^2 + 1 = 0 + 1 = 1
$$

  This matches the point $(0, 1)$.

- **At $x = 1$:**

$$
p(1) = 2(1)^2 + 1 = 2 + 1 = 3
$$

  This matches the point $(1, 3)$.

- **At $x = 2$:**

$$
p(2) = 2(2)^2 + 1 = 8 + 1 = 9
$$

  This matches the point $(2, 9)$.

All three points lie on the graph of $p(x) = 2x^2 + 1$, confirming the solution.
