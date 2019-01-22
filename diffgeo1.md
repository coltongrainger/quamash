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
\providecommand{\sM}{\mathsf{M}}

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
- We stated the inverse function theorem.

TODO setup the total derivative in Banach spaces. (see notes for 2019-01-23).

TODO reference proofs for the inverse function theorem.

In Friday's lecture we stated the implicit function theorem.

TODO reference a proof for the implicit function theorem.

### Topological manifolds

We'll give properties of topological manifolds, then add structure until we've a sufficiently interesting category of "smooth manifolds" with smooth maps as morphisms.
