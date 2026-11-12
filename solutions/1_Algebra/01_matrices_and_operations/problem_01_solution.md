### Exercise 1. Matrix Size and Entries

## Question

Given

$$
A =
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix}
$$

and

$$
B =
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Solution

1. Matrix $A$ has $2$ rows and $3$ columns, so its size is $2 \times 3$. Matrix $B$ has $3$ rows and $2$ columns, so its size is $3 \times 2$.

2. An entry $m_{ij}$ refers to the element in row $i$ and column $j$:
   - $a_{12}$ (row $1$, column $2$ of $A$) is $-1$.
   - $a_{23}$ (row $2$, column $3$ of $A$) is $5$.
   - $b_{21}$ (row $2$, column $1$ of $B$) is $-2$.
   - $b_{32}$ (row $3$, column $2$ of $B$) is $1$.

3. The second row of $A$ as a row vector is

$$
r_2(A) =
\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix}
$$

The first column of $B$ as a column vector is

$$
c_1(B) =
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}
$$

## Verification

Counting the individual elements confirms the stated dimensions: $A$ contains $2 \cdot 3 = 6$ elements and $B$ contains $3 \cdot 2 = 6$ elements. 

Checking the matrix transposes also confirms the indices, since $(M^T)_{ji} = m_{ij}$:

$$
A^T =
\begin{pmatrix}
2 & 0 \\
-1 & 4 \\
3 & 5 \\
\end{pmatrix}
$$

and

$$
B^T =
\begin{pmatrix}
1 & -2 & 4 \\
0 & 3 & 1 \\
\end{pmatrix}
$$

In $A^T$, the entry at position $(2, 1)$ is $-1 = a_{12}$ and the entry at $(3, 2)$ is $5 = a_{23}$. In $B^T$, the entry at $(1, 2)$ is $-2 = b_{21}$ and the entry at $(2, 3)$ is $1 = b_{32}$. Furthermore, the second column of $A^T$ matches the second row of $A$, and the first row of $B^T$ matches the first column of $B$.
