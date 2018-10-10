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

\newcommand{\QQ}{\mathbf{Q}}
\newcommand{\NN}{\mathbf{N}}
\newcommand{\ZZ}{\mathbf{Z}}
\newcommand{\RR}{\mathbf{R}}
\newcommand{\sB}{\mathscr{B}}
\newcommand{\sC}{\mathscr{C}}
\newcommand{\sT}{\mathscr{T}}

### Week 1

Course with [Carla Farsi](https://math.colorado.edu/~farsi/). 

assessment | weight
--- | ---
presentations | 10%
homeworks | 20%
midterm 1 | 20%
midterm 2 | 20%
final exam | 30%

The course's first part will cover point-set topology up to the definitions of connected, respectively compact, spaces (which, fortunately, mirrors Rosoff's notes [@Ro16]). 

After passing through canonical definitions, counter examples, etc. in point-set, the second part  will introduce algebraic topology, namely, the correspondence between covering spaces and fundamental groups.

We'll cover Munkres [@Mu00], *excluding*

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

#### Axioms

We defined a topological structure on a set and the corresponding topological space. 

An introduction from [@Su75, chapter 3.1] and [@Ru87].

DEF: (Sutherland) A topological space is a nonempty set $A$ together with ... a fixed collection $\sT$ of subsets of $A$  satisfying (T1) $A, \emptyset \in A$; (T2) the intersection of any two sets in $\sT$ is again in $\sT$; (T3) the union of an arbitrary collection of sets in $\sT$ is again in $\sT$.

DEF: (Rudin) A collection of subset of $X$ is said to be a topology in $X$ if $\sT$ has the following properties ... (i) $\emptyset \in \sT$ and $X \in \sT$; (ii) if $V_i \in \sT$ for $i = 1, \ldots, n$, then $V_1 \cap \ldots \cap V_n \in \sT$; (iii) if $\{V_\alpha\}$ is an arbitrary collection of members of $\sT$, then $\cup_\alpha V_\alpha \in \sT$.

We can draw an abstract analogy between topological spaces and [measurable spaces](/prelims/algebra).

topological spaces | measurable spaces
--- | ---
topology | $\sigma$-algebra
open set | measurable set
continuous function | measurable function

DEF: If $\sT$ is a topology on $X$, then $X$ is called a topological space, and the members of $\sT$ are called the open sets in $X$.

DEF: (Rudin) If $X$ and $Y$ are topological spaces and if $f$ is a mapping of $X$ into $Y$, then $f$ is said to be continuous provided that ... $f^{-1}(V)$ is an open set in $X$ for every open set $V$ in $Y$.

#### Little examples

To laundry list some exemplar topological structures

- a discrete space $(X, 2^X)$
- an indiscrete space $X$ with open sets $X$ and $\emptyset$
- the arrow, $X = [0, \infty)$ with open sets of the form $(a, \infty)$ for $a \ge 0$.
- a cofinite topology
    - the real line with $T_1$ topology, where the open sets are $\RR$, $\emptyset$, and sets with finite complements
    - the complex plane with the cofinite topology
- a cocountable topology
    - the real line with open sets having countable complements
- the poset $\{a,b,c,d\}$ with open sets $\emptyset, X, \{a\}, \{b\}, \{a,c\},\{a,b,c\},\{a,b\}$
- the connected pair of points
- the Sierpiŉski topology, $\{\emptyset, \{0\},\{0,1\}\}$ on $X = \{0,1\}$
- a particular point topology $Y= X \cup \{a\}$, whose definition requires some finite topological space $(X, \Omega)$, with the topological structure $$\{\{a\} \cup U: U \in \Omega\}\cup \{\emptyset\}.$$
- the arithmetic progressions of positive integers form a base for some topology on $\NN$ (and $\ZZ$)
    - whence a slick proof of the infinitude of prime numbers
- the empty space as "the empty set endowed with the only possible topology on it"
    - the *initial object* in the category of topological spaces

The following example we'll have to revisit. Its open sets are defined *synthetically* (and we haven't yet the notion of a basis or subbasis for a topological structure).

- the standard topology on the real line, with topological structure as an *linear continuum*
    - $\RR$ having the least upper bound property
    - for $x < y$ in $\RR$, there's a $z \in \RR$ such that $x<z<y$

Now, Vipul Naik has a category of [particular topological spaces](https://topospaces.subwiki.org/wiki/Category:Particular_topological_spaces) on the Topospaces wiki, but to describe their open sets, we'll need, e.g., Emily Reihl's [On the construction of new topological spaces from existing ones](http://math.jhu.edu/~eriehl/topologies.pdf).

Ordered by set theoretic containment, we compare topological structures (*on the same set!*) as finer or coarser, where a discrete topology is the finest and an indiscrete topology the coarsest.

#### Motivation

##### Topological structures qua sets

From [@Gow08, number III.90]: The concept of a straight up topological structure might be a bit too general. We'll often require our topological space to be *Hausdorff*, and we'll usually work with basis sets rather than open sets.

DEF! The topological space $X$ is said to be Hausdorff iff ... for any two points $x_1$ and $x_2$ in $X$ there are disjoint open sets $U_1$ and $U_2$ such that $U_1 \ni x_1$ and $U_2 \ni x_2$.

DEF! A basis $\sB$ for a topological space $(X, \sT)$ is a subcollection of $\sT$ such that ... every open set is a union of open sets in $\sB$.

What properties do we study of topological structures alone?

- separability
- countability
- connectedness
    - Are the points in $\RR^2$ with exactly one rational coordinate connected?
    - That is, is the space $((\QQ \times \RR) \cup (\RR \times \QQ)) \setminus (\QQ \times \QQ)$ connected or not?
- compactness
    - In what spaces is a closed and bounded set compact?

DEF! We say that a space $X$ is connected if ... there is no decomposition $X = U_1 \cup U_2$ of $X$ into two disjoint, nonempty, open sets.

Note, in $\RR$, open sets may be written as countable unions of open intervals.

DEF! We say that a space $X$ is compact if ... given any collection $\sC$ of open sets that cover $X$ (i.e., whose union is $X$) we may find a finite subcollection $\{U_1, \ldots, U_k\} \subset \sC$ that still covers $X$.

##### Functions

In a naive sense, we care deeply about set theory only insofar that *functions between sets* are well defined and (mathematically) interesting. At least one driving motivation in the historical development of the subject was to generalize continuity, that is, to abstract an analytic notion of distance in favor of a set theoretic notion of inclusion in sufficiently many neighborhoods of a point.

##### Local to global principles

Now the structure of domain and codomain constrains the families of functions that are well defined between them.

- for coarse topologies, we're interested in functions taking values in the codomain [@Ri15]
- for fine topologies, we want to know which functions can be defined out of the domain

From [@Go08, number III.9] on compactness: Each of the following is true when $X$ is finite and false otherwise.

- all functions defined on $X$ are bounded
- all functions defined on $X$ attain a maximum
- all sequences in $X$ have convergent subsequences

How can we proceed from local principles towards global properties (and vice versa)? For example, suppose a function's values are bounded at each point separately. In what cases can one argue that because $f$ is bounded pointwise, there's a single, global bound, $M$ such that $M \le \abs{f(x)}$ for all $x \in X$? What should our domain be?

- a set
- a topological space
- a metric space
- a group?

What global to local properties are amenable to these settings?

EX! In the category of topological and metric spaces these "almost finite" objects are known as ... compact spaces.

Likewise, in the category of groups we have the notion of a pro-finite group, and in the category of normed spaces with linear operators there's a notion of a compact operator which is of "almost finite rank".

#### Bases for topological structures

Associated to each topology $\sT$, we have a family of collections of sets $\{\Sigma\}$ called *bases for the topology*. In the wild, we may encounter a base $\Sigma$ either before ("synthetically") or after ("analytically") seeing the topology. 

That is, we can both

- *find* $\Sigma$ such that every open set in a given topological structure $\sT$ can be written as a union of elements in $\Sigma$, which is equivalent to requiring that if $U$ is an open set in $\sT$ and $x \in U$, there exists a basis element $B \in \Sigma$ such that $x \in B \subset U$, or
- *generate* a topological structure $\sT$ on $X$ from $\Sigma$, where the union of elements in $\Sigma$ is $X$ and the intersection of any two sets in $\Sigma$ is the union of some sets in $\Sigma$; in this case the open sets in $\sT$ are *defined* as unions of sets in $\Sigma$.

To borrow a definition and proposition (base vs basis---why?) from Sutherland, [@Su75, chapter 3]:

DEF! (Synthetic basis criteria) Given a set $A$, a collection $\sB$ of subsets of $A$ is a basis for $A$ if ... (B1) $A$ is a union of sets from $\sB$, (B2) if  $B_1, B_2 \in \sB$, then the intersection of $B_1 \cap B_2$ is a union of sets from $\sB$.

In the synthetic case, to specify a topology on a set, we may say "Let $\sT$ be a topology with the sets ... as a basis." In this case, the named sets should satisfy (B1) and (B2).

PROP! Suppose that $\sB$ is a basis for a nonempty set $A$, and let $\sT$ be given by ... $\{U \in 2^A : U \text{ is a union of sets from } \sB\}$. Then $\sT$ is a topology for $A$.

In the analytic case, when we "find a base" for a topological structure $\sT$, we say that $\sT$ *admits* a basis.

DEF! A topological space that admits a countable basis is called ... second countable.

Now $\RR^n$ is a metric space (with a family of equivalent $\ell_p$ metrics). To specify a topological structure on $\RR^n$, let the open sets be those sets $E$ such that for all $x \in E$, there's an open ball $B_\epsilon(x)$ of some radius $\epsilon >0$ around $x$ such that $x \in B_\epsilon(x) \subset E$. Note that with rational balls $\RR^n$ is second countable.

Base elements should be easier to handle than open sets qua elements of the topology. We'll cite two examples, the first due to the of connective properties of $\RR$, and the second fora 
EX! Every nonempty open set in $\RR$ can be written as a ... countable union of open intervals.

### Week 2

#### Continuous functions

Morphisms we care about, from [@Su75, chapter 3.1]:

DEF! Given any two topological spaces $X$ and $Y$, we say a function $f\colon X \to Y$ is continuous if ... for every $Y$-open $U$, $f^{-1}(U)$ is $X$-open too.

DEF! A function $f \colon X \to Y$ between topological spaces $X$ and $Y$, is strongly continuous if ... $U$ is $Y$-open iff $f^{-1}(U)$ is $X$-open.

DEF! A function $f\colon X \to Y$ is continuous at a point $a \in X$ if ... given any neighborhood $U$ of $f(a)$ there exists a neighborhood $V$ of $a$ such that $f(V) \subset U$.

\newcommand{\Int}[1]{\left(#1\right)^\circ}
\newcommand{\Cl}[1]{\overline{#1}}

With interiors, closures, and a local definition of continuity, we can cycle through the following characterizations of continuity. 

Suppose that $X$ and $Y$ are topological spaces. Consider a function $f \colon X \to Y$. The following are equivalent.

(a) $f$ is continuous.
(b) $f^{-1}(\Int{B}) \subset \Int{f^{-1}(B)}$ for all sets $B\subset Y$ in the codomain.
(c) $\Cl{f^{-1}(B)} \subset f^{-1}\left(\Cl{B}\right)$ for all sets $B \subset Y$ in the codomain.
(d) $f\left(\Cl{A}\right) \subset \Cl{f(A)}$ for all sets $A\subset X$ in the domain.
(e) $f$ is continuous at the point $x$ for all $x \in X$ in the domain.

For a function between metric spaces, the $\epsilon$-$\delta$ definition usually studied in Calculus is also equivalent to those criteria above.

Lastly, since the inverse image is a set map that respects unions and intersections, to check that $f \colon X \to Y$ is continous, it's enough to show that, for each set $B$ is some basis $\sB$ for the topology of $Y$, the inverse image $f^{-1}(B)$ is open in $X$.

> For suppose that this has been proven. Then for any open set $U$ in $Y$, we write $U = \cup B_i$ for basis elements $B_i$ in $\sB$. Thence $f^{-1}(U) = f^{-1}\left(\cup B_i\right) = \cup f^{-1}(B_i)$. [@Su75, chapter 3.2]

#### New spaces from old: products

There are three reasonable topologies with which to endow a product of topological spaces

- a box topology, 
- a uniform topology,
- a product topology,

but only one of the above has the desirable universal property. From [@Ri15, page 8]:

DEF! (Coarsest topology for the product) Given spaces $X_\alpha$, the product topology on $\prod_\alpha X_\alpha$ is the coarsest topology so that ... the canonical projections $\prod_\alpha X_\alpha \to X_\alpha$ are continuous.A

ALTDEF! (Product topology) Given spaces $X_\alpha$ the product topology on $\prod_\alpha X_\alpha$ has open sets: ... $\prod_\alpha U_\alpha$ where $U_\alpha \subset X_\alpha$ is open and $U_\alpha = X_\alpha$ for all but finitely many indices $\alpha$.

THM! (Universal property of the product topology) Let $Z$ be a topological space, let $X_\alpha$ be a collection of spaces, and give $\prod_\alpha X_\alpha$ the product topology. Then a function $f \colon Z \to \prod_\alpha X_\alpha$ is continuous if and only if ... each coordinate function $f_\alpha \colon Z \to X_\alpha$ is continuous.

The box topology is defined by amending "all but finitely many indices $\alpha$" to "maybe" in the definition of the product topology. When $A$ is finite, the box and product topology coincide. Otherwise, when $A$ is infinite, the box topology is strictly finer than the product topology. Hence for the box topology, the universal property "degrades" into a single sided implication. 

> Consider $\RR^\omega$ with the box topology, the function $t \mapsto (t,t,t,\ldots):\RR \to \RR^\omega$ is not continuous even though its coordinate functions are. [@Ri15, p. 9]

As a warning against naive interpretation, note that the product topology is *not* necessarily hyperconnected (as a cofinite topology on an infinite set must be). That is, two open sets in these topologies intersect when they intersect in *all coordinates*, not just a handful.

