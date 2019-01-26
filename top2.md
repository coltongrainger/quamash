---
title: Topology 2
author: Colton Grainger
date: 2019-01-13
nonumbering: true
---

\providecommand{\RR}{\mathbf{R}}
\providecommand{\ZZ}{\mathbf{Z}}

\setcounter{section}{-1}

## MATH 6220 Syllabus

Instructor: [Dr. Agnès Beaudry](https://sites.google.com/view/agnesbeaudry)

Website: <https://sites.google.com/view/agnesbeaudry/teaching/spring-2019/math-6220>

Git Repo: <http://github.com/coltongrainger/fy19alg2>. 

> Continuation of [MATH 6210](top1). Topics covered will be homology, cohomology and some applications. 

### Prelim exam topics

- singular homology
- the Eilenberg-Steenrod axioms
- homology group of spheres
- the degree of a map between spheres
- homology calculations via CW complexes
- proof of homotopy invariance
- proof of excision
- universal coefficient 
- Kunneth Theorem

### Textbooks

- Topology and Geometry, Glen E. Bredon [@Bre93]
- Algebraic Topology, A. Hatcher [@Hat02]
- A Concise Course in Algebraic Topology, J. Peter May [@May99]

### Problem sets

From the [syllabus](https://drive.google.com/file/d/1bPOnqftRnfLxF4UrC44a1NZQMoZHE0tF/view):

> Problems sets will be posted to a [restricted dropbox] and discussed in class during a problem session, which will be approximately every two weeks. We will cover as many problems as we can during problem sessions. For a problem: 
> 
> - One student will be chosen to present the solution in class and lead the discussion on that problem.
> - A different student will be chosen to write-up the solution (typeset using LATEX). Solutions (.tex and .pdf files) are due via email by 1 pm the day of the class following the problem session.
>
> Tentative dates for the problem sessions: Jan 30, Feb 13, Feb 27, Mar 13, Apr 3, Apr 17, and possibly May 1.

### Grading

With emphasis on participation.

measure | weigh
--- | ---
presentations | 40%
write-ups | 30%
participation | 10%
final exam | 20%

### About these notes

I have tried (and failed) to talk myself out of keeping notes:

- I have no comparative advantage to narrate the development of homology/cohomology.
    - For example, Dr. Beaudry is live-TeXing her lecture notes, and [extensive references](https://math.stackexchange.com/a/1560607/469856) for algebraic topology notes are already listed on stackexchange. 

- When considering Philip Guo's [heuristic](http://pgbovine.net/writings.htm) when deciding what to write    

    > Will at least 100 people care about this topic three years from now?

    - I suspect the answer is yes, in general.
    - It's unlikely, however, that at least 100 people will care about my perspective.

- My preferred markup language is pandoc markdown, rendered here with MathJax, which has [limited support](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) for [commutative diagrams](http://www.jmilne.org/not/Mamscd.pdf). 
    - Just to render diagonal arrows, I'll have to port images from <http://presheaf.com/>.

However, in juxtaposed posts,

- <http://www.aaronsw.com/weblog/greatlectures>
- <http://www.aaronsw.com/weblog/awfullectures>

Aaron Schwartz via Tufte reminds us "to always ask about the information density of a method of communication". Won't these notes be sparse on content? Well, sure, but some communication owes its efficacy to "emotional density". So Schwartz' second essay wins out, and I'll bother anyways to record how I think and feel about the curriculum.

## Week 1

### Pre-requisites 

It's good to have seen

- point-set topology up to the Baire category theorem
- the statement of Seifert van-Kampen
- hopefully, category theory
- group actions on covering spaces
- informally, singular homology.

### Introduction

Homology and cohomology theory, as with homotopy theory, associate homeomorphism-invariant algebraic structures to topological spaces. We have functors:

- $\pi_0 \colon \mathsf{Top} \to \mathsf{Set}$ 
    - where $\pi_0(X)$ is the set of path connected components of the space $X$
    - easy enough to compute on manifolds
    - hard on fractals, e.g., Sierpiński and Apollonian gaskets
        - throughout the Fall, using his K-homology expertise, Alex was coloring our chalkboard with different recursions trying to set up a dynamical system on the Sierpiński gasket
        - see <https://arxiv.org/abs/1002.3081>

- $\pi_1 \colon \mathsf{Top}_* \to \mathsf{Grp}$
    - where $\pi_1(X, x)$ is the group of loops $\mathsf{Map}_*(S^1, X) / \cong_{\text{homotopy}}$ under concatenation, modulo base-point respecting homotopy.
    - one covers the space with appropriately intersecting open sets and applies SVK

- $\pi_n \colon  \mathsf{Top}_* \to \mathsf{Ab}$
    - no SVK for higher homotopy groups
    - TODO: If $n > 1$, then the group $\pi_n(X, x)$ of images of $n$-spheres modulo homotopy is *abelian*.

- $H_n \colon \mathsf{Top} \to \mathsf{Ab}$
    - "homology" groups for $n \in \ZZ_{\ge 0}$
    - algorithmically computable, hence TDA

We won't look at maps of "higher tetrahedra" modulo homotopy (they're simply connected). Rather we'll define a *homologous* relation between $p$-chains.

### Simplices

DEF: Let $\{e_n\}_0^\infty$ be the standard basis for $\RR^\infty$. The standard $p$-simplex $\Delta_p$ is the topological subspace ... given by the convex hull of the first $p+1$ basis vectors.

Similarly to affine hulls, the convex hull of the empty set has dimension $-1$ and is empty. The convex hull of a singleton $\{v_0\}$ has dimension $0$ and is just $\{v_0\}$. 

Note that convex and affine hulls are distinct, but both are described analogously by restrictive and constructive definitions. <https://en.wikipedia.org/wiki/Convex_hull>

DEF: An affine hull $\text{aff}(S)$ of a set is the smallest affine subspace containing the set. Constructively, ... $$\left\{\sum \lambda_i p_i :  p_i \in S, \lambda_i \in \RR, \text{ and } \sum \lambda_i = 1\right\}.$$ 

DEF: The convex hull $\text{conv}(S)$ is the smallest convex set containing $S$, whereas constructively, ... $$\left\{\sum \lambda_i p_i :  p_i \in S, \lambda_i \in I, \text{ and } \sum \lambda_i = 1\right\}.$$

EX: To construct the standard $p$-simplex, consider set of linear combinations ... $$\left\{\sum_{i =0}^p  \lambda_i e_i : \lambda_i \in [0,1] \text{ such that } \sum \lambda_i = 1\right\}.$$

EX: $\Delta_0$ is ... the set containing the point $\{(1, 0, 0, \ldots ) \}$ in $\RR^\infty$.

EX: $\Delta_1$ is homeomorphic to ... the closed interval $[0,1]$

EX: $\Delta_2$ is homeomorphic to ... a triangle.

We want to describe all possible embeddings of $p$-simplices in a topological space. So let $v_0, \ldots, v_p$ in $\RR^N$ be vectors. 

DEF: Let $[v_0, \ldots, v_p] \colon \Delta_p \to \RR^N$ send ... $$\sum \lambda_i e_i \mapsto \sum \lambda_i v_i.$$

The above map is said to be *degenerate* whenever (TFAE)

- the $v_i$ are affinely dependent
- there's a linear dependence $\sum \alpha_i v_i = \vec{0}$ between the $v_i$ such that atleast one coefficient $\alpha_\ell \neq 0$
- the set of differences $\{v_0 - v_1, \ldots, v_0 - v_p\}$ is linearly dependent 
- the $v_0, \ldots, v_p$ lie in an affine subspace (called a hyperplane) of codimension $1$ in $\RR^p$

<https://www.ti.inf.ethz.ch/ew/lehre/ApproxGeom08/notes/01_Basic_Geometry.pdf>

DEF: The ith face of $\Delta_p$ is the map $F_i^p \colon \Delta_{p-1} \to \Delta_p$ given by ... $$[e_0, \ldots, \underbrace{{ \hat{e}_i }}_{\text{omit}}, \ldots, e_p].$$

Why consider face maps $F_i^p  \colon \Delta_{p-1} \to \Delta_p \subset \RR^\infty$? Well, working in $\RR^\infty$ might later be useful for defining a chain complexes.

PROP: When $i < j$, the faces $F_i^p$ satisfy the simplicial identity ... $F_j^{p+1} \circ F_i^p = F_i^{p+1} \circ F_{j-1}^p$.

EX: For $i < j$, sketch the simplicial identity  $F_j^{p+1} \circ F_i^p = F_i^{p+1} \circ F_{j-1}^p$ ... $$\begin{CD} \Delta_{p-1} @>{F_i^p}>> \Delta_p\\ @VV{F_{j-1}^p}V @VV{F_j^{p+1}}V\\ \Delta_p @>{F_i^{p+1}}>>\Delta_{p+1} \end{CD}$$

IDEA: Geometrically describe the transition from homotopy to homology. ... Spheres replaced by simplices, with extra combinatorial data!

### Singular chains

Let $X$ be a topological space.

DEF: A singular $p$-simplex of $X$ is ... a continuous map $\sigma \colon \Delta_p \to X$.

### Graded abelian groups

> Given a math banana, you should tell me what's a map of bananas.

### Chain complexes

### Singular homology

## Week 2

### First homology groups

### Hurewicz

IDEA: If we have a continuous map from the topological boundary $f \colon \delta \Delta_n \to X$ that extends to a map $\sigma \colon \Delta_n \to X$ such that $\sigma \circ \iota = f$, then the algebraic boundary of the space $\Delta_n$ in the chain complex $\Delta_*(X)$ is just ... the appropriately signed image of the topological boundary $\delta\Delta_n$ in the free abelian group $\Delta_{n-1}(X)$.

Q: In the proof of the Hurewicz theorem, we defined $\psi \colon \sigma \mapsto \lambda_{\sigma(0)} * \sigma * \lambda_{\sigma(1)}^{-1}$, then restricted from $\Delta_1(X)$ to $Z_1(X)$. Why did we argue $\psi$ respects boundaries, that is, $B_1(X) \subset \ker\psi$? ... So that we could find $\psi_*$ that descends to the quotient.

From <https://math.stackexchange.com/questions/1168939/definition-of-descends-to>.

Q: What does it mean for maps to "descend to" other maps?  ... It usually has the same meaning as "induces a function on" (or "is compatible with the given equivalence relation"). It is often used in connection with the universal property of a quotient, which explains the "descend". (mathSE)

### Preview of relative homology

What homomorphism between $H_*(A)$ and $H_*(X)$ is induced by $A \hookrightarrow X$? Eventually, we'll prove the following (proposition borrowed from <https://ncatlab.org/nlab/show/relative+homology>).

> If $A \hookrightarrow X$ is a topological subspace inclusion which is good in the sense of the definition of a good pair, then the $A$-relative singular homology of $X$ coincides with the reduced singular homology of the quotient space $X/A$: $$H_n(X , A) \simeq \tilde H_n(X/A).$$

Such "good pairs" tend to arise when approximating a space by a CW-complex. Here's more motivation from <https://en.wikipedia.org/wiki/Relative_homology>.

DEF: For a topological space $X$ and a subset $A$, the relative chain complex is ... $\Delta_*(X, A) := \frac{\Delta_*(X)}{\Delta_*(A)}$.

Q: What's a topological interpretation of the relative chain complex $\Delta_*(X, A)$? ... Intuitively, it helps determine what part of an absolute homology group comes from which subspace.

EX: The relative homology group $H_n(X, x_0)$, where $x_0$ is a point in $X$, is just ... the $n$-th reduced homology group of $X$.

EX: For all $i > 0$, the relative homology group $H_i(X, x_0) = H_i(X)$. When $i = 0$, $H_0(X, x_0)$ is what? (and why?) ... It's the free module of one rank less than $H_0(X)$, because the connected component containing $x_0$ becomes trivial in relative homology.

Where are we to begin? Well,  visibly, $\Delta_*(A) \hookrightarrow \Delta_*(X)$. This gives a short exact sequence (of chain complexes) $$0 \to \Delta_*(A) \hookrightarrow \Delta_*(X) \to \frac{\Delta_*(X)}{\Delta_*(A)} \to 0.$$ 

We'll need more homological algebra (the snake lemma) to argue that the short exact sequence of chain groups produces a long exact sequence of homology groups.

Then I suppose we aim to prove the excision theorem.

### Long exact sequences

DEF: The diagram $$\cdots \to A_{n+1} \to A_n \to A_{n-1} \to \cdots$$ of Abelian groups is exact if ... it's exact in each degree.

To quote basic definitions from [@May99, chapter 12.4]---we'll need these for speed!

DEF: A sequence $M' \xrightarrow{f} M \xrightarrow{g} M''$ of modules is exact (at $M$) if ... $f(M') = \ker g$.

DEF: Suppose $0 \to M \xrightarrow{g} M''$ is exact. Then ... $g$ is a monomorphism. 

DEF: Suppose $M' \xrightarrow{f} M \to 0$ is exact. Then ... $f$ is an epimorphism.

I asked about the sequence of abelian groups with their homomorphisms as an object in some category.

EX: The diagram $$\cdots \to A_{n+1} \to A_n \to A_{n-1} \to \cdots$$ of Abelian groups and group homomorphisms is an object in ... the category $$\mathrm{Fun}\left(\{\mathrm{Obj}(\ZZ), \mathrm{Morp}(a,b) = \{\emptyset \text{ if $a>b$, else pt. if $a < b$}\}\}, \mathrm{Ab}\right).$$

From [“functor in nLab”](https://ncatlab.org/nlab/show/functor). Retrieved January 25, 2019.

> A functor $F$ from a category $C$ to a category $D$ is a map sending each object $x \in C$ to an object $F(x) \in D$ and each morphism $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$, such that $F$ preserves composition $F(g\circ f) = F(g)\circ F(f)$ whenever the left-hand side is well-defined, $F$ preserves identity morphisms for each object $x \in X$, $F(1_x) = 1_{F(x)}$.
> 
> Or equivalently, since compositions $g f = g\circ f$ (commuting triangles) and identities $1_x$ (commuting loops) are both simple commuting diagrams, we can combine the above conditions to the single statement $F$ preserves commuting diagrams.

Anyways, so a long exact sequence exhibits an object in the functor category $\mathrm{Quiv}$ or $\mathrm{DiGraph}$. 

To quote definitions from [“Quiv in nLab”](https://ncatlab.org/nlab/show/Quiv). Retrieved January 26, 2019.

DEF: A quiver is a functor $G\colon X^{op} \to \mathrm{Set}$, where $X^{op}$ is the category with ... an object $0$, an object $1$ and two morphisms $s, t\colon 1 \to 0$, along with identity morphisms. 

DEF: $\mathrm{Quiv}$ is ... the functor category from $X^{op}$ to $\mathrm{Set}$.

DEF: The objects and morphisms of $\mathrm{Quiv}$ are ... the functors $G\colon X^{op} \to Set$, and the natural transformations between such functors.

Here's another example from [“Functor category”](https://en.wikipedia.org/wiki/Functor_category). English Wikipedia. Retrieved January 26, 2019.

EX: Any group $G$ can be considered as a one-object category in which every morphism is invertible. The category of all $G$-sets is the same as ... the functor category $\mathrm{Set}^G$.
