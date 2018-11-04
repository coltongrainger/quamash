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
    - compactness
    - connectedness
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
\providecommand{\abs}[1]{\left\lvert #1 \right\rvert}

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

DEF: The topological space $X$ is said to be Hausdorff iff ... for any two points $x_1$ and $x_2$ in $X$ there are disjoint open sets $U_1$ and $U_2$ such that $U_1 \ni x_1$ and $U_2 \ni x_2$.

DEF: A basis $\sB$ for a topological space $(X, \sT)$ is a subcollection of $\sT$ such that ... every open set is a union of open sets in $\sB$.

What properties do we study of topological structures alone?

- separability
- countability
- connectedness
    - Are the points in $\RR^2$ with exactly one rational coordinate connected?
    - That is, is the space $((\QQ \times \RR) \cup (\RR \times \QQ)) \setminus (\QQ \times \QQ)$ connected or not?
- compactness
    - In what spaces is a closed and bounded set compact?

DEF: We say that a space $X$ is connected if ... there is no decomposition $X = U_1 \cup U_2$ of $X$ into two disjoint, nonempty, open sets.

Note, in $\RR$, open sets may be written as countable unions of open intervals.

DEF: We say that a space $X$ is compact if ... given any collection $\sC$ of open sets that cover $X$ (i.e., whose union is $X$) we may find a finite subcollection $\{U_1, \ldots, U_k\} \subset \sC$ that still covers $X$.

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

EX: In the category of topological and metric spaces these "almost finite" objects are known as ... compact spaces.

Likewise, in the category of groups we have the notion of a pro-finite group, and in the category of normed spaces with linear operators there's a notion of a compact operator which is of "almost finite rank".

### Week 2

#### Bases for topological structures

Associated to each topology $\sT$, we have a family of collections of sets $\{\Sigma\}$ called *bases for the topology*. In the wild, we may encounter a base $\Sigma$ either before ("synthetically") or after ("analytically") seeing the topology. 

That is, we can both

- *find* $\Sigma$ such that every open set in a given topological structure $\sT$ can be written as a union of elements in $\Sigma$, which is equivalent to requiring that if $U$ is an open set in $\sT$ and $x \in U$, there exists a basis element $B \in \Sigma$ such that $x \in B \subset U$, or
- *generate* a topological structure $\sT$ on $X$ from $\Sigma$, where the union of elements in $\Sigma$ is $X$ and the intersection of any two sets in $\Sigma$ is the union of some sets in $\Sigma$; in this case the open sets in $\sT$ are *defined* as unions of sets in $\Sigma$.

To borrow a definition and proposition (base vs basis---why?) from Sutherland, [@Su75, chapter 3]:

DEF: (Synthetic basis criteria) Given a set $A$, a collection $\sB$ of subsets of $A$ is a basis for $A$ if ... (B1) $A$ is a union of sets from $\sB$, (B2) if  $B_1, B_2 \in \sB$, then the intersection of $B_1 \cap B_2$ is a union of sets from $\sB$.

In the synthetic case, to specify a topology on a set, we may say "Let $\sT$ be a topology with the sets ... as a basis." In this case, the named sets should satisfy (B1) and (B2).

PROP: Suppose that $\sB$ is a basis for a nonempty set $A$, and let $\sT$ be given by ... $\{U \in 2^A : U \text{ is a union of sets from } \sB\}$. Then $\sT$ is a topology for $A$.

In the analytic case, when we "find a base" for a topological structure $\sT$, we say that $\sT$ *admits* a basis.

DEF: A topological space that admits a countable basis is called ... second countable.

Now $\RR^n$ is a metric space (with a family of equivalent $\ell_p$ metrics). To specify a topological structure on $\RR^n$, let the open sets be those sets $E$ such that for all $x \in E$, there's an open ball $B_\epsilon(x)$ of some radius $\epsilon >0$ around $x$ such that $x \in B_\epsilon(x) \subset E$. Note that with rational balls $\RR^n$ is second countable.

Base (or basis, whatever) elements should be easier to handle than open sets qua elements of the topology. We summon two examples, the first due to the connective properties of $\RR$, and the second just an application of $f^{-1}$ as a [set map](https://en.wikipedia.org/wiki/Inverse_image_functor) respecting unions.

EX: Every nonempty open set in $\RR$ can be written as a ... countable union of open intervals.

EX: To check that $f \colon X \to Y$ is continuous, it's enough to show that, for each set $B$ ... in some basis $\sB$ for the topology of $Y$, the inverse image $f^{-1}(B)$ is open in $X$.

> For suppose that this has been proven. Then for any open set $U$ in $Y$, we write $U = \cup B_i$ for basis elements $B_i$ in $\sB$. Thence $f^{-1}(U) = f^{-1}\left(\cup B_i\right) = \cup f^{-1}(B_i)$. [@Su75, chapter 3.2]

DEF: A subbasis for a topology $\sT$ is a subcollection $\sS \in \sT$ such that any set in $\sT$ can be written ... as a union of finite intersections of sets from $\sS$.

To sketch a (naive) analogy between three hierarchies in three subjects. 

topology | measure theory | algebra
--- | --- | --- 
subbasis | semialgebra | generating elements
basis | algebra | the presentation of a group
topology | $\sigma$-algebra | the whole enchilada

(At some point Connor asked if there was a [categorical notion of "generating"](https://math.stackexchange.com/questions/749805/the-idea-of-generators-for-arbitrary-categories).)

PROP: The topology generated by a subbasis $\sS$ is the coarsest topology containing $\sS$, also characterized as the ... intersection of all topologies containing $\sS$.

SCHEMA: Consider a family of spaces $X_\alpha$ and a set $X$ given the coarsest topology so that certain maps $f_\alpha \colon X \to X_\alpha$ are continuous. (It's the topology generated by $\{f_\alpha^{-1}(U_\alpha) : U_\alpha \text{ is open in $X_\alpha$, for all $\alpha$}\}$.) Then if $Z$ is any space, a function $f:Z \to X$ is continuous if and only if ... the composite maps $f\circ f_\alpha \colon Z \to X \to X_\alpha$ are continuous.

#### Continuous functions

Morphisms we care about, from [@Su75, chapter 3.1]:

AGAIN: Given any two topological spaces $X$ and $Y$, we say a function $f\colon X \to Y$ is continuous if ... for every $Y$-open $U$, $f^{-1}(U)$ is $X$-open too.

DEF: A function $f \colon X \to Y$ between topological spaces $X$ and $Y$, is strongly continuous if ... $U$ is $Y$-open iff $f^{-1}(U)$ is $X$-open.

DEF: A function $f\colon X \to Y$ is continuous at a point $a \in X$ if ... given any neighborhood $U$ of $f(a)$ there exists a neighborhood $V$ of $a$ such that $f(V) \subset U$.

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

#### New spaces from old: products

There are three reasonable topologies with which to endow a product of topological spaces

- a box topology, 
- a uniform topology,
- a product topology,

but only one of the above has the desirable universal property. From [@Ri15, page 8]:

DEF: (Coarsest topology for the product) Given spaces $X_\alpha$, the product topology on $\prod_\alpha X_\alpha$ is the coarsest topology so that ... the canonical projections $\prod_\alpha X_\alpha \to X_\alpha$ are continuous.A

ALTDEF: (Product topology) Given spaces $X_\alpha$ the product topology on $\prod_\alpha X_\alpha$ has open sets: ... $\prod_\alpha U_\alpha$ where $U_\alpha \subset X_\alpha$ is open and $U_\alpha = X_\alpha$ for all but finitely many indices $\alpha$.

THM: (Universal property of the product topology) Let $Z$ be a topological space, let $X_\alpha$ be a collection of spaces, and give $\prod_\alpha X_\alpha$ the product topology. Then a function $f \colon Z \to \prod_\alpha X_\alpha$ is continuous if and only if ... each coordinate function $f_\alpha \colon Z \to X_\alpha$ is continuous.

The box topology is defined by amending "all but finitely many indices $\alpha$" to "maybe" in the definition of the product topology. When $A$ is finite, the box and product topology coincide. Otherwise, when $A$ is infinite, the box topology is strictly finer than the product topology. Hence for the box topology, the universal property "degrades" into a single sided implication. 

> Consider $\RR^\omega$ with the box topology, the function $t \mapsto (t,t,t,\ldots):\RR \to \RR^\omega$ is not continuous even though its coordinate functions are. [@Ri15, p. 9]

As a warning against naive interpretation, note that the product topology is *not* necessarily hyperconnected (as a cofinite topology on an infinite set must be). That is, two open sets in these topologies intersect when they intersect in *all coordinates*, not just a handful.

### Week 3

#### A problem textbook is found!

Great news: I started into Viro, Ivanov, Netsvetaev, and Kharlamov's *[Elementary Topology: Problem Textbook](https://www.maths.ed.ac.uk/~v1ranick/papers/viro.pdf)*. And then, in a backwards looking fit of anxiety, I pulled these definitions out of context. 

DEF: Fix $x \in X$. An (open) neighborhood of $x$ is ... an open set containing $x$.

DEF: Let $X$ be a space and $a$ some point in $X$. A neighborhood base at $a$ (or just a base of $X$ at $a$) is a collection $\Sigma$ of neighborhoods of $a$ such that ... each neighborhood of $a$ contains a neighborhood from $\alpha$.

DEF: A collection $\sigma = \{U_\alpha\}$ of open sets is said to be an open cover of a subset $A$ if ... $$A \subset \cup_\alpha U_\alpha.$$

DEF: The subset $A$ of a topological space is compact if given any open cover of $A$, there's a finite subcover.

DEF: A topological space $X$ is connected if it's not possible to find two open sets $U$ and $V$ in $X$ with $X = U \cup V$ and $U \cap V = \emptyset$.

DEF: A topological space $X$ is path connected if given any two points $a,b \in X$ there's a continuous map $f \colon [0,1] \to X$ where $f(0) = a$ and $f(1) = b$.

#### Separation properties

DEF: A topological space $X$ is $T_0$ (Kolmogorov) if ... for all distinct $x,y \in X$, there's a neighborhood of one of the points not containing the other.

DEF: A topological space $X$ is $T_1$ (Tikhonov) if ... for all distinct $x,y \in X$, there are two neighborhoods $U, V$ such that both $U\ni x$ with $U\not\ni y$ and $V \ni y$ with $V \not\ni x$.

DEF: A topological space $X$ is $T_2$ (Hausdorff) if ... for all distinct $x,y \in X$, there are two neighborhoods of $U\ni x$ and $V \ni y$  such that $U \cap V = \emptyset$.

EX: The lower ray topology on $\RR$ has Trennungsaxiom ... $T_0$ and not $T_1$.

EX: Line with two origins $\RR\times\{0,1\}/\sim$ has Trennungsaxiom ... $T_1$ and not $T_2$.

THM: (Recognizing Kolmogorov) A space is $T_0$ iff ... for all points $x \neq y$ we have $\Cl{\{x\}} \neq \Cl{\{y\}}$.

THM: (Recognizing Tikhonov) A space is $T_1$ iff ... for all points $x \neq y$ we have $\Cl{\{x\}} = \{x\}$.

THM: (Recognizing Hausdorff) A space $X$ is $T_2$ iff ... the diagonal $\Delta \subset (X \times X, \sT_{\mathrm{PROD}})$ (defined $\Delta = \{(x,x) : x \in X\}$) is closed, i.e., $\Cl{\Delta} = \Delta$.

#### Homeomorphism

TODO 

- define homeomorphism (2018-09-21)
    - necessary and sufficient conditions to check
    - laundry list equivalent definitions
- relate to embeddings in $\RR^n$
    - why can't certain compact non-orientable curves be embedded here?
- state the pasting lemma (see notes from 2018-09-17)

#### New spaces from old: subspaces 

TODO

- inclusions
- universal property?
- behaviour of closure and interior

#### New spaces from old: quotient spaces

TODO

- laundry list the definitions
    - via equivalence relation
    - via surjection
    - just the quotient map
    - (see notes 2018-09-29)
    - (see notes 2018-09-30
- identification topology (see notes 2018-09-19)
- what's the universal property?

- describe "quotienting out" the real line by the $K$-topology.

> Quotienting out $K$ in the $K$-topology [@Mu00, number 22.6]
> 
> Let $Y$ be the quotient space obtained from $\RR_K$ by collapsing the set $K$ to point, with $p \colon \RR_K \to Y$ as the corresponding quotient map.
> 
> (a) $Y$ is $T_1$ but not Hausdorff.
> (b) The map $p \times p \colon \RR_K \times\RR_K \to Y \times Y$ is not a quotient map.^[The diagonal is not closed in $Y \times Y$, but its inverse image is closed in $\RR_K \times \RR_K$.]

### Week 4

TODO (see notes 2018-09-26)

- quotient topology examples
- define the connected sum

TODO (see notes 2018-09-28)

- state classification of compact orientable surfaces
    - e.g., the connected sum of two tori is an $8$ sided polygon with sides $a,b,c,d$ and boundary symbol $aba^{-1}b^{-1}cdc^{-1}d^{-1}$.
- define projective space
- upper hemisphere vs Poincaré disk model for projective space

### Week 6: 

#### Connectedness

From lecture:

- definitions
    - connected
    - path connected
    - local connected 
    - locally path connected

- propositions
    - unions of connected spaces (with nonempty intersection) are connected
    - products of connected spaces are connected
    - connected components are maximal connected subspaces
    - homeomorphisms preserve the number of connected components
    - a set nested between a connected set and its closure is connected
    - path connected implies connected

From [@VINK, chapter III]:

DEF! We say topological space $X$ is connected if ... $X$ has only two subsets that are both open and closed.

PROP! A topological space $X$ is connected iff ... $X$ does not admit a partition into two nonempty open sets; equivalently, $X$ does not admit a partition into two nonempty closed sets.

PROP! Is the closure of a connected set connected? ... yes.

PROP! If $A$ is connected and $B$ is a set such that $A \subset B \subset \Cl{A}$, is $B$ connected? ... yes.

DEF! A connected component of a space $X$ is a ... maximal (with respect to set inclusion) connected subset of $X$.

One can spin out profuse variations these themes, e.g., see notes from 2018-10-07 and 2018-10-09, also [@VINK08, III.12].

DEF! A topological space is totally disconnected if ... all of its components are singletons.

- discrete spaces
- the cantor set
- the rational numbers

PROP! Why is the continuous image of a connected space connected? ... consider the lifts of open sets and argue by contradiction.

CORO! The number of connected components is ... a topological invariant.

Other directions

- *Connectedness on the real line* [@VINK08, III.12]
    - The interval $I = [0,1]$ is connected.
    - Every open subset of the real line is a union of disjoint open intervals.
    - Every open set in $\RR$ has countably many connected components.
    - Convex sets are connected.
    - The $n$-sphere is connected for $n \ge 1$.
    - and so on...
- *Applications*
    - With $X$ be a connected space, $f \colon X \to \RR$ a continuous function, the image $f(X)$ is an interval of $\RR$.
    - $\RR^1$ and $\RR^n$ are not homeomorphic for $n > 1$
    - path connected as in homotopy
    - cut points readily prevent two spaces from being homeomorphic

See also

- Dimension Theory and Separation Theorems, A History of Algebraic and Differential Topology, 1900-1969 by J. Dieudonné, Birkhäuser (1989) <https://www.maths.ed.ac.uk/~v1ranick/jordan/dieujord.pdf>
- <https://terrytao.wordpress.com/2011/06/13/brouwers-fixed-point-and-invariance-of-domain-theorems-and-hilberts-fifth-problem/>
- [“Space-filling curve”](https://en.wikipedia.org/wiki/Space-filling_curve#The_Hahn%E2%80%93Mazurkiewicz_theorem). English Wikipedia. Retrieved October 23, 2018.

### Week 7: review for midterm

- position of a point with respect to a set [@VINK08, I.6]
    - closure
    - interior
    - boundary
    - exterior
    - limit/adherent points
    - dense/nowhere dense sets

PROP! A set is everywhere dense in a space iff it meets ... each nonempty open set.

PROP! A space $X$ is discrete iff it contains a unique ... everywhere dense set, namely $X$ itself.

DEF! We say a set $A$ is nowhere dense in a space $X$ when ... its exterior is everywhere dense.

PROP! A set $A$ is nowhere dense in $X$ iff ... each neighborhood of each point $x \in X$ contains a point $y \in X \setminus A$ such that there's a neighborhood $U \ni y$ for which $U \cap A = \emptyset$.

EX! $\RR$ is not the union of countably many ... nowhere dense subsets.

EX! A countable intersection of open everywhere dense sets in $\RR$ is ... everywhere dense.

EX! $\QQ$ is not the intersection of countably many ... open sets in $\RR$.

#### Images, preimages, etc

Took a set theoretic digression through [@VINK08, II.9]

PROP: $f(f^{-1}(B)) = B$ iff ... $B \subset \Im f$.

PROP: $f^{-1}(f(A)) = A$ iff ... $f(A) \cap f(X\setminus A) = \emptyset$.

PROP: Let $g \circ f$ be bijective. It's not necessarily true that $f$ or $g$ is bijective. Though ... $f$ must be injective and $g$ must be surjective.

DEF: If $A \subset X$ and $B \subset Y$, then for every $f \colon X \to Y$ such that $f(A) \subset B$, we call $A \xrightarrow{?} B$ mapping $x \mapsto f(x)$ ... $\mathrm{ab}(f)  = f\vert_{A,B}$, the abbreviation, or submap, of $f$ to $A$ and $B$.

DEF: If $A \subset X$ and $f \colon X \to Y$, the restriction of $f$ to $A$ is ... the abbreviation $A \xrightarrow{\mathrm{ab}(f)} Y$, denoted $f\vert_A$.

PROP: The restriction of a map $f \colon X \to Y$ to $A \subset X$ is just the composition ... $A \hookrightarrow X \xrightarrow{f} Y$.

PROP: Any submap of an injection is ... injective.

PROP: If a map possesses a surjective restriction, then it is ... surjective.

See also

- [“image in nLab”](https://ncatlab.org/nlab/show/image). 
- [“preimage in nLab”](https://ncatlab.org/nlab/show/preimage). 
- [“inverse image in nLab”](https://ncatlab.org/nlab/show/inverse+image). 

#### On the construction of sets

Here's a quick constellation from Emily Riehl's [On the construction of new topological spaces from existing ones](http://math.jhu.edu/~eriehl/topologies.pdf). Let $f \colon X \to Y$ be a function.

- "coarse"

    - define a topology on $X$ such that it's the coarsest topology so that $f$ is continuous
    - a sub-basis in $X$ is given by inverse images of open sets in $Y$
    - a function $W \to X$ is continuous iff the composite function $W \to Y$ is continuous

- "fine"

    - define a topology on $Y$ be asking that it's the finest so that $f$ is continuous
    - a subset of $Y$ is open iff its preimage in $X$ is open
    - a function $Y \to Z$ is continuous iff the composite $X \to Z$ is continuous

- constructions

    - disjoint unions (coproducts)
    - products
    - subsets
    - quotients
    - gluings (pushouts)
    - fibre products (pullbacks)

On 2018-10-19, we started a [review group](https://github.com/coltongrainger/fy19top1/blob/master/review-group.md)!

#### The Hausdorff condition

Another perspective on separation properties [@Su75, chapter 4]. What's the Hausdorff condition? 

DEF: A topological space satisfies the Hausdorff condition if ... given any two distinct points $x$ and $y$ in $T$ there exist disjoint open subsets $U, V$ of $T$ containing $x$ and $y$ respectively.

PROP: In a Hausdorff space, any given convergent sequence has ... a unique limit.

WARNING: A quotient space of a Hausdorff space ... may not be Hausdorff.

DEF: A topological space is regular if ... given any closed subset $V$ and $x$ in $T\setminus V$, there're disjoint open subsets separating $V$ and $x$.

For normal spaces, here's fine: <https://en.wikipedia.org/wiki/Normal_space>.

DEF: A topological space is normal if ... given two disjoint closed subsets $E$ and $F$, there are neighborhoods $U$ of $E$ and $V$ of $F$ that are also disjoint.

### Week 9: compactness

We defined compactness

- with open covers
- with closed sets having empty intersection 
- with closed sets having the finite intersection property

To list basic examples

- $\RR$ is not compact.
- Any topological space with the finite complement topology is compact.
- Any topological space with a finite topology $\abs{\sT} < \infty$ is compact.
- If $(X, \sT)$ is compact and $\sT \subset \Sigma$, then $(X, \Sigma)$ is compact too.

PROP! If $X$ is compact and $F \subset X$ is closed, then ... $F$ as a subspace is also compact.

We have the partial converse.

PROP! If $X$ is a Hausdorff topological space and $F \subset X$ is a compact subset, then ... $F$ is closed in $X$.

Apparently "compact Hausdorff" (abbreviated CH) is a desirable property of a topological space (though compactness is not hereditary!). For example,

PROP! If $X$ is a compact Hausdorff space, then ... $X$ is regular ($T_3$).

*Key idea.* In a compact Hausdorff space, a subset $F$ is closed iff it's compact.

PROP! The continuous image $f(X)$ of a compact space $X$ is ... compact.

Albeit that compactness is not a hereditary property, compactness is

- preserved under passage to a *closed* subspace
- preserved by homeomorphism.

CORO! A continuous bijection of a compact space onto a Hausdorff space is a homeomorphism.

> We're really only considering the category of topological spaces modulo homeomorphism equivalence.

On the other hand, Lindelöf is a hereditary property.

DEF! A Lindel\"of space is ... a space in which every open cover has a countable subcover.

Further directions for compactness.

- define [filters](https://proofwiki.org/wiki/Definition:Filter_on_Set), [ultra-filters](https://proofwiki.org/wiki/Definition:Ultrafilter_on_Set)
- state the [ultrafilter lemma](https://en.wikipedia.org/wiki/Boolean_prime_ideal_theorem#The_ultrafilter_lemma)
- prove [Alexander's subbase theorem](https://en.wikipedia.org/wiki/Subbase#Alexander_subbase_theorem)
- prove [Tychonoff's theorem](https://en.wikipedia.org/wiki/Tychonoff%27s_theorem)

#### Revisiting metric spaces

Consider the following equivalences for a subset $C \subset \RR^n$.

- $C$ is closed and bounded.
- Every sequence in $C$ has subsequence that converges to a point in $C$.
- Every infinite subset of $C$ has an accumulation point.
- $C$ is compact.

What of the above result carries over to arguments in metric spaces? 

- In a metric space a set is compact iff it's closed and bounded. 

    - One needs to define the *diameter* of a set for this claim to make any sense.
    - Alternatively, a *metric space itself* is compact iff it's complete and totally bounded.

In a metric space, we recover intuition from analysis.

- We get familiar definitions.

    - completeness
    - boundedness
    - uniform continuity

- We're permitted to make arguments with open balls and closed disks.
- Moreover, we have (at least three) useful implications [@St78, section 5]:

    - A metric space is compact iff it's sequentially compact (aka limit point compact).
    - A metric space is separable iff it's second countable iff it's Lindelöf.
    - A compact subset of a metric space has a countably dense subset.

The difficulty is not in generating topological spaces given a metric, but rather in determining when an existing space is *metrizable*.

DEF! We say two distance functions $d$ and $d'$ are equivalent on a set $X$ when ... there exist $c, c' > 0$ such that for all $x, y \in X$ we've $$c\cdot d(x,y) \le d'(x,y) \le c'\cdot d(x,y).$$

PROP! If two distance functions $d$ and $d'$ on a set $X$ are equivalent, then $d$ and $d'$ induce ... the same topology on $X$.

Further directions in metrization theory.

- [metrizability is a topological property?](https://math.stackexchange.com/questions/320942/metrizability-is-a-topological-property)
- [“Metrization theorem - Wikipedia”](https://en.wikipedia.org/wiki/Metrization_theorem). English Wikipedia. Retrieved November 3, 2018.

    - Urysohn's sufficient condition
    - [Nagata-Smirnov Metrization theorem](https://en.wikipedia.org/wiki/Nagata%E2%80%93Smirnov_metrization_theorem)
    - [Bing's version](https://en.wikipedia.org/wiki/Bing_metrization_theorem)

CORO! A compact Hausdorff space is metrizable iff ... it's second-countable.

### Week 9: Wrapping up point-set

#### Countability

- first countability
- second countability
- Lindelöf
