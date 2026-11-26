### Exercise 5. A $3 \times 3$ Matrix

## Question

Use Gauss–Jordan elimination to find the inverse of

$$
A = \begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

## Solution

1. **Set Up the Augmented Matrix $[A \mid I]$:**
   Attach the $3 \times 3$ identity matrix $I$ to the right of matrix $A$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}
$$

2. **Forward Elimination (Create Zeros Below Pivot 1):**
   Eliminate the $1$ in the third row, first column using the row operation $R_3 \leftarrow R_3 - R_1$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 - 1 & 0 - 1 & 1 - 0 & \mid & 0 - 1 & 0 - 0 & 1 - 0 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}
$$

3. **Forward Elimination (Create Zeros Below Pivot 2):**
   Eliminate the $-1$ in the third row, second column using the row operation $R_3 \leftarrow R_3 + R_2$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 + 0 & -1 + 1 & 1 + 1 & \mid & -1 + 0 & 0 + 1 & 1 + 0 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}
$$

4. **Scale Pivot 3 to $1$:**
   Divide the third row by $2$ using the row operation $R_3 \leftarrow \frac{1}{2}R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

5. **Backward Elimination (Create Zeros Above Pivot 3):**
   Eliminate the $1$ in the second row, third column using the row operation $R_2 \leftarrow R_2 - R_3$:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 - 0 & 1 - 0 & 1 - 1 & \mid & 0 - \left(-\frac{1}{2}\right) & 1 - \frac{1}{2} & 0 - \frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
= \begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

6. **Backward Elimination (Create Zeros Above Pivot 2):**
   Eliminate the $1$ in the first row, second column using the row operation $R_1 \leftarrow R_1 - R_2$:

$$
\begin{pmatrix}
1 - 0 & 1 - 1 & 0 - 0 & \mid & 1 - \frac{1}{2} & 0 - \frac{1}{2} & 0 - \left(-\frac{1}{2}\right) \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0 & \mid & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

7. **Extract the Inverse Matrix $A^{-1}$:**
   Since the left block is now the $3 \times 3$ identity matrix $I$, the right block is $A^{-1}$:

$$
A^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
= \frac{1}{2} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
$$

## Verification

Check the result by computing the matrix product $AA^{-1}$:

$$
\begin{aligned}
AA^{-1} &= \begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\left( \frac{1}{2} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix} \right) \\
&= \frac{1}{2} \begin{pmatrix}
1(1) + 1(1) + 0(-1) & 1(-1) + 1(1) + 0(1) & 1(1) + 1(-1) + 0(1) \\
0(1) + 1(1) + 1(-1) & 0(-1) + 1(1) + 1(1) & 0(1) + 1(-1) + 1(1) \\
1(1) + 0(1) + 1(-1) & 1(-1) + 0(1) + 1(1) & 1(1) + 0(-1) + 1(1) \\
\end{pmatrix} \\
&= \frac{1}{2} \begin{pmatrix}
1 + 1 + 0 & -1 + 1 + 0 & 1 - 1 + 0 \\
0 + 1 - 1 & 0 + 1 + 1 & 0 - 1 + 1 \\
1 + 0 - 1 & -1 + 0 + 1 & 1 + 0 + 1 \\
\end{pmatrix} \\
&= \frac{1}{2} \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

Since $AA^{-1} = I$, the computed inverse matrix $A^{-1}$ is verified.
