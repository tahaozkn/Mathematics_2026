### Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

Given

$$
A =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},
\qquad
B =
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},
\qquad
C =
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

**Path 1: Computing $(AB)C$**

First, multiply $A$ ($2 \times 3$) by $B$ ($3 \times 2$) to get a $2 \times 2$ matrix:

$$
\begin{aligned}
AB &=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 1 + 2\cdot 2 + 0\cdot (-1) & 1\cdot 0 + 2\cdot 1 + 0\cdot 3 \\
0\cdot 1 + 1\cdot 2 + 1\cdot (-1) & 0\cdot 0 + 1\cdot 1 + 1\cdot 3 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\end{aligned}
$$

Next, multiply $(AB)$ ($2 \times 2$) by $C$ ($2 \times 2$):

$$
\begin{aligned}
(AB)C &=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5\cdot 2 + 2\cdot 0 & 5\cdot 1 + 2\cdot (-1) \\
1\cdot 2 + 4\cdot 0 & 1\cdot 1 + 4\cdot (-1) \\
\end{pmatrix} \\
&=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
\end{aligned}
$$

**Path 2: Computing $A(BC)$**

First, multiply $B$ ($3 \times 2$) by $C$ ($2 \times 2$) to get a $3 \times 2$ matrix:

$$
\begin{aligned}
BC &=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot (-1) \\
2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot (-1) \\
(-1)\cdot 2 + 3\cdot 0 & (-1)\cdot 1 + 3\cdot (-1) \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}
\end{aligned}
$$

Next, multiply $A$ ($2 \times 3$) by $(BC)$ ($3 \times 2$):

$$
\begin{aligned}
A(BC) &=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 2 + 2\cdot 4 + 0\cdot (-2) & 1\cdot 1 + 2\cdot 1 + 0\cdot (-4) \\
0\cdot 2 + 1\cdot 4 + 1\cdot (-2) & 0\cdot 1 + 1\cdot 1 + 1\cdot (-4) \\
\end{pmatrix} \\
&=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
\end{aligned}
$$

**Comparison of results and intermediate operations:**
- **Results:** Both paths yield the exact same matrix, $(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$.
- **Operation count:** Multiplying an $m \times n$ matrix by an $n \times p$ matrix requires $mnp$ scalar multiplications.
  - For $(AB)C$: Computing $AB$ requires $2 \cdot 3 \cdot 2 = 12$ scalar multiplications, and multiplying by $C$ requires $2 \cdot 2 \cdot 2 = 8$, for a total of **$20$ scalar multiplications** (and $12$ additions).
  - For $A(BC)$: Computing $BC$ requires $3 \cdot 2 \cdot 2 = 12$ scalar multiplications, and multiplying by $A$ requires $2 \cdot 3 \cdot 2 = 12$, for a total of **$24$ scalar multiplications** (and $14$ additions).

**Meaning of associativity:** 
Associativity means that when multiplying a chain of matrices in a fixed order, grouping adjacent pairs with parentheses in different ways produces the exact same final matrix. Although the final answer never changes, the choice of grouping alters the size of the intermediate matrices and therefore changes the total computational cost.

## Verification

We can verify the final product by applying both groupings to the test vector

$$
v =
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
$$

Using our final matrix product:

$$
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
=
\begin{pmatrix}
13 \\
-1 \\
\end{pmatrix}
$$

Applying the individual matrices sequentially from right to left ($A(B(Cv))$):
1. $Cv = \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 3 \\ -1 \end{pmatrix}$
2. $B(Cv) = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 3 \\ -1 \end{pmatrix} = \begin{pmatrix} 3 \\ 5 \\ -6 \end{pmatrix}$
3. $A(B(Cv)) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 3 \\ 5 \\ -6 \end{pmatrix} = \begin{pmatrix} 13 \\ -1 \end{pmatrix}$

Both evaluations produce $\begin{pmatrix} 13 \\ -1 \end{pmatrix}$, confirming the accuracy of both multiplication paths.
