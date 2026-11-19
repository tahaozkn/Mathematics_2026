### Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## Question

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

1. **Set up the Augmented Matrix and Apply Elimination:**
   Write the system in augmented matrix form:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

   Eliminate the entry below the leading $1$ in the first column using the row operation $R_2 \leftarrow R_2 - aR_1$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a - a(1) & a - a(1) & \mid & 4 - a(2) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4 - 2a \\
\end{pmatrix}
$$

2. **Analyze the Second Row Depending on $a$:**
   The second row represents the equation:

$$
0x + 0y = 4 - 2a \implies 0 = 4 - 2a
$$

   - **Case 1: $4 - 2a = 0$ (i.e., $a = 2$)**
     When $a = 2$, the augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

     The second equation reduces to the identity $0 = 0$, leaving a single non-zero equation $x + y = 2$ with $r = 1$ pivot and $n = 2$ variables. Assigning $y = t$ as a free variable ($t \in \mathbb{R}$) gives $x = 2 - t$. Thus, for $a = 2$, the system has **infinitely many solutions**.

   - **Case 2: $4 - 2a \neq 0$ (i.e., $a \neq 2$)**
     When $a \neq 2$, the right-hand side $c = 4 - 2a$ is non-zero. The second row represents the false statement $0 = c$ with $c \neq 0$, which is a contradiction. Thus, for all $a \neq 2$, the system is inconsistent and has **no solution**.

3. **Why Exactly One Solution Cannot Occur:**
   For a linear system in $n = 2$ variables to have a unique solution, the coefficient matrix must have $r = 2$ pivots (non-zero rows with independent leading entries), meaning its determinant must be non-zero. Here, the two rows of the coefficient matrix are proportional for every $a \in \mathbb{R}$:

$$
\det \begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}
= (1)(a) - (1)(a) = 0
$$

   Geometrically, the first equation defines the line $x + y = 2$. For $a = 0$, the second equation becomes $0 = 4$ (no geometric locus). For $a \neq 0$, dividing the second equation by $a$ yields $x + y = \frac{4}{a}$, which represents a line with the exact same slope ($-1$) as the first line. Because two lines with identical slopes can either coincide ($a = 2$) or remain strictly parallel ($a \neq 2$), they can never intersect at a single point.

## Verification

- **Check $a = 2$:** Substituting $a = 2$ into the original system yields $x + y = 2$ and $2x + 2y = 4$. The second equation is simply twice the first, confirming infinitely many solutions along the line $x + y = 2$ (for example, $(x, y) = (1, 1)$ satisfies both $1 + 1 = 2$ and $2(1) + 2(1) = 4$).
- **Check $a \neq 2$ (e.g., $a = 1$):** Substituting $a = 1$ gives $x + y = 2$ and $x + y = 4$, which directly requires $2 = 4$, confirming that no solution exists.
