---
title: Differential Geometry 1
author: Colton Grainger
date: 2018-12-01
bibliography: /home/colton/coltongrainger.bib
---

\setcounter{section}{-1}


## MATH 6230 Syllabus

Instructor: [Prof. Jeanne Clelland](http://math.colorado.edu/~jnc/)

Git repo: <http://github.com/coltongrainger/fy19diffgeo1>. 

Here are the changes I hope to make in contrast with my [topology 1](top1) notes.

- More: open questions, metacognitive dialogue
- Less: mathjax, math macros, definitions

### Grading

assessment | weight
--- | ---
take-home midterm | 0.25
final exam | 0.25
homework | 0.5

Collaboration was encouraged.

### Textbooks

Lectures will follow the canonical course text.

- John Lee's *Introduction to Smooth Manifolds* [@Lee03]

These are for supplement.

- Serge Lang's *Fundamentals of Differential Geometry* [@Lan99]
- Wilhelm Klingenberg's *A Course in Differential Geometry* [@Kli78]
- John Milnor's *Topology from the Differentiable Viewpoint* [@Mil65]
- Michael Spivak's *Calculus on Manifolds* [@Spi65]

There are for review.

- Folland's *Advanced Calculus* [@Fol02]
- Hubbard's *Unified Approach* [@HH15]

### Prerequisites

Here's a long list from John M. Lee's undergraduate and graduate courses (1.5 years of work!):

From the [Math 442](https://sites.math.washington.edu/~lee/Courses/442-2013/syllabus.pdf) syllabus:

> - Vector calculus: partial derivatives, the chain rule, dot products, cross products, tangent lines, tangent planes, line integrals, surface integrals, gradients, vector fields, the divergence theorem.
> - Linear algebra: vector spaces, bases and dimension, linear maps and their representation by matrices, rank of a matrix, determinants, matrix algebra, eigenvectors and eigenvalues. 
> - Analysis in several variables: functions of several variables and their differentials; the inverse and implicit function theorems; the change of variables theorem for double and triple integrals.
> - Topology: open and closed sets, boundaries, limit points, closures, continuous maps, homeomorphisms, connected sets, compact sets. 

From the [Math 554](https://sites.math.washington.edu/~lee/Courses/544-2006/syllabus.pdf) syllabus, for a study of *topological manifolds*:

> - Set Theory : Operations on sets, functions, equivalence and order relations, number systems and cardinality, the axiom of choice. References : Principles of Mathematical Analysis by Rudin, Chapter 1; Mathematical Analysis by Apostol, Chapters 1 and 2; Appendix to [ITM]. 
> - Analysis : Metric spaces; convergence and continuity; open and closed sets; interior, exterior, and boundary; compactness. Reference : Principles of Mathematical Analysis by Rudin, Chapters 2,3,4; Mathematical Analysis by Apostol, Chapters 3 and 4; Appendix to [ITM]. 
> - Algebra : Elementary group theory, homomorphisms, isomorphisms, subgroups, normal sub- groups, permutation groups, cyclic groups, cosets, quotient groups. Reference : Abstract Algebra: An Introduction by Hungerford, Chapter 7; Abstract Algebra by Herstein, Chapters 1–3; Appendix to [ITM].

From, again, MATH 554, for a study of *smooth manifolds*:

> - Topology : All the material covered in Math 544. Reference : [ITM].
> - Linear algebra : Abstract vector spaces, subspaces, bases, dimension, matrices, determinants, change of basis formulas, linear maps, kernel and image, norms and inner products, orthonormal bases. Reference : any rigorous linear algebra text, such as Linear Algebra by Friedberg, Insel, and Spence; Appendix to [ISM].
> - Multivariable  calculus : Partial derivatives; the total derivative as a linear approximation; Taylor’s formula in several variables; multiple integrals and the change of variables formula; gradient, divergence, and curl; the theorems of Green, Gauss, and Stokes; uniform convergence. References : Basic  Multivariable  Calculus by Marsden, Tromba, and Weinstein; Principles of  Mathematical  Analysis by Rudin, Chapters 5,6,7; Mathematical  Analysis by Apostol, Chapters 12–14; Appendix to [ISM].
> - Differential  equations : Basic facts about existence and uniqueness of solutions to ODEs; elementary techniques for solving first-order equations and systems at the level of Math 307 and 309. Reference : Elementary Differential Equations and Boundary Value Problems by Boyce and DiPrima.

### Prelim Exam Outline

Here's an outline for the geometry half of CU's topology/geometry preliminary exam. See also [the topology half](top1#prelim-exam-syllabus).

- Smooth manifolds
    - implicit function theorem and regular values of functions
    - coordinate charts on manifolds
    - topological and $C^\infty$ manifolds
    - examples of manifolds: Lie groups
    - submanifolds defined via implicit functions
    - classification of two-dimensional compact manifolds
- Vector fields and tangent bundle
    - differential operators
        - tangent spaces 
        - vectors
    - tangent bundle over a manifold 
    - vector fields on manifolds 
        - local flows
        - straightening
        - the Lie bracket (commutator and derivative)
- Differential forms and tensor fields
    - dual spaces and multilinear operators
    - $k$-forms on a vector space and wedge products
    - $k$-forms and other tensor fields on a manifold
    - change-of-coordinate formulas for vector fields and $k$-forms
    - $d$ operator from $k$-forms to $(k + 1)$-forms
    - $k$-chains
    - Stokes’ theorem on manifolds.
- Riemannian manifolds
    - metrics on manifolds
    - covariant derivative
    - parallel transport
    - orientability
    - curvature
        - tensor
        - sectional curvature
    - baby Chern-Weil
    - the geodesic equation
    - Levi Cevita connection
    - exponential map
    - Jacobi fields
    - arc length variation formulas
    - fundamental equations for metric immersions and submersions
    - space forms
    - Hopf-Rinow
    - Hadamard-Cartan
    - Bonnet-Myers 
        - Gauss-Bonnet 
        - Bochner technique
- Exotic geometric structures
    - Kahler manifolds
    - symplectic manifolds
    - contact manifolds

## Week 1

\providecommand{\ZZ}{\mathbf{Z}}
\providecommand{\RR}{\mathbf{R}}
\providecommand{\CC}{\mathbf{C}}
\providecommand{\FF}{\mathbf{F}}
\providecommand{\sM}{\mathsf{M}}
\providecommand{\abs}[1]{\left\lvert #1 \right\rvert}
\providecommand{\norm}[1]{\left\lVert #1 \rVert\right}

For the first lecture, there are about 20 people in class, at noon-time in the Engineering Center.

Clelland's goal is to give us practice working with tensors and differential forms.

- As applications, we'll study vector fields & vector bundles.
- Will we discuss [connections](https://en.wikipedia.org/wiki/Connection_(mathematics))? Perhaps not by May, but it's open ended how we progress through Lee.

### Review of linear algebra

IDEA! (Basis) Let $V$ be a real vector space $V$ of dimension $n$. Any vector in $V$ can be expressed as a linear combination of the vectors $\{e_1, \ldots, e_n\}$ iff ... that set is a basis for $V$.

In Einstein summation notation, we have $v = a^i e_i := \sum_i a^i e_i$ for $n$ real coefficients $a^i$.

Q! Say $\tilde{e}_1, \ldots \tilde{e}_n$ is another basis for the vector space $V$. How can we express $v = a^i {e}_i$ relative to the $\tilde{e}_i$? Say $R \in GL_n(\RR)$ and $[\tilde{e}_1 \ldots \tilde{e}_n] = [{e}_1 \ldots {e}_n] R$. Then $v$ is ... $$[\tilde{e}_1 \ldots \tilde{e}_n] R^{-1} \begin{bmatrix} a^1 \\ \vdots \\ a^n\end{bmatrix}.$$

A! The coefficients $\tilde{a}^i$ of $v = a^i e_i$ relative to the new basis $\tilde{e}_i$ (obtained from the right action of $R \in GL_n(\RR)$ sending each $e_i$ to $\tilde{e}_i$) are given by ... $$[\tilde{a}^i] = R^{-1}[a^i].$$

Roughly speaking, a vector exhibits a rank $1$ tensor. It's rank $1$ because when we express a vector in terms of a basis, each component is of index $1$. Higher ranked tensors require us to make explicit how components are transformed when one changes bases for the space.

DEF! (Naive) A covariant $k$-tensors on the finite dimensional real vector space $V$ is ... a real-valued multilinear function of $k$ elements of $V$: $$\alpha \colon \underbrace{ V \times \ldots \times V }_\text{$k$ copies} \to \RR.$$

EX! The (row vector of) basis vectors $$e = [e_1 | \ldots | e_n]$$ and the (column vector of) coefficients $$a = \begin{bmatrix} a^1 \\ \vdots \\ a^n\end{bmatrix}$$ are basis-dependent, but the product ... $v = ea$ is independent of basis.

*Because* each $v \in V$ is independent of basis, we are *forced* to new coefficients $\tilde{a}^i$ when changing bases to $\tilde{e}_i$ from $e_i$. 

NOTE! If the row vector of basis vectors $[e_i]$ (with lower indices) is right-acted on by an invertible linear map $R$, how are the coefficients of $v = [e_i][a^i]$ transformed? ... The column vector of coefficients $[a^i]$ (with upper indices) are left-acted on by the matrix $R^{-1}$.

Now let $V$ and $W$ be real vector spaces with respective bases $[e_1 \ldots e_m]$ and $[f_1 \ldots f_n]$. Let $T \colon V \to W$ be a linear map. There's some $A_T \in \sM_{n \times m}(\RR)$ such that for all $v \in V$, $A_T v = T(v) =: Tv$. What do we really mean by this?

Given a vector $v \in V$, we usually represent:

- $v$ as a column vector $$ a = [a^i] = \begin{bmatrix} a^1 \\ \vdots \\ a^m\end{bmatrix},$$ to abbreviate $v = [e_1 \ldots e_m] a$.
- $Tv = w$ as the matrix product $b = A_T a$, i.e., $$\begin{bmatrix} b^1 \\ \vdots \\ b^n\end{bmatrix} = \begin{bmatrix} c_1^1 &\ldots & c_m^1\\ \vdots & & \vdots\\ c_1^m & \ldots & c_n^m\end{bmatrix}\begin{bmatrix}a^1 \\ \vdots \\ a^m\end{bmatrix} =: [c_i^j a^i]$$ summing over $1 \le i \le n$, with columns indexed by $1 \le j \le m$.

To then write out the image of $v$ under $T$ as $w$ in full glory, 
\begin{align*}
w &= [f_1 \ldots f_n]\begin{bmatrix} b^1 \\ \vdots \\ b^n\end{bmatrix}\\
  &= T\left([e_1 \ldots e_m]\begin{bmatrix}a^1 \\\vdots\\ a^m\end{bmatrix}\right).
\end{align*}

Q! Suppose we change bases for $V$ and $W$ by taking transition matrices $R \in GL_n(\RR)$ and $S \in GL_m(\RR)$ so that \begin{align*} { [\tilde{e}_j] }_\text{new in $V$}  &= [e_j]R\\ { [\tilde{f}_i] }_\text{new in $W$}  &= [f_i]S. \end{align*} How is the matrix $A_T$ associated to $V \xrightarrow{T} W$ transformed? ... $$\tilde{A}_T = S^{-1} A_T R.$$

To give "intuition" as to why a linear transformation should be a rank $2$ tensor: 

- the upper index $i$ with range $1 \le i \le n$ corresponds to $W$, while
- the lower index $j$ with range $1 \le j \le m$ corresponds to $V$.

### Einstein Notation

From comments to a [“frustrating experience about differential geometry”](https://math.stackexchange.com/questions/1011835/frustrating-experience-about-differential-geometry) on Mathematics Stack Exchange. 

> Algebra is the study of objects invariance under isomorphism, while DG is the study of objects invariance under change of notations.

From top2, to justify suppressing indices for boundary maps, face maps, $p$-th degree simplices:

> You should learn to be "flexible" with your notation. (Or else you'll get headaches.) I'm dropping the $p$ in $\partial_p$. It's there, but you'll need to get it from context.

I asked Clelland what other disciplines used Einstein summation notation. 

- Mostly theoretical physics. Good enough. 
- It's useful to have shorthand in case one toggle between explicit constructions and abstract universal properties.
  - E.g., to demonstrate some property is independent of basis, one should try to give a coordinate-free proof.
  - Though having bases and coordinates is useful for computation.

From <https://en.wikipedia.org/wiki/Einstein_notation>.

> - upper indices represent components of contravariant vectors (vectors),
> - lower indices represent components of covariant vectors (covectors).

To borrow from <http://mathworld.wolfram.com/EinsteinSummation>

RULE! (Weisstein) Repeated indices are ... implicitly summed over.

RULE! (Weisstein) Each index can appear at most ... twice in any term.

RULE! (Weisstein) Each term must contain ... identical non-repeated indices. 

RULE! (Clelland) If the same index appears twice, one up and one down, then ... one sums along the range of that index.

EX! Given a differentiable function $f \colon \RR^n \to \RR$ and $y \colon \RR^m \to \RR^n$, the term $\frac{\partial f}{\partial x^i}$ in the Jacobian representing the total derivative of $f$ (in Einstein summation notation) is ... $\frac{\partial f}{\partial y^j} \frac{\partial y^j}{\partial x^i}$, where an up index in the denominator counts as a down index in the numerator.

I'd like to know more about "raising and lowering indices" given, e.g., a metric tensor. See also:

- <https://en.wikipedia.org/wiki/Metric_tensor>
- <https://en.wikipedia.org/wiki/Raising_and_lowering_indices>

### Review of differential calculus

Wednesday's lecture assumed **finite dimensional normed vector spaces**, presumably over $\RR$ or $\CC$. I'll gloss what we covered in $\RR^n$ as a specific setting.

- We defined the total derivative, variously denoted $DF(a)$, $DF\vert_a$, $dF_a$ (no! this is too close to $\partial_a F$), or $(F_*)_a$.
- We wrote out the Jacobian.
- We set up the chain rule for $U \xrightarrow{F} V \xrightarrow{G} X$.
  - "The derivative of the composite is the composite of the derivative."
- We further defined:
  - partial derivatives as entries in the Jacobian
  - classes of continuously differentiable functions by way of the existence of partials
  - class $C^k$ diffeomorphisms, also local diffeomorphisms

We stated the inverse function theorem.

In Friday's lecture we stated the implicit function theorem.

TODO reference proofs

### Banach spaces and the smooth chain rule

> As before, we prefer to work in a coordinate-free representation. In other words, we develop the differential calculus for maps between Banach spaces. This representation is conceptually simple and actually makes many expressions look much simpler. The classical formulas for the derivatives in the usual coordinate representation follow easily from the general results using the product structure of finite-dimensional Euclidean spaces. [@AE08, ch. VII]

**Road map.** We aim to consider finite dimensional real vector spaces as Banach spaces. We need to:

- Define the Fréchet derivative in Banach spaces.^[Idea from <https://math.stackexchange.com/questions/1851553>, <https://math.stackexchange.com/questions/2826748>.]
- Prove a composition of $p$-times continuously differentiable maps is again $C^p$.
- Define partial derivatives in the special case that the codomain is a finite dimensional vector space. 
- Argue the Jacobian matrix representing the derivative function with respect to the standard bases between finite dimensional real vector spaces has entries given by $$\frac{\partial(G^i \circ F)}{\partial x^j}(x) = \sum_{k = 1}^m \frac{\partial G^i}{\partial y^k}(F(x))\frac{\partial F^k}{\partial x^j}(x).$$

**Definitions.** (Paraphrased from Lang [@Lan99, ch. I]) A *Banach space* is a topological vector space that's complete and whose topology can be defined by a norm. The set of *continuous linear maps* from one Banach space $E$ to another $F$ will be denoted by $L(E,F)$, whereas the set of *continuous $r$-multilinear* maps $$\psi \colon E \times \cdots \times E \to F$$ of $E$ into $F$ will be denoted by $L^r(E, F)$. We put a topology on $L^n(E,F)$ for all $n \ge 0$ by declaring $L^0(E, F) := F$ and defining the norm of an $r$-multilinear map $\psi \in L^r(E, F)$ to be $$\sup\{K : \abs{\psi(x^1, \ldots, x^r)} \le K \abs{x^1} \cdots \abs{x^r}\}.$$ The $L^n(E,F)$ are thus Banach spaces.

**Proposition.** If $E_1, \ldots, E_r$ are Banach spaces, then the canonical map $L\big(E_1, L(E_2, \ldots, L(E_r, F), \ldots )\big)$ to $L^r(E_1, \ldots, E_r, F)$ is a norm-preserving toplinear isomorphism. 

**Definition.** Say $E$ and $F$ are Banach spaces, $U \subset E$ is open and $a \in U$. A map $f \colon U \to F$ is said to be *differentiable at $a$* if there's a linear approximation $\lambda_a \in L(E,F)$ such that $$f(a + v) = f(a) + \lambda_a(v) + r(v) \quad \text{ where } \frac{\abs{r(v)}}{\abs{v}} \to 0 \text{ as } v \to 0.$$

**Remark.** $\lambda_a$ is uniquely determined by $f$ and $a$. We say $\lambda_a$ is the *derivative of $f$ at $a$* (also called the *total* or *Fréchet* derivative of $f$ at $a$). We denote $\lambda_a$ by $\partial f(a)$, $Df(a)$, etc.

If $f$ is differentiable at each $a \in U$, the we have a map $$Df : U \to L(E, F), \quad a \mapsto Df(a),$$ which we say is *the derivative function of $f$* (known also as the *Fréchet*, or *total* derivative of $f$).

**Proposition.** (Chain rule) Say $E$, $F$, and $G$ are Banach spaces and we've maps defined on open subsets $$U \subset E \xrightarrow{f} V \subset F \xrightarrow{g} G.$$ If $f$ and $g$ are differentiable at $a \in U$ and $f(a) \in V$ (resp.), then $g \circ f$ is differentiable at $a$ with derivative $$\underbrace{D(g \circ f)(a)}_\text{in $L(E, G)$} = \underbrace{Dg(f(a))}_\text{in $L(F,G)$} \underbrace{Df(a)}_\text{in $L(E, F)$}.$$

*Proof.* (Adapted from Folland [@Fol02, ch. 2.6]) Let $b = f(a)$. By definition of differentiability at a point, both 
\begin{align*}
g(b + h) & = g(b) + Dg(b)h + E_1(h), &\frac{\abs{E_1(h)}}{\abs{h}} \to 0 \text{ as $h \to 0$}\\
f(a + k) & = f(a) + Df(a)k + E_2(k), &\frac{\abs{E_2(k)}}{\abs{k}} \to 0 \text{ as $k \to 0$}.
\end{align*}

Let $h := f(a+k) - f(a)$, then so too $h = Df(a)k + E_2(k)$. Consider 
\begin{align*}
(g \circ f)(a + k) &= g(b + h) = g(b) + Dg(b)h + E_1(h)\\
    &= g(f(a)) + Dg(b)[Df(a)k + E_2(k)] + E_1(h)\\
    &= (g \circ f)(a) + Dg(b)Df(a)k + E_3(k),\\
\end{align*}
where $E_3(k) = Dg(b)E_2(k) + E_1(h)$. We claim $E_3(k)/\abs{k} \to 0$ as $k \to 0$, in which case $$(g \circ f)(a +k)  = (g \circ f)(a) + Dg(b)Df(a)k + \text{ remainder }$$ confirms that the linear map $Dg(b)Df(a)$ is the total derivative of $g \circ f$ at $a$. For the claim, consider each term in the error summand. By our definition of a norm for linear maps, $$\frac{\abs{Dg(b)E_2(k)}}{\abs{k}} \le \abs{Dg(b)}\frac{\abs{E_2(k)}}{\abs{k}} \to 0, \quad \text{ as $k \to 0$.}$$
This also implies when $k$ is a vector close to $0$, then $\abs{E_2(k)} \le \abs{k}$, hence by the triangle inequality and our definition of a norm for linear maps $$\abs{h} = \abs{Df(a)k + E_2(k)} \le \underbrace{ (\abs{Df(a)} + 1)}_\text{constant}\abs{k}.$$ Since $\abs{k}$ is bounded below by a constant multiple of $\abs{k}$, as $k \to 0$, it's true also that $$\frac{\abs{ E_1(h) }}{\abs{k}} \le \frac{\abs{ E_1(h) }}{\text{const.}\cdot\abs{h}} \to 0.$$ 

**Definitions.** (Directional and partial derivatives) Consider a map $f \colon U \to F$ from open $U$ in $E$, choose a base point $a \in U$, and a vector $v \in E \setminus \{0\}$. Because $U$ is open, there's an $\epsilon > 0$ such that $a +tv \in U$ for all $t \in (-\epsilon, \epsilon)$. We dub the *directional derivative of $f$ at $a$ in the $v$ direction to be $$\partial_v f(a) := \frac{d}{dt} f(a + tv)\lvert_{t=0} = \lim_{t \to 0 } \frac{f(a + tv) - f(a)}{t}.$$

To quote [@AE08, pg. 153]:

> If $E = \RR^n$, the derivatives in the direction of the coordinate axes are particularly important, for practical and historical reasons. ... We thus write $\partial_k$ or $\partial/\partial x^k$ for the derivatives in the direction of the standard basis vectors $e_k$ for $k = 1, \ldots,n$.

**Theorems for Euclidean space.** [@AE08, no. VII.2.8]

i. Suppose $E = \RR^n$ and $f \colon U \to F$ is differentiable at $a \in U$. Then $$Df(a) h = \sum_{k =1}^n \partial_k f(a)h^k\quad \text{ for $h = (h^1, \ldots, h^k) \in \RR^n.$}$$

ii. Suppose $E$ is a Banach space and $f = (f^1, \ldots, f^m) \colon U \to \FF^m$ (an $m$ dimensional $\FF$-vector space). The $f$ is differentiable at $a$ if and only if all the coordinate functions $f^j$ are differentiable at $a$. Then $$Df(a) = (Df^1(a), \ldots, Df^m(a)).$$

iii. Suppose $U$ is open in $\RR^n$ and $f = (f^1, \ldots, f^m) \colon U \to \RR^m$ is differentiable at $a$. The matrix representation (in the standard basis) of the derivative of $f$ is the Jacobi matrix of $f$: $$[Df(a)] = [\partial_k f^j(a)].$$

**Definition.** (Continuously differentiable) Let $U$ be open in a Banach space $E$ and say $f \colon U \to F$ is differentiable. When the derivative function $Df \colon U \to L(E, F)$ is continuous, we say that $f$ is *continuously differentiable*, or of *class $C^1$*. To define class $C^p$, we need to inductively define higher total derivatives. The $p$th derivative of $f$ is $D(D^{p-1}f)$, which is a map $$D^p f \colon U \to L\big(E, L(E, \ldots, L(E,F), \ldots )\big) \cong L^p(E, F) \quad \text{by isometry.}$$ A maps is said to be of *class $C^p$* if its $k$th derivative exists $1 \le k \le p$.

**Smooth Chain Rule (Base Case).** If $U \xrightarrow{f} V \xrightarrow{g} V \xrightarrow G$ are maps of class $C^1$ between open sets of Banach spaces $E, F$, and $G$, then the composite $g \circ f$ is of class $C^1$. 

\pf Consider a point $a \in U$. By the chain rule, defining $\phi (a) = (Dg(f(a)), Df(a))$ and $\psi(A, B) = AB$ (as composition of linear maps), the following diagram commutes.

<a href="http://presheaf.com/?d=d6011306w2j6p5x6n5571404173356x55"><img src="http://presheaf.com/cache/d6011306w2j6p5x6n5571404173356x55.png" title="click to go to presheaf.com for editing"/></a>

Since $\phi$ is continuous in each coordinate, $\phi$ is a continuous. At the same time, $\psi$ is just the product of linear functions $(A,B) \mapsto AB$, hence is continuous. (Idea from <https://math.stackexchange.com/questions/2826748>.) Thence $g\circ f$ is of class $C^1$.

**Lemma.** Any *continuous* multilinear map $\psi \in L^r(E, F)$ is infinitely differentiable. 

\pf Let $(a^1, \ldots, a^r)$ be a basepoint and $(h^1, \ldots, h^r)$ be a step vector in $E \times \cdots \times E$. Observe $\psi(a^1 + h^1 , \ldots, a^r + h^r)$ can be written as $2^n$ terms $$\psi(a^1, \ldots, a^r) + \sum_{i=1}^r \psi(a^1, \ldots, h^i, \ldots, a^r) + \sum \text{ terms with at least two coordinates $h_i, h_j$.}$$ Assuming $\psi$ is continuous, the last $2^r - (r + 1)$ terms converge to $0_F$ superlinearly as $(h^1, \ldots, h^r) \to 0$. Note that in whatever norm we choose for $E \times \cdots \times E$, that norm is equivalent to, say, the max norm, so that 
$$\frac{\abs{\psi(a^1, \ldots, h^i, \ldots, h^j, \ldots, a^r)}}{(\abs{h^1, \ldots, h^r)}} \le \frac{\abs{\psi} \cdot \text{const.} \cdot \abs{h^i}\abs{h^j}}{\abs{h^\text{max}}} \to 0.$$ 
So we have a continuous $(r-1)$-multilinear map $$D\psi(a) \colon h \mapsto \sum_{i=1}^r \psi(a^1, \ldots, h^i, \ldots, a^r),$$ which implies that the map $D\psi: a \mapsto D\psi(a)$ is $r$-multilinear and continuous as well. Given continuous bilinear maps as a base case, by induction on $r$ we've show all continuous $r$-multilinear maps are infinitely differentiable. 

**Smooth Chain Rule (Inductive Step).** If $U \xrightarrow{f} V \xrightarrow{g} V \xrightarrow G$ are maps of class $C^p$ between open sets of Banach spaces $E, F$, and $G$, then the composite $g \circ f$ is of class $C^p$. 

\pf Let our inductive hypothesis be that the composite of any two compatible $C^{p-1}$ maps on Banach spaces is also $C^{p-1}$. Assume now that $f \in C^p(U, F)$ and $g \in C^p(V,G)$. Say a point $a \in U$. By the chain rule, defining as before $\phi (a) = (Dg(f(a)), Df(a))$ and $\psi(A, B) = AB$, TFDC.

<a href="http://presheaf.com/?d=d6011306w2j6p5x6n5571404173356x55"><img src="http://presheaf.com/cache/d6011306w2j6p5x6n5571404173356x55.png" title="click to go to presheaf.com for editing"/></a>

By assumption, the map $a \mapsto Df(a)$ is in $C^{p-1}(U, L(E,F))$ and $b \mapsto Dg(b)$ is in $C^{p-1}(V, L(F, G))$. By inductive hypotheses, the composition $a \mapsto f(a) \mapsto Dg(f(a))$ of $C^{p-1}$ maps is in $C^{p-1}(U, L(E,G))$. By its coordinates $\phi$ is in $C^{p-1}(U, L(E, F) \times L(F, G))$. By lemma, the continuous bilinear map $\psi$ is in $C^\infty(L(E, F) \times L(F, G), L(E,G))$. By the inductive hypothesis, then $\psi \circ \phi$ is in $C^{p-1}(U, L(E,G))$. so $D(g \circ g)$ is of class $C^{p-1}$, and we conclude $g \circ f$ is of class $C^p$. 

### Topological manifolds

We'll give properties of topological manifolds, then add structure until we've a sufficiently interesting category of "smooth manifolds" with smooth maps as morphisms.
