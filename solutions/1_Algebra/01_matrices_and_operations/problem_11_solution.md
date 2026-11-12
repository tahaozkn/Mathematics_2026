### Exercise 11. When Do Matrices Commute?

## Question

Given

$$A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix}, \qquad B = \begin{pmatrix} a & b \\ c & d \\ \end{pmatrix}$$

Find the conditions on $a$, $b$, $c$, and $d$ under which $AB = BA$. Describe the general form of all such matrices $B$.

## Solution

To find when $A$ and $B$ commute, we compute both products $AB$ and $BA$ and equate their corresponding entries.

First, compute $AB$:

$$\begin{aligned} AB &= \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix} \begin{pmatrix} a & b \\ c & d \\ \end{pmatrix} \\ &= \begin{pmatrix} 1\cdot a + 1\cdot c & 1\cdot b + 1\cdot d \\ 0\cdot a + 1\cdot c & 0\cdot b + 1\cdot d \\ \end{pmatrix} \\ &= \begin{pmatrix} a+c & b+d \\ c & d \\ \end{pmatrix} \end{aligned}$$

Next, compute $BA$:

$$\begin{aligned} BA &= \begin{pmatrix} a & b \\ c & d \\ \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} a\cdot 1 + b\cdot 0 & a\cdot 1 + b\cdot 1 \\ c\cdot 1 + d\cdot 0 & c\cdot 1 + d\cdot 1 \\ \end{pmatrix} \\ &= \begin{pmatrix} a & a+b \\ c & c+d \\ \end{pmatrix} \end{aligned}$$

Setting $AB = BA$ yields the matrix equation:

$$\begin{pmatrix} a+c & b+d \\ c & d \\ \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \\ \end{pmatrix}$$

Equating the corresponding entries gives a system of equations:
1. $a+c = a \implies c = 0$
2. $b+d = a+b \implies d = a$
3. $c = c$ (trivially satisfied since $c = 0$)
4. $d = c+d \implies c = 0$ (consistent with the first condition)

Thus, the conditions for $AB = BA$ are that **$c = 0$** and **$d = a$**, while $b$ can be any arbitrary real number.

**General form of matrix $B$:**
Substituting these conditions into $B$ gives:

$$B = \begin{pmatrix} a & b \\ 0 & a \\ \end{pmatrix}$$

where $a$ and $b$ are any real numbers.

## Verification

To
