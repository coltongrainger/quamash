---
title: Special Matrices
---

\renewcommand{\abs}[1]{\lvert #1\rvert}

When the set of $n \times n$ matrices with entries from $\mathbf{F}$ forms a ring under matrix addition and multiplication, we have a [Matrix Ring](https://en.wikipedia.org/wiki/Matrix_ring) (or "full ring of n-by-n matrices") over the field $\mathbf{F}$, denoted $\mathcal{M}_n(\mathbf{F})$ (or generally $\mathcal{M}_n$).

For example, the [Biquaternions](https://en.wikipedia.org/wiki/Biquaternion), $\mathcal{M}_2(\mathbf{C})$ were in algebraic vogue among British mathematicians during the middle of the 19th century. A notable subset is the set of [Pauli Matrices](https://en.wikipedia.org/wiki/Pauli_matrices)---the biquaternions $hi$, $hj$, $hk$---which forms a basis for the vector space of $2 \times 2$ Hermitian matrices.

DEF! $A \in \mathcal{M}_n$ is positive definite iff ... $x^T A x > 0$ for all $x \neq 0$. 

DEF! $A \in \mathcal{M}_n$ is strictly diagonally dominant iff ... $$\abs{a_{ii}} > \sum_{j\neq i} \abs{a_{ij}}.$$

DEF! $A \in \mathcal{M}_n$ is called a band matrix (with bandwidth $2p+1$) iff ... $a_{ij} = 0$ for $\abs{i-j} > p$.
