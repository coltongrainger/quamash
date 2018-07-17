---
title: Interpolation
author: Colton Grainger
---

## Polynomial approximation

To take intuition from [Wikipedia](https://en.wikipedia.org/wiki/Polynomial):

>  Polynomials can be constructed from constants and indeterminates using only addition and multiplication.

The implementation should optimized according to the set from which these constants are chosen.[^mca]

[^mca]: 
    > p. 1 However, we shall see that many algorithms for polynomial arithmetic are similar  to  the  corresponding  algorithms  for  integer  arithmetic,  but simpler due to the lack of carries in polynomial arithmetic. Consider for example addition: the sum of two polynomials of degree $n$ always has degree at most $n$, whereas the sum of two $n$ -digit integers may have $n+1$ digits. Thus, we often describe algorithms for  polynomials  as  an  aid  to  understanding  the  corresponding algorithms for integers.
    >  p. 49 A strong link exists between modular arithmetic and arithmetic on polynomials. One way of implementing finite fields $\FF_q$ with $q = p^n$ elements is to work with polynomials in $\FF_p[x]$, which are reduced modulo a monic irreducible polynomial $f(x)\in\FF_p[x]$ of degree $n$. In this case, modular reduction happens both at the coefficient level (in $F_p$) and at the polynomial level (modulo $f(x)$)
    R. Brent and P. Zimmermann *[Modern Computer Arithmetic](https://members.loria.fr/PZimmermann/mca/mca-cup-0.5.9.pdf)*. Version 0.5.9. Retrieved July 17, 2018.


