### Exercise 14. A Small Change in the Right-Hand Side

## Question

Compare the systems

**System 1**

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3
\end{cases}
$$

and

**System 2**

$$
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

## Solution

### Consistency Check for System 1

1. **Set up the Augmented Matrix:**
   Write System 1 in augmented matrix form:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3 \\
\end{pmatrix}
$$

2. **Gaussian Elimination:**
   Eliminate $x$ from the second and third rows using $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & -3 & \mid & -3 \\
\end{pmatrix}
$$

   Eliminate the third row using $R_3 \leftarrow R_3 - R_2$, and scale the second row using $R_2 \leftarrow -\frac{1}{3}R_2$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 1 & \mid & 1 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

3. **Conclusion for System 1:**
   The third row represents $0x + 0y = 0$, which is an identity. There are $r = 2$ non-zero pivot rows for $n = 2$ unknowns. Back-substitution gives $y = 1$ and $x = 2 - 1 = 1$. Therefore, **System 1 is consistent** and has a unique solution $(x, y) = (1, 1)$.

---

### Consistency Check for System 2

1. **Set up the Augmented Matrix:**
   Write System 2 in augmented matrix form:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3.1 \\
\end{pmatrix}
$$

2. **Gaussian Elimination:**
   Apply the exact same row operations ($R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$):

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & -3 & \mid & -2.9 \\
\end{pmatrix}
$$

   Subtract Row 2 from Row 3 ($R_3 \leftarrow R_3 - R_2$):

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & 0.1 \\
\end{pmatrix}
$$

3. **Conclusion for System 2:**
   The third row represents the equation $0x + 0y = 0.1$, or $0 = 0.1$, which is a mathematical contradiction. Therefore, **System 2 is inconsistent** and has **no solution**.

---

### Why a Small Change Changes the System Type

Both systems are **overdetermined** ($3$ equations in $2$ unknowns), and the left-hand sides of the three equations are linearly dependent: adding the first equation ($x + y$) and the second equation ($2x - y$) always equals the third left-hand side ($3x$).

- For the system to remain consistent, the right-hand sides must satisfy the exact same linear relation: $b_1 + b_2 = b_3$.
- In **System 1**, $2 + 1 = 3$, so the third equation passes directly through the unique intersection point $(1, 1)$ of the first two lines, making it redundant and preserving consistency.
- In **System 2**, changing $3$ to $3.1$ breaks this balance ($2 + 1 \neq 3.1$). Geometrically, the first two lines intersect at $(1, 1)$, while the third line is shifted slightly to $x = \frac{3.1}{3} = 1.033\dots$, missing their intersection point. Because three lines in a plane only share a common point under an exact algebraic condition, any arbitrarily small perturbation off that condition destroys the common intersection and turns a consistent system into an inconsistent one.

## Verification

- **System 1 Check with $(x, y) = (1, 1)$:**
  - $1 + 1 = 2$ (Matches $2$)
  - $2(1) - 1 = 1$ (Matches $1$)
  - $3(1) = 3$ (Matches $3$)

- **System 2 Check:** The first two equations uniquely force $x = 1$ and $y = 1$, which gives $3x = 3(1) = 3 \neq 3.1$ in the third equation, confirming the inconsistency.
