---
title: Topology 2
author: Colton Grainger
date: 2019-01-13
revised:
bibliography: /home/colton/coltongrainger.bib
nonumbering: true
---

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

measure | weigh
--- | ---
presentations | 40%
write-ups | 30%
participation | 10%
final exam | 20%

## Spring semester notes

I have tried (and failed) to talk myself out of keeping notes:

- I have no comparative advantage to narrate the development of homology/cohomology.
    - For example, Dr. Beaudry is live-TeXing her lecture notes, and [extensive references](https://math.stackexchange.com/a/1560607/469856) for algebraic topology notes are already listed on stackexchange. 

- When considering Philip Guo's [heuristic](http://pgbovine.net/writings.htm) when deciding what to write    

    > Will at least 100 people care about this topic three years from now?

    - I suspect the answer is yes, in general.
    - It's unlikely, however, that at least 100 people will care about my perspective.

- My preferred markup language is pandoc markdown, rendered here with MathJax, which has [limited support](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) for [commutative diagrams](http://www.jmilne.org/not/Mamscd.pdf). 
    - Just to render diagonal arrows, I'll have to port images from <http://presheaf.com/>.

$\begin{CD}
A     @>\text{ for example }>>  B\\
@VVbV        @VVcV\\
C     @> \text{ with AMScd }>>  D
\end{CD}$

However, in juxtaposed posts,

- <http://www.aaronsw.com/weblog/greatlectures>
- <http://www.aaronsw.com/weblog/awfullectures>

Aaron Schwartz via Tufte reminds us "to always ask about the information density of a method of communication".

Won't these notes be sparse on content? 

Well, sure, but some communication owes its efficacy to "emotional density". So Schwartz' second essay wins out, and I'll bother anyways to record how I think and feel about the curriculum.

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
        - cf <https://arxiv.org/abs/1002.3081>

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

DEF! Let $\{e_n\}_0^\infty$ be the standard basis for $\RR^\infty$. The standard $p$-simplex is the topological subspace ... given by the convex hull of the first $p+1$ basis vectors.

Similarly to affine hulls, the convex hull of the empty set has dimension $-1$ and is empty. The convex hull of a singleton $\{v_0\}$ has dimension $0$ and is just $\{v_0\}$. 

Note that convex and affine hulls are distinct, but both are described analogously by restrictive and constructive definitions. <https://en.wikipedia.org/wiki/Convex_hull>

hull | restrictive def | constructive def
--- | --- | ---
$\text{aff}(S)$ | An affine hull of a set is the smallest affine subspace containing the set. | $$\{\sum \lambda_i p_i : n \ge 0, p_i \in S, \lambda_i \in \RR, \text{ and } \sum \lambda_i = 1\}$$
$\text{conv}(S)$ | A convex hull is the smallest convex set, etc | $$\{\sum \lambda_i p_i : n \ge 0, p_i \in S, \lambda_i \in I, \text{ and } \sum \lambda_i = 1\}$$


EX! To construct the standard $p$-simplex, consider set of linear combinations ... $$\left\{\sum_{i =1}^p  \lambda_i e_i : \lambda_i \in [0,1] \text{ such that } \sum \lambda_i = 1\right\}.$$

EX! $\Delta_0$ is ... the set containing the point $\{(1, 0, 0, \ldots ) \}$ in $\RR^\infty$.

EX! $\Delta_1$ is homeomorphic to ... the closed interval $[0,1]$

EX! $\Delta_2$ is homeomorphic to ... a triangle.

We want to describe all possible embeddings of $p$-simplices in a topological space.

Let $v_0, \ldots, v_p$ in $\RR^N$ be vectors. 

DEF! Let $[v_0, \ldots, v_p] \colon \Delta_p \to \RR^N$ send ... $$\sum \lambda_i e_i \mapsto \sum \lambda_i v_i.$$

The above map is said to be *degenerate* whenever (TFAE)

- the $v_i$ are affinely dependent
- there's a linear dependence $\sum \alpha_i v_i = \vec{0}$ between the $v_i$ such that atleast one coefficient $\alpha_\ell \neq 0$
- the set of differences $\{v_0 - v_1, \ldots, v_0 - v_p\}$ is linearly dependent 
- the $v_0, \ldots, v_p$ lie in an affine subspace (called a hyperplane) of codimension $1$ in $\RR^p$

<https://www.ti.inf.ethz.ch/ew/lehre/ApproxGeom08/notes/01_Basic_Geometry.pdf>

DEF! The ith face of $\Delta_p$ is the map $F_i^p \colon \Delta_{p-1} \to \Delta_p$ given by ... $$[e_0, \ldots, \underbrace{{ \hat{e}_i }}_{\text{omit me}}, \ldots, e_p].$$

If you need to, consider the face maps as $F_i^p  \colon \Delta_{p-1} \to \Delta_p \subset R^\infty$, so that the faces respectively line up.
