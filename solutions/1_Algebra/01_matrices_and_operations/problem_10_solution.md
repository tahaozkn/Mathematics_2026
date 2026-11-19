### Exercise 10. Columns of a Matrix Product

## Question

Given

$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \\ \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \\ \end{pmatrix}.$$

Denote the columns of $B$ by $\mathbf{b}_1, \mathbf{b}_2$.

1. Compute $A\mathbf{b}_1$ and $A\mathbf{b}_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $A\mathbf{b}_1$ and $A\mathbf{b}_2$.

## Solution

1. **Compute $A\mathbf{b}_1$ and $A\mathbf{b}_2$:**
   Extract the two columns of the $3 \times 2$ matrix $B$:

$$\mathbf{b}_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \\ \end{pmatrix}, \quad \mathbf{b}_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \\ \end{pmatrix}$$

   - **Compute $A\mathbf{b}_1$:**

$$\begin{aligned} A\mathbf{b}_1 &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3) \\ \end{pmatrix} \\ &= \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \\ \end{pmatrix} \\ &= \begin{pmatrix} -1 \\ 2 \\ \end{pmatrix} \end{aligned}$$

   - **Compute $A\mathbf{b}_2$:**

$$\begin{aligned} A\mathbf{b}_2 &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \\ \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1) \\ \end{pmatrix} \\ &= \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 2 \\ 1 \\ \end{pmatrix} \end{aligned}$$

2. **Compute the Matrix Product $AB$:**
   Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, their product $AB$ is a $2 \times 2$ matrix whose $(i, j)$-th entry is the dot product of the $i$-th row of $A$ and the $j$-th column of $B$:

$$\begin{aligned} AB &= \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} 1(1) + 2(-1) + 0(3) & 1(2) + 2(0) + 0(1) \\ 0(1) + 1(-1) + 1(3) & 0(2) + 1(0) + 1(1) \\ \end{pmatrix} \\ &= \begin{pmatrix} 1 - 2 + 0 & 2 + 0 + 0 \\ 0 - 1 + 3 & 0 + 0 + 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} -1 & 2 \\ 2 & 1 \\ \end{pmatrix} \end{aligned}$$

3. **Comparison and Explanation:**
   Comparing the results from parts 1 and 2 shows that the first column of $AB$ is $\begin{pmatrix} -1 \\ 2 \\ \end{pmatrix} = A\mathbf{b}_1$, and the second column of $AB$ is $\begin{pmatrix} 2 \\ 1 \\ \end{pmatrix} = A\mathbf{b}_2$:

$$AB = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 \\ \end{pmatrix}$$

   **Why this holds in general:**
   By definition of matrix multiplication, the $j$-th column of the product $AB$ is formed by taking the inner product of each row of $A$ with the $j$-th column of $B$ ($\mathbf{b}_j$). That sequence of row-by-column dot products is the exact definition of the matrix-vector product $A\mathbf{b}_j$. Equivalently, each column of $AB$ is a linear combination of the columns of $A$ weighted by the entries of the corresponding column of $B$, meaning matrix multiplication acts column-by-column on $B$.

## Verification

We can verify the columns of $AB$by expressing each matrix-vector product$A\mathbf{b}_j$directly as a linear combination of the columns of$A$:  $$
\mathbf{a}_1 = \begin{pmatrix}
1 \\
0 \\
\end{pmatrix}, \quad
\mathbf{a}_2 = \begin{
