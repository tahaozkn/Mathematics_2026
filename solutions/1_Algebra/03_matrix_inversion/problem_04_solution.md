### Exercise 4. Gauss–Jordan

## Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A = \begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A \mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Solution

1. **Set Up the Augmented Matrix $[A \mid I]$:**
   Attach the $2 \times 2$ identity matrix $I$ to the right side of matrix $A$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

2. **Forward Elimination (Create Zeros Below the First Pivot):**
   Eliminate the $3$ in the second row, first column using the row operation $R_2 \leftarrow R_2 - 3R_1$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 - 3(1) & 5 - 3(2) & \mid & 0 - 3(1) & 1 - 3(0) \\
\end{pmatrix}
= \begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

3. **Scale the Second Pivot to $1$:**
   Multiply the second row by $-1$ using the row operation $R_2 \leftarrow -R_2$:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

4. **Backward Elimination (Create Zeros Above the Second Pivot):**
   Eliminate the $2$ in the first row, second column using the row operation $R_1 \leftarrow R_1 - 2R_2$:

$$
\begin{pmatrix}
1 - 2(0) & 2 - 2(1) & \mid & 1 - 2(3) & 0 - 2(-1) \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

   Since the left block is now the identity matrix $I$, the right block is $A^{-1}$:

$$
A^{-1} = \begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

5. **Why Obtaining $I$ on the Left Gives $A^{-1}$ on the Right:**
   - **Row Operations as Matrix Multiplication:** Every elementary row operation applied to a matrix is equivalent to multiplying that matrix on the left by an elementary matrix $E_i$. Applying a sequence of $k$ row operations corresponds to multiplying on the left by the single combined matrix $E = E_k \cdots E_2 E_1$.
   - **Simultaneous Transformation:** When we apply these operations to the augmented block matrix $[A \mid I]$, we are computing:

$$
E \begin{pmatrix}
A & \mid & I \\
\end{pmatrix}
= \begin{pmatrix}
EA & \mid & EI \\
\end{pmatrix}
= \begin{pmatrix}
EA & \mid & E \\
\end{pmatrix}
$$

   - **Conclusion:** When the left side transforms into the identity matrix ($EA = I$), the combined transformation matrix $E$ must by definition be the inverse matrix $A^{-1}$. Because the exact same row operations were applied to $I$ on the right side, the right block becomes $EI = E = A^{-1}$. (Equivalently, we are simultaneously solving the two linear systems $A\mathbf{x}_1 = \mathbf{e}_1$ and $A\mathbf{x}_2 = \mathbf{e}_2$, whose solutions form the columns of $A^{-1}$.)

## Verification

We can verify the result by multiplying $A$ by $A^{-1}$ and checking the $2 \times 2$ inverse formula:

- **Matrix Multiplication ($AA^{-1} = I$):**

$$
\begin{aligned}
AA^{-1} &= \begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1(-5) + 2(3) & 1(2) + 2(-1) \\
3(-5) + 5(3) & 3(2) + 5(-1) \\
\end{pmatrix} \\
&= \begin{pmatrix}
-5 + 6 & 2 - 2 \\
-15 + 15 & 6 - 5 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

- **$2 \times 2$ Formula Check:**
  With $\det A = (1)(5) - (2)(3) = 5 - 6 = -1$:

$$
A^{-1} = \frac{1}{-1} \begin{pmatrix}
5 & -2 \\
-3 & 1 \\
\end{pmatrix}
= \begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

Both checks confirm that $A^{-1}$ is accurate.
