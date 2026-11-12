### Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrix sizes are

$$
A_{2\times 3}, \quad B_{3\times 4}, \quad C_{4\times 2}, \quad D_{2\times 2}.
$$

For the products

$$
AB, \quad BA, \quad BC, \quad CB, \quad AC, \quad CA, \quad AD, \quad DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

A matrix product $XY$ of an $m \times n$ matrix $X$ and a $p \times q$ matrix $Y$ is defined if and only if the inner dimensions match ($n = p$). When defined, the resulting matrix has size $m \times q$, determined by the outer dimensions.

- **$AB$:** Comparing $(2 \times 3)$ and $(3 \times 4)$, the inner dimensions match ($3 = 3$). The product is **defined** and has size **$2 \times 4$**.
- **$BA$:** Comparing $(3 \times 4)$ and $(2 \times 3)$, the inner dimensions do not match ($4 \neq 2$). The product is **undefined**.
- **$BC$:** Comparing $(3 \times 4)$ and $(4 \times 2)$, the inner dimensions match ($4 = 4$). The product is **defined** and has size **$3 \times 2$**.
- **$CB$:** Comparing $(4 \times 2)$ and $(3 \times 4)$, the inner dimensions do not match ($2 \neq 3$). The product is **undefined**.
- **$AC$:** Comparing $(2 \times 3)$ and $(4 \times 2)$, the inner dimensions do not match ($3 \neq 4$). The product is **undefined**.
- **$CA$:** Comparing $(4 \times 2)$ and $(2 \times 3)$, the inner dimensions match ($2 = 2$). The product is **defined** and has size **$4 \times 3$**.
- **$AD$:** Comparing $(2 \times 3)$ and $(2 \times 2)$, the inner dimensions do not match ($3 \neq 2$). The product is **undefined**.
- **$DA$:** Comparing $(2 \times 2)$ and $(2 \times 3)$, the inner dimensions match ($2 = 2$). The product is **defined** and has size **$2 \times 3$**.

## Verification

We can verify the defined products using the transpose identity $(XY)^T = Y^T X^T$, since a product $XY$ is defined if and only if $Y^T X^T$ is defined, and the resulting transposed size must be $q \times m$.

The transposed matrix sizes are $A^T_{3\times 2}$, $B^T_{4\times 3}$, $C^T_{2\times 4}$, and $D^T_{2\times 2}$:

- **$(AB)^T = B^T A^T$:** $(4 \times 3)$ multiplied by $(3 \times 2)$ is defined and yields size $4 \times 2$, matching $(2 \times 4)^T$.
- **$(BC)^T = C^T B^T$:** $(2 \times 4)$ multiplied by $(4 \times 3)$ is defined and yields size $2 \times 3$, matching $(3 \times 2)^T$.
- **$(CA)^T = A^T C^T$:** $(3 \times 2)$ multiplied by $(2 \times 4)$ is defined and yields size $3 \times 4$, matching $(4 \times 3)^T$.
- **$(DA)^T = A^T D^T$:** $(3 \times 2)$ multiplied by $(2 \times 2)$ is defined and yields size $3 \times 2$, matching $(2 \times 3)^T$.

For each undefined product ($BA$, $CB$, $AC$, $AD$), reversing the order with transposes likewise leaves mismatched inner dimensions, confirming all eight results.
