---
title: Numerical Analysis
author: Colton Grainger
---

I took this course before I had this wiki setup. Course summary: <http://blog.coltongrainger.com/math-428>.

## Constellation of concepts

- root-finding

- numerical quadrature

    - differentiation
    - integration

- interpolation

- matrix eigenvalue problem

- solution of linear systems

    - error analysis
    - "distance to singularity"

- linearization

    - local/global convergence?

### Desiderata

We can evaluate a method based on:

- accuracy

- stability

- failure modes

- implementation

    - functional/imperative
    - legibility
    - sanity
    - computational complexity

\providecommand{\NN}{\mathbf{N}}
\providecommand{\RR}{\mathbf{R}}
\providecommand{\eps}{\varepsilon}
\providecommand{\abs}[1]{\lvert #1\rvert}
\providecommand{\norm}[1]{\lVert #1\rVert}

## Special Matrices

\renewcommand{\abs}[1]{\lvert #1\rvert}

When the set of $n \times n$ matrices with entries from $\mathbf{F}$ forms a ring under matrix addition and multiplication, we have a [Matrix Ring](https://en.wikipedia.org/wiki/Matrix_ring) (or "full ring of n-by-n matrices") over the field $\mathbf{F}$, denoted $\mathcal{M}_n(\mathbf{F})$ (or generally $\mathcal{M}_n$).

For example, the [Biquaternions](https://en.wikipedia.org/wiki/Biquaternion), $\mathcal{M}_2(\mathbf{C})$ were in algebraic vogue among British mathematicians during the middle of the 19th century. A notable subset is the set of [Pauli Matrices](https://en.wikipedia.org/wiki/Pauli_matrices)---the biquaternions $hi$, $hj$, $hk$---which forms a basis for the vector space of $2 \times 2$ Hermitian matrices.

DEF! $A \in \mathcal{M}_n$ is positive definite iff ... $x^T A x > 0$ for all $x \neq 0$. 

DEF! $A \in \mathcal{M}_n$ is strictly diagonally dominant iff ... $$\abs{a_{ii}} > \sum_{j\neq i} \abs{a_{ij}}.$$

DEF! $A \in \mathcal{M}_n$ is called a band matrix (with bandwidth $2p+1$) iff ... $a_{ij} = 0$ for $\abs{i-j} > p$.

## Vector norms

DEF! A vector norm is a real valued function $\norm{\cdot}\colon \RR^n \to \RR$ with $3$ properties, namely ... it's positive unless zero, or $\norm{x}\geq 0$ and $\norm{x}= 0$ iff $x=0$; it scales, i.e., $\norm{\alpha x} = \abs{\alpha}\cdot \norm{x}$; and it respects the triangle inequality $\norm{x + y} \leq \norm{x}+\norm{y}$.

DEF! The $l_p$ norms (for $p \in \RR^+$) are given by ... $\norm{x}_p = \sqrt[p]{\sum_{i=1}^n \abs{x_i}^p}$.

FACT! The Holder inequality (of which the Cauchy Bunyakovsky Schwarz inequality is a special case) states ... for all $x,y \in \RR^n$ and $p,q$ such that $\frac1p + \frac1q = 1$ we have $\abs{x^Ty} \leq \norm{x}_p\norm{y}_q$.

DEF! The $l_\infty$ norm is ... $\norm{x}_\infty = \max\{\abs{x_i} : i=1,n\}$.

EXAMPLE! The $l_2$ norm is ... $\norm{x}_2 = \sum_{i=1}^n \abs{x_i}^2 = \sqrt{x^T x}$.

DEF! A matrix norm is a real valued function $\norm{\cdot}\colon \RR^{m\times n} \to \RR$ with $3$ properties, namely ... it's positive unless zero, or $\norm{A}\geq 0$ and $\norm{A}= 0$ iff $A=0$; it scales, i.e., $\norm{\alpha A} = \abs{\alpha}\cdot \norm{A}$; and it respects the triangle inequality $\norm{A + B} \leq \norm{A}+\norm{B}$.

DEF! A matrix norm has the submultiplicative property iff ... $$\forall A \in \RR^{m\times n}\, \forall B \in \RR^{n\times p}\, \norm{AB}\leq\norm{A}\norm{B}.$$

Vector norms induce matrix norms; these are called *natural* matrix norms.

FACT! Some matrix norms guaranteed to have the submultiplicative property are ... those induced by $l_p$ vector norms.

EX! The matrix norm given by the max column sum of magnitudes is ... the $l_1$ matrix norm.

EX! The matrix norm given by the max row sum of magnitudes is ... the $l_\infty$ matrix norm.

EX! Turns out that the scalar $\max_i\{\sqrt{\lambda_i}: \lambda_i \text{ is an eigenvalue of } A^T A\}$ is given by ... $\norm{A}_2$, the spectral norm.

DEF! Given a vector norm, the induced matrix norm is ... $$\norm{A} = \sup_{x\neq 0} \frac{\norm{Ax}}{\norm{x}}.$$

## Polynomial approximation

To take intuition from [Wikipedia](https://en.wikipedia.org/wiki/Polynomial):

>  Polynomials can be constructed from constants and indeterminates using only addition and multiplication.

The implementation of said addition and multiplication, of course, should optimized according to the set from which these constants are chosen.[^mca]

[^mca]: R. Brent and P. Zimmermann, *[Modern Computer Arithmetic](https://members.loria.fr/PZimmermann/mca/mca-cup-0.5.9.pdf)*. Version 0.5.9. Retrieved July 17, 2018.

    > We shall see that many algorithms for polynomial arithmetic are similar  to  the  corresponding  algorithms  for  integer  arithmetic,  but simpler due to the lack of carries in polynomial arithmetic. Consider for example addition: the sum of two polynomials of degree $n$ always has degree at most $n$, whereas the sum of two $n$ -digit integers may have $n+1$ digits. Thus, we often describe algorithms for  polynomials  as  an  aid  to  understanding  the  corresponding algorithms for integers. (p. 1)

    >  A strong link exists between modular arithmetic and arithmetic on polynomials. One way of implementing finite fields $\mathbf{F}_q$ with $q = p^n$ elements is to work with polynomials in $\mathbf{F}_p[x]$, which are reduced modulo a monic irreducible polynomial $f(x)\in\mathbf{F}_p[x]$ of degree $n$. In this case, modular reduction happens both at the coefficient level (in $F_p$) and at the polynomial level (modulo $f(x)$). (p. 49)

We'll make concrete use of the [Weierstrass Approximation Theorem](https://en.wikipedia.org/wiki/Stone%E2%80%93Weierstrass_theorem) (only later generalized to $C(X)$, the ring of continuous functions on a compactum $X$ with the topology of uniform convergence, by [Stone](https://en.wikipedia.org/wiki/Marshall_Harvey_Stone)):

!THM (Weierstrass Approximation) Given a continuous function $f\colon [a,b] \to \RR$ for all $\varepsilon > 0$ ... there exists a polynomial $p \in \RR[x]$ such that for all $x \in [a,b]$ we have $\abs{f(x) - p(x)} < \varepsilon$.

For notation's sake, we also define a general [polynomial ring](https://en.wikipedia.org/wiki/Polynomial_ring).

!DEF (The polynomial ring $\mathbf{K}[X]$) Let $\mathbf{K}$ be a field. By the ring of polynomials in the indeterminate, $X$, written as $\mathbf{K}[X]$, we mean ... the set of all symbols $\sum_{i=1}^n a_i X^i$ where $n \in \NN$ and the coefficients $a_i$ are elements of the field $\mathbf{K}$.

Here's the application of polynomial approximation in numerical quadrature:

- I desire $\int_a^b f(x)\, dx$.
- I can bound $\abs{\int_a^b f(x)\, dx - \int_a^b p(x)\, dx} \leq \varepsilon(b-a)$.
- To obtain the desired precision, I ought to control $\varepsilon$.

The set of Taylor polynomials is an obvious candidate to approximate a differentiable function. Yet, looking at Taylor's theorem, we might not have a promising error bound our interval of integration.

!FACT (Taylor error bounds) Let $f(x)$ be defined on $[a,b]$ and suppose $f^{(n+1)}$ is (defined and) continuous on $[a,b]$. For any $x, x_0 \in [a,b]$ there exists $\xi(x) = \xi$ between $x$ and $x_0$ such that, where $p_n$ is the $n$th degree Taylor polynomial centered at $x_0$, the remainder $r = f - p_n$ is given ... $$r(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}.$$

For example, the Taylor series representation of the function $f(x) = \frac{1}{1+25x^2}$ only converges uniformly for $\abs{x}<0.2$. 

## Lagrange form

Consider $f \in C[a,b]$ (the set of continuous real-valued functions on the compact interval $[a,b]$), and let $x_0,\ldots,x_n$ be $n+1$ distinct points. Does there exist polynomial of least degree $p \in \RR[x]$ which *interpolates* $f$ at the given points? such that $f(x_i) = p(x_i)$ for all $i \in \{0,1,\ldots,n\}$? Is it unique?

The fundamental theorem of algebra guarantees uniqueness,^[The difference between any two least degree interpolating polynomials is the zero polynomial.] and Lagrange's construction demonstrates existence.

DEF! Having $n+1$ distinct points $x_i$ specified, the $n+1$ Lagrange polynomials $\ell_k$ are written as the product ... $$\ell_k(x) = \prod_{i\neq k} \frac{x-x_i}{x_k-x_i} \text{ for all } k \in \{0,1,\ldots,n\}.$$

It can be shown that the set of $n+1$ Lagrange polynomials spans $\mathcal{P}_n$---the vector space of polynomials of degree at most $n$ over the field $\RR$. We note the Lagrange polynomials form a basis for $\mathcal{P}_n$ since $\dim(\mathcal{P}_n) = n+1$.

Now for Lagrange's construction, which specifies the linear combination of basis vectors $\{\ell_k : k=0,1,\ldots,n\}$.

DEF! (Lagrange form) Let $f \in C[a,b]$, and specify $n+1$ distinct points $x_i$. The interpolating polynomial in Lagrange form is $p_n \in \mathcal{P}_n$ where ... $$p_n(x) = \sum_{k=0}^n f(x_k) \ell_k(x).$$

FACT! The degree of a Lagrange polynomial generated by $n+1$ points is ... $n$.

FACT! Evaluated at any of the $n+1$ generating points $x_i$, the Lagrange $k$th polynomial is equal to ... the Kroenecker delta $$\delta_{ik} = \begin{cases} 1 &\text{ if } i=k\\ 0 &\text{ else.} \end{cases}$$

The least degree interpolating polynomial we sought the existence of is $p_n$. Moreover, $p_n$ is a unique vector in $\mathcal{P}_n$ (though it may have different representations, which can be more or less computationally efficient, by change of bases), so existence proof for interpolating polynomials (generated by a finite number of distinct points) is finished.

Coming up:

- What is the computational cost to evaluate $p_n(x)$ at $x\neq x_i$?
- How large is the error $\abs{f(x) - p_n(x)}$ at $x \neq x_i$?
- Can we guarantee the error bound shrinks as we increment the number of generating points $x_i$?
- What is the computational complexity of an algorithm to generate the Lagrange form of the interpolating polynomial?
- Can we reduce computational complexity by iteratively generating more accurate approximations to a given function? that is, by using successively higher degree interpolating polynomials? 
- What criteria do we have to choose higher-degree polynomials (from an otherwise underdetermined solution space)?

## Newton form

An example first. Consider the linear interpolant (degree $n=1$) between $(x_0,f(x_0))$ and $(x_1,f(x_1))$.

\begin{align} p_1(x) &= f(x_1)\ell_1(x)+f(x_1)\ell_1(x) &\\
&=f(x_0)\frac{x-x_1}{x_0-x_1} + f(x_1)\frac{x-x_0}{x_1-x_0}& \text{(Lagrange form)}\\
&=f(x_0) + f(x_1)\frac{f(x_1)-f(x_0)}{x_1-x_0}& \text{(Newton form)}
\end{align}

Newton's form allows us to compute $p_n$ from $p_{n-1}$ recursively. That is, we define $p_n$ with the same $n-1$ basis vectors and $n-1$ coordinates as $p_{n-1}$, but add a basis vector that's $0$ at all points $x_i$ with $i < n$. 

Namely, $$p_n(x) = p_{n-1}(x)+a_n\prod_{i < n} (x-x_i)$$ with $$a_n = \left(f(x_n) - p_{n-1}(x_n)\right)\left(\prod_{i < n} (x_n-x_i)\right)^{-1}.$$

In practice we express the coordinate $a_n$ in recursive *divided differences*, i.e., $$a_n = f[x_0,\ldots,x_n] = \frac{f[x_1, \ldots, x_n] - f[x_0, \ldots, x_{n-1}]}{x_n-x_0}$$
where the identification $f[x] = f(x)$ for all $x$ is the base for recursion.

The Newton form of the interpolating polynomial is
$$p_n(x) = a_0 + a_1(x-x_0) + \cdots + a_n(x-x_0)\cdots(x-x_{n-1})$$
or, from another view,
$$p_n(x) =  a_0 + (x-x_0)\bigg(a_1 + (x-x_1)\Big(a_2+\cdots + a_n(x-x_{n-1})\cdots\Big)\bigg).$$

Redistributing the parentheses by nesting them, we can evaluate $p_n(x)$ with $O(n)$ operations, namely, $n$ multiplications and $n$ additions.

## Matrix interpretation

For $n+1$ generating points $(x_i,f(x_i))$, there is a unique interpolating polynomial $p_n$ of degree $n$.

But $p_n$ is just point in the vector space $\mathcal{P}_n$, so we should try to express the constraint that $p_n(x_i) = f(x_i)$ for all $i \in \{0,1,\ldots,n\}$ as $n+1$ linear equations to determine the coordinates of $p_n$. 

We are required to choose a basis for $\mathcal{P}_n$, and we've thus far seen three:

- the standard basis $\{1,x,x^2,\ldots, x^n\}$

    - yields a power series approximation[^taylor] to $f$

- the Lagrange polynomials $\{\ell_0, \ell_1, \ldots, \ell_n\}$

    - produces the Lagrange form of the interpolating polynomial

- the basis of the Newton form $\{1, (x-x_0), \ldots, (x-x_0)\cdots(x-x_n)\}$

    - gives rise to the Newton/nested form

[^taylor]: Indeed, the standard basis *is a minimal spanning set* for $\mathcal{P}_n$, so the divergence of Taylor series representation cannot be blamed on having the wrong vectors to create $p_n$. Instead, we find that the Taylor series representation implements a differential (rather than linear algebraic) algorithm for reducing a highly ill-conditioned system, which, in some cases, as when the function to be interpolated is analytic, proceeds, but fails for merely continuous functions.

The constraint as a matrix equation (in any basis) is
$$A \begin{pmatrix}a_0\\ \vdots\\ a_n\end{pmatrix} = \begin{pmatrix}f(x_0)\\ \vdots\\ f(x_n)\end{pmatrix}.$$

For the standard basis, $A$ is the Vandermode matrix, which tends to be ill-conditioned.

For the Lagrange polynomial basis, we have simply^[It's computing the basis that's expensive!] $A = I$.

For the basis of the Newton form, $A$ is a lower triangular matrix. Solving $A \vec{a} = \vec{f}$ for the coordinates $\vec{a}$ requires $n^2/2$ operations---the same required to compute with a divided difference table. In practice, we use divided differences to avoid storing the matrix elements in memory.

## Error bounds

THEOREM! Let $f \in C^{n+1}[a,b]$, the $x_i$ be $n+1$ distinct points in $[a,b]$, and suppose $p_n$ is a polynomial of degree at most $n$ that interpolates $f$ at the $x_i$. Given $x \in [a,b]$, there exists a point $\xi \in (a,b)$ such that ... $$f(x) = p_n(x) + \frac{f^{(n+1)}(\xi)}{(n+1)!}\prod_{\forall i}(x-x_i).$$
