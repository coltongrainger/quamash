---
title: Topology for prelims
author: Colton Grainger
date: 2018-08-27
---

## Exam syllabus

### Point-set topology

- topological spaces
    - subspaces
    - products (and box)
    - quotients
- countability axioms
- properties of spaces
    - $T$-separation axioms
    - compact
    - connected
- canonical examples
    - spheres
    - projective spaces
    - homogeneous spaces
    - CW-complexes

### Basic algebraic topology

- foundations
    - homotopy
- canonical examples
    - simply connected spaces
    - circles and $n$-spheres
    - compact surfaces
- fundamental groups
    - functorial properties
    - deformation retractions
- Seifert-van Kampen theorem
- applications
    - Brouwer fixed-point theorem
    - fundamental theorem of algebra
    - Hairy Ball theorem
- covering spaces
    - universal covering spaces
    - lifting lemma
    - covering homotopy
    - group actions
- homology
    - singular homology
    - the Eilenberg-Steenrod axioms
    - homology group of spheres
    - the degree of a map between spheres
    - homology calculations via CW complexes
    - proof of homotopy invariance
    - proof of excision
    - universal coefficient 
    - Kunneth Theorem

### Differential Geometry

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

## Fall semester notes

### Week 1

Course with Carla Farsi. We'll cover Munkres [@Mu00], excluding

- the Tychonoff theorem
    - Stone-Čech compactification
- Baire spaces
    - nowhere differentiable functions
    - dimension theory
- separation theorems in the place
    - the Jordan separation theorem
    - the Jordan curve theorem
    - embedding graphs in the plane
    - the Cauchy integral formula
- applications to group theory
    - covering spaces of a graph
    - subgroups of free groups

The course's first part will address point-set topology up to the definitions of connected, respectively compact, spaces (which, fortunately, mirrors Rosoff's notes [@Ro16]).

### Week 2

#### Local to global principles

From [@Su75, chapter 3.1] and [@Ru87], an introduction.

\newcommand{\sT}{\mathscr{T}}

DEF: (Sutherland) A topological space is a nonempty set $A$ together with ... a fixed collection $\sT$ of subsets of $A$  satisfying (T1) $A, \emptyset \in A$; (T2) the intersection of any two sets in $\sT$ is again in $\sT$; (T3) the union of an arbitrary collection of sets in $\sT$ is again in $\sT$.

We keep in mind the following abstract analogy between topological spaces and [measurable spaces](/prelims/algebra).

topological spaces | measurable spaces
--- | ---
topology | $\sigma$-algebra
open set | measurable set
continuous function | measurable function

DEF: (Rudin) A collection of subset of $X$ is said to be a topology in $X$ if $\sT$ has the following properties ... (i) $\emptyset \in \sT$ and $X \in \sT$; (ii) if $V_i \in \sT$ for $i = 1, \ldots, n$, then $V_1 \cap \ldots \cap V_n \in \sT$; (iii) if $\{V_\alpha\}$ is an arbitrary collection of members of $\sT$, then $\cup_\alpha V_\alpha \in \sT$.

DEF: If $\sT$ is a topology on $X$, then $X$ is called a topological space, and the members of $\sT$ are called the open sets in $X$.

DEF: (Rudin) If $X$ and $Y$ are topological spaces and if $f$ is a mapping of $X$ into $Y$, then $f$ is said to be continuous provided that ... $f^{-1}(V)$ is an open set in $X$ for every open set $V$ in $Y$.

Our goal is to generalize continuity, moving from the notion of *distance as a measurement* to that of *closeness as inclusion* in sufficiently many open sets. In the transition, one might ask of functions:

- Does the image of any sequence converge to the "correct" functional limit?
- Do I have a local neighborhood system?
- Can I show $f$ is continuous at a point $a$? At all points in the domain?
- Are inverse images of open sets open in the domain?

From [@Gow08, number III.90]: The concept of a straight up topological structure might be a bit too general. We'll often require our topological space to be *Hausdorff*, and we'll usually work with basis sets rather than open sets.

DEF! The topological space $X$ is said to be Hausdorff iff ... for any two points $x_1$ and $x_2$ in $X$ there are disjoint open sets $U_1$ and $U_2$ such that $U_1 \ni x_1$ and $U_2 \ni x_2$.

\newcommand{\sB}{\mathscr{B}}

DEF! A basis $\sB$ for a topological space $(X, \sT)$ is a subcollection of $\sT$ such that ... every open set is a union of open sets in $\sB$.

To list non-trivial examples of topological structures.

- the discrete topology
- the euclidean $\RR^n$
- the subspace topology
- the [Zariski topology](https://en.wikipedia.org/wiki/Zariski_topology)
    - What is Hilbert's basis theorem?

What properties do we study of topological structures alone?

\newcommand{\QQ}{\mathbf{Q}}

- connectedness
    - Are the points in $\RR^2$ with exactly one rational coordinate connected?
    - That is, is the space $((\QQ \times \RR) \cup (\RR \times \QQ)) \setminus (\QQ \times \QQ)$ connected or not?
- compactness
    - In what spaces is a closed and bounded set compact?

DEF! We say that a space $X$ is connected if ... there is no decomposition $X = U_1 \cup U_2$ of $X$ into two disjoint, nonempty, open sets.

Note, in $\RR$, open sets may be written as countable unions of open intervals.

\newcommand{\sC}{\mathscr{C}}

DEF! We say that a space $X$ is compact if .. given any collection $\sC$ of open sets that cover $X$ (i.e., whose union is $X$) we may find a finite subcollection $\{U_1, \ldots, U_k\} \subset \sC$ that still covers $X$.

#### Compactness and Compactification

Notes from [@Go08, number III.9]: Each of the following is true when $X$ is finite and false otherwise.

- all functions defined on $X$ are bounded
- all functions defined on $X$ attain a maximum
- all sequences in $X$ have convergent subsequences

We want to proceed from local principles towards global properties (and vice versa). For example, suppose a function's values are bounded at each point separately. In what cases can one argue that because $f$ is bounded pointwise, there's a single, global bound, $M$ such that $M \le \abs{f(x)}$ for all $x \in X$?

What should our domain be?

- a set
- a topological space
- a metric space
- a group?

What global to local properties are amenable to these settings?

EX! In the category of topological and metric spaces these "almost finite" objects are known as ... compact spaces.

Likewise, in the category of groups we have the notion of a pro-finite group, and in the category of normed spaces with linear operators there's a notion of a compact operator which is of "almost finite rank".

\newcommand{\sB}{\mathscr{B}}
