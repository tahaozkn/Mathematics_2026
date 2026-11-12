### Exercise 10. Columns of a Matrix Product

## Question

Given

$$A = \begin{pmatrix} 1 & 2 \\ 0 & 0 \\ 1 & 1 \\ \end{pmatrix}$$

and

$$B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \\ \end{pmatrix}$$

Denote the columns of $B$ by $b_1$ and $b_2$.
1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

Let the columns of $B$ be

$$b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \\ \end{pmatrix}, \qquad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \\ \end{pmatrix}$$

**1. Computing $Ab_1$ and $Ab_2$:**

$$Ab_1 = \begin{pmatrix} 1 & 2 \\ 0 & 0 \\ 1 & 1 \\ \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \\ \end{pmatrix} = \begin{pmatrix} 1\cdot 1 + 2\cdot (-1) \\ 0\cdot 1 + 0\cdot (-1) \\ 1\cdot 1 + 1\cdot (-1) \\ \end{pmatrix} + \text{Wait, the inner dimensions must match.}$$

Let's check the size of $A$ and $B$:
Matrix $A$ is $3 \times 2$, and matrix $B$ is $3 \times 2$. 
Wait, a $3 \times 2$ matrix $A$ cannot multiply a $3 \times 1$ vector $b_1$ (since $2 \neq 3$). 

Let's re-read the input matrices from the prompt carefully:
$A = \begin{pmatrix} 1 & 2 \\ 0 & 0 \\ 1 & 1 \end{pmatrix}$ (size $3 \times 2$)
$B = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 1 \end{pmatrix}$? No, wait, the prompt text says:
`A=(120011),B=(12−1031)` -> Wait, let's look at how the prompt wrote it:
`A=(120011)` -> $A = \begin{pmatrix} 1 & 2 \\ 0 & 0 \\ 1 & 1 \end{pmatrix}$ has rows (1, 2), (0, 0), (1, 1)? Wait, let's look at the spacing: `(120011)` -> $3 \times 2$? 
Wait, let's check $B$: `(12-1031)` -> $B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}$ which is size $3 \times 2$.
If $A$ is $3 \times 2$ and $B$ is $3 \times 2$, then the product $AB$ is **undefined** because the inner dimensions ($2$ and $3$) do not match!
Wait, let's re-examine the matrices as typically given in this exercise sheet format. Usually $A$ is $2 \times 3$ or $B$ is $2 \times 2$, etc. Let's look at the text:
`A=(120011)` -> rows could be $(1, 2, 0)$ and $(0, 1, 1)$, meaning size $2 \times 3$!
Let's check:
$$A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \\ \end{pmatrix}$$
And $B$:
$$B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \\ \end{pmatrix}$$
Here, $A$ is $2 \times 3$ and $B$ is $3 \times 2$. Then $A$ is $2 \times 3$ and $B$ is $3 \times 2$, so the inner dimensions match ($3 = 3$), and $AB$ is a $2 \times 2$ matrix!
Let's verify the entries for $A$ from `(120011)`: row
