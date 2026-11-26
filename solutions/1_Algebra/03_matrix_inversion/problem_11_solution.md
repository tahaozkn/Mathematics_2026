### Exercise 11. Parameter and Invertibility

## Question

For

$$
A(t) = \begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Solution

1. **Compute the Determinant of $A(t)$:**
   Using the $2 \times 2$ determinant formula $\det A(t) = ad - bc$:

$$
\det A(t) = (1)(1) - (t)(t) = 1 - t^2
$$

2. **Find All Values of $t$ for Which $A(t)$ is Invertible:**
   A square matrix is invertible if and only if its determinant is non-zero:

$$
\begin{aligned}
1 - t^2 &\neq 0 \\
(1 - t)(1 + t) &\neq 0 \\
t \neq 1 \quad &\text{and} \quad t \neq -1
\end{aligned}
$$

   Thus, $A(t)$ is invertible for all real (or complex) numbers $t \in \mathbb{R} \setminus \{-1, 1\}$.

3. **Give a Formula for $A(t)^{-1}$:**
   For any $t \neq \pm 1$, apply the explicit $2 \times 2$ inverse formula by swapping the main diagonal entries ($1$ and $1$), negating the off-diagonal entries ($t$ and $t$), and dividing by $\det A(t) = 1 - t^2$:

$$
A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}
= \begin{pmatrix}
\frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\
-\frac{t}{1 - t^2} & \frac{1}{1 - t^2} \\
\end{pmatrix}
$$

4. **Explain What Happens at the Excluded Values ($t = 1$ and $t = -1$):**
   - **Algebraic Breakdown (Division by Zero):** At $t = 1$ and $t = -1$, the denominator $1 - t^2$ in the scalar factor $\frac{1}{1 - t^2}$ becomes $0$, causing every entry in the formula for $A(t)^{-1}$ to involve division by zero and become undefined (diverging to $\pm\infty$ as $t \to \pm 1$).
   - **Structural Breakdown (Row/Column Dependence):** Substituting the excluded values directly into $A(t)$ reveals why no inverse can exist:
     - When **$t = 1$**, $A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \\ \end{pmatrix}$, where the two rows are identical ($\mathbf{r}_2 = \mathbf{r}_1$).
     - When **$t = -1$**, $A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \\ \end{pmatrix}$, where the second row is the negative of the first ($\mathbf{r}_2 = -\mathbf{r}_1$).
   - In both cases, the rows are linearly dependent, collapsing the 2D plane onto a 1D line and making the transformation irreversible.

## Verification

We can verify the formula for $A(t)^{-1}$ by multiplying $A(t)$ and $A(t)^{-1}$ for any $t \neq \pm 1$:

$$
\begin{aligned}
A(t)A(t)^{-1} &= \begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
\left( \frac{1}{1 - t^2} \begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix} \right) \\
&= \frac{1}{1 - t^2} \begin{pmatrix}
1(1) + t(-t) & 1(-t) + t(1) \\
t(1) + 1(-t) & t(-t) + 1(1) \\
\end{pmatrix} \\
&= \frac{1}{1 - t^2} \begin{pmatrix}
1 - t^2 & -t + t \\
t - t & -t^2 + 1 \\
\end{pmatrix} \\
&= \frac{1}{1 - t^2} \begin{pmatrix}
1 - t^2 & 0 \\
0 & 1 - t^2 \\
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
&= I
\end{aligned}
$$

Since $A(t)A(t)^{-1} = I$ for all $t \neq \pm 1$, the inverse formula is confirmed.
