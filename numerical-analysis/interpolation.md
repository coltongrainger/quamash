---
title: Interpolation
author: Colton Grainger
---

<meta charset="UTF-8">

## Polynomial approximation

To take intuition from [Wikipedia](https://en.wikipedia.org/wiki/Polynomial):

>  Polynomials can be constructed from constants and indeterminates using only addition and multiplication.

The implementation of said addition and multiplication, of course, should optimized according to the set from which these constants are chosen.[^mca]

[^mca]: R. Brent and P. Zimmermann, *[Modern Computer Arithmetic](https://members.loria.fr/PZimmermann/mca/mca-cup-0.5.9.pdf)*. Version 0.5.9. Retrieved July 17, 2018.

    > We shall see that many algorithms for polynomial arithmetic are similar  to  the  corresponding  algorithms  for  integer  arithmetic,  but simpler due to the lack of carries in polynomial arithmetic. Consider for example addition: the sum of two polynomials of degree $n$ always has degree at most $n$, whereas the sum of two $n$ -digit integers may have $n+1$ digits. Thus, we often describe algorithms for  polynomials  as  an  aid  to  understanding  the  corresponding algorithms for integers. (p. 1)

    >  A strong link exists between modular arithmetic and arithmetic on polynomials. One way of implementing finite fields $\mathbf{F}_q$ with $q = p^n$ elements is to work with polynomials in $\mathbf{F}_p[x]$, which are reduced modulo a monic irreducible polynomial $f(x)\in\mathbf{F}_p[x]$ of degree $n$. In this case, modular reduction happens both at the coefficient level (in $F_p$) and at the polynomial level (modulo $f(x)$). (p. 49)

We'll make concrete use of the familiar [Weierstrass Approximation Theorem](https://en.wikipedia.org/wiki/Stone%E2%80%93Weierstrass_theorem) (only later generalized to $C(X)$, the ring of continuous functions on a compactum $X$ with the topology of uniform convergence, by [Marshall Harvey Stone](https://en.wikipedia.org/wiki/Marshall_Harvey_Stone)):

!THM (Weierstrass Approximation) Given a continuous function $f\colon [a,b] \to \RR$ for all $\varepsilon > 0$ ... there exists a polynomial $p \in \RR[x]$ such that for all $x \in [a,b]$ we have $\abs{f(x) - p(x)} < \varepsilon$.

For notation's sake, we also define a general [polynomial ring](https://en.wikipedia.org/wiki/Polynomial_ring).

!DEF (The polynomial ring $K[X]$) Let $K$ be a field. By the ring of polynomials in the indeterminate, $X$, written as $K[X]$, we mean ... the set of all symbols $$\sum_{i=1}^n a_i X^i$$ where $n \in \NN$ and the coefficients $a_i$ are elements of the field $K$.

Here's the application of polynomial approximation in numerical quadrature:

- I desire $\int_a^b f(x)\, dx$.
- I can bound $\abs{\int_a^b f(x)\, dx - \int_a^b p(x)\, dx} \leq \varepsilon(b-a)$.
- To obtain the desired precision, I ought to control $\varepsilon$.

Taylor polynomials are an obvious candidate to approximate differentiable functions.Yet, rewording Taylor's theorem, we might not have a promising error bound on the remainder over our desired interval of integration.

!FACT (Taylor error bounds) Let $f(x)$ be defined on $[a,b]$ and suppose $f^{(n+1)}$ is (defined and) continuous on $[a,b]$. For any $x, x_0 \in [a,b]$ there exists $\xi(x) = \xi$ between $x$ and $x_0$ such that with $p_n$ is the $n$th degree Taylor polynomial centered at $x_0$ and $r = f - p_n$ we have ... $$r(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}$$.

For example, the Taylor series representation of the function $f(x) = \frac{1}{1+25x^2}$ only converges for $\abs{x}<0.2$. 
