### Exercise 13. A Recurrence Written in Matrix Form

## Question

Let

$$
F =
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0, 1, 1, 2, 3, 5, 8, \dots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Solution

First, compute the successive powers of $F$:

$$
\begin{aligned}
F^2 &=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\
1\cdot 1 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
F^3 &= F^2 \cdot F \\
&=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot 1 + 1\cdot 1 & 2\cdot 1 + 1\cdot 0 \\
1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
F^4 &= F^3 \cdot F \\
&=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
3\cdot 1 + 2\cdot 1 & 3\cdot 1 + 2\cdot 0 \\
2\cdot 1 + 1\cdot 1 & 2\cdot 1 + 1\cdot 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\end{aligned}
$$

$$
\begin{aligned}
F^5 &= F^4 \cdot F \\
&=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
5\cdot 1 + 3\cdot 1 & 5\cdot 1 + 3\cdot 0 \\
3\cdot 1 + 2\cdot 1 & 3\cdot 1 + 2\cdot 0 \\
\end{pmatrix} \\
&=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
\end{aligned}
$$

**Relationship to the sequence:**
Denote the Fibonacci sequence by $f_0 = 0$, $f_1 = 1$, $f_2 = 1$, $f_3 = 2$, $f_4 = 3$, $f_5 = 5$, $f_6 = 8$, and so on. Each matrix power $F^n$ holds three consecutive terms of this sequence:

$$
F^n =
\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix}
$$

The top-left entry is $f_{n+1}$, the off-diagonal entries are both $f_n$, and the bottom-right entry is $f_{n-1}$.

**Recurrence step via matrix-vector multiplication:**
For an arbitrary column vector with entries $a$ and $b$:

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
=
\begin{pmatrix}
1\cdot a + 1\cdot b \\
1\cdot a + 0\cdot b \\
\end{pmatrix}
=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}
$$

If $a = f_k$ and $b = f_{k-1}$ are two consecutive terms of the recurrence, the first row sums them to produce $a+b = f_k + f_{k-1} = f_{k+1}$, while the second row shifts the upper entry $a = f_k$ downward so it remains available for the subsequent step.

## Verification

We can verify the general formula for $F^n$ by applying $F^5$ to the initial state vector of the sequence,

$$
v_1 =
\begin{pmatrix}
f_1 \\
f_0 \\
\end{pmatrix}
=
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}
$$

Applying $F^5$ should advance the sequence by $5$ steps to yield $\begin{pmatrix} f_6 \\ f_5 \end{pmatrix}$:

$$
F^5 v_1 =
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}
=
\begin{pmatrix}
8\cdot 1 + 5\cdot 0 \\
5\cdot 1 + 3\cdot 0 \\
\end{pmatrix}
=
\begin{pmatrix}
8 \\
5 \\
\end{pmatrix}
$$

In the sequence $0, 1, 1, 2, 3, 5, 8, \dots$, the fifth and sixth terms after $f_0 = 0$ are indeed $f_5 = 5$ and $f_6 = 8$, confirming both the matrix power $F^5$ and its action as a 5-step recurrence operator.
