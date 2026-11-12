### Exercise 8. Row Operations and Their Reversibility

## Question

For

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:
1. $R_2 \leftarrow R_2 - 2R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

**Step 1:** Perform $R_2 \leftarrow R_2 - 2R_1$. 
Subtracting $2$ times the first row from the second row:

$$
\begin{pmatrix}
1 & 2 & -1 \\
2 - 2(1) & 4 - 2(2) & 1 - 2(-1) \\
-1 & 1 & 3 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

**Step 2:** Perform $R_3 \leftarrow R_3 + R_1$. 
Adding the first row to the third row:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 + 1 & 1 + 2 & 3 + (-1) \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

**Step 3:** Interchange $R_2$ and $R_3$. 
Swapping the second and third rows:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

**Reversing Operations:**
1. The operation $R_2 \leftarrow R_2 - 2R_1$ is reversed by **$R_2 \leftarrow R_2 + 2R_1$**.
2. The operation $R_3 \leftarrow R_3 + R_1$ is reversed by **$R_3 \leftarrow R_3 - R_1$**.
3. Interchanging $R_2$ and $R_3$ is reversed by **interchanging $R_2$ and $R_3$ again**.

## Verification

To verify the reversibility of these transformations, we start from the final matrix and apply the reverse operations in reverse order (Step 3 reverse, then Step 2 reverse, then Step 1 reverse).

Starting from the final matrix:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

1. **Reverse of Step 3 (Interchange $R_2$ and $R_3$):**

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

2. **Reverse of Step 2 ($R_3 \leftarrow R_3 - R_1$):**

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 - 1 & 3 - 2 & 2 - (-1) \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

3. **Reverse of Step 1 ($R_2 \leftarrow R_2 + 2R_1$):**

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 + 2(1) & 0 + 2(2) & 3 + 2(-1) \\
-1 & 1 & 3 \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

This successfully recovers the original matrix $A$, confirming both the intermediate steps and the correctness of the reverse operations.
