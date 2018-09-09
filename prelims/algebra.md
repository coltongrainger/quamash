---
title: Algebra for prelims
author: Colton Grainger
date: 2018-08-27
---

## Exam syllabus

### Group theory

- foundations
- canonical examples
    - cyclic groups
    - permutation groups (symmetric and alternating)
    - matrix groups
- lattices
    - subgroups
    - normal subgroups
- automorphisms
- conjugacy
- quotient groups
- direct products
- isomorphism theorems
- Lagrange’s Theorem
    - cosets
- structure of finitely generated abelian groups
- Cauchy’s Theorem
- group actions
    - Cayley’s Theorem
    - G-sets
- the class equation
- Sylow’s Theorems
- the Jordan-Hölder Theorem
- simple groups
- solvable groups
- semidirect products
- free groups
- presentations of groups

###  Ring theory

- foundations
- canonical examples
    - matrix rings
    - polynomial rings
- lattices
    - subrings
    - ideals
- prime and maximal ideals
- quotient rings
- homomorphism theorems
- chain conditions
- rings of fractions
- Chinese remainder theorem
- euclidean domains
- principal ideal domains
- unique factorization domains
- irreducibility criteria
- localization of rings
- field of fractions
- integral ring extensions

### Modules and linear algebra

- foundations
- canonical examples
    - finite dimensional vector spaces
    - linear transformations 
    - matrix representations
- modules
    - lattice of submodules
    - quotient modules
- homomorphism theorems
- structure of finitely generated modules
- language of categories and functors
- minimal polynomial of a transformation
- Cayley-Hamilton theorem over a commutative ring
- direct sums and products
- free, projective, injective modules
- duality
- multilinear forms
- determinants
- canonical forms
    - Jordan
    - rational
    - primary rational
- invariant factors
- elementary divisors
- localization of modules

### Field theory

- foundations
- canonical examples
    - finite fields
- field extensions
    - algebraic
    - transcendental
    - cyclotomic and cyclic
    - transcendence degree
    - algebraic closure
- Greek construction problems
    - impossibility proofs
    - e.g., trisecting angles
- Fundamental theorem of Galois theory
    - Galois correspondence
- splitting fields
    - separability
    - normality
- Galois groups of extensions/polynomials
    - solvable and nilpotent groups
- solvable and radical extensions
    - the insolvability of the quintic
- Fundamental Theorem of Algebra
- Frobenius endomorphism

### Additional Algebra

- applications of Zorn’s lemma
- tensor products
    - algebras
- chain conditions
    - Artinian and Noetherian rings and modules
    - Hilbert basis theorem
- Nullstellensatz

## Fall semester notes



### Week 0

EX: The Ur monoid on a non-trivial set $S$ is ... the set of transformations of $S$ into itself, with composition of functions as the binary operation.

EX: The Ur group on a non-trivial set $T$ is ... the set of automorphisms $\mathrm{Sym}(T)$ (bijections from $T$ to itself) with composition of functions as the binary operation.

\newcommand{\RR}{\mathbf{R}}

EX: $GL_n(\RR)$ is a subgroup, properly contained in ... $\mathrm{Sym}(\RR^n)$.

> You cannot learn too much linear algebra!

EX: What is the order of the permutation group on $n$ letters? ... $S_n$ is a finite group with order $n!$.

> I recommend you never write out multiplication tables when reasoning through the problem will do.

FACT: The multiplication table of an Abelian group with $n$ elements is (what type of matrix)? ... symmetric.

\newcommand{\ZZ}{\mathbf{Z}}

EX: What's the matrical subgroup of $GL_2(\RR)$ that stabilizes the line $y=0$? ... $H = \left\{ \begin{pmatrix}a & b \\ 0 & d\end{pmatrix} : ad \neq 0 \right\}$, since the first basis vector is taken to a scalar multiple of itself!

PROP: The subgroups of $(\ZZ, +)$ are precisely given by ... $(b\ZZ, +)$, where $b$ is a fixed integer.

PROOF: Show that $(b\ZZ, +)$ for any fixed integer $b$ is a subgroup of $(\ZZ,+)$. ... It's closed: $bm + bn = b(m+n)$; inverses exist: $-bm = -b(m)$; the identity is $b0 =0$. 

PROOF: Show that the $(b\ZZ, +)$ for $b \in \ZZ$ exhaust the subgroups of $(\ZZ, +)$. [...] In this latter case, $H$ has $m \neq 0$ and inverses exist, so $H$ has a least positive integer $b > 0$. Then $H \supset b\ZZ$ by closure under addition and inversion. Suppose $h \in H$. Then $h = mb + r$ by the Euclidean algorithm, and $m \in \ZZ$, $0 \leq r < b$. I claim $r=0$. Why? $r = h - mb \in H$ and $r < b$, but $b$ is the least positive element. So $H \subset b\ZZ$. ... If $H$ is a subgroup of $\ZZ$, either $H = \{0\}$ (a subgroup) or $H$ is non-empty. 

<!---
PROOF: Show that the $(b\ZZ, +)$ for $b \in \ZZ$ exhaust the subgroups of $(\ZZ, +)$. If $H$ is a subgroup of $\ZZ$, either $H = \{0\}$ (a subgroup) or $H$ is non-empty. [...] Then $H \supset b\ZZ$ by closure under addition and inversion. Suppose $h \in H$. Then $h = mb + r$ by the Euclidean algorithm, and $m \in \ZZ$, $0 \leq r < b$. I claim $r=0$. Why? $r = h - mb \in H$ and $r < b$, but $b$ is the least positive element. So $H \subset b\ZZ$. ... In this latter case, $H$ has $m \neq 0$ and inverses exist, so $H$ has a least positive integer $b > 0$.

PROOF: Show that the $(b\ZZ, +)$ for $b \in \ZZ$ exhaust the subgroups of $(\ZZ, +)$. If $H$ is a subgroup of $\ZZ$, either $H = \{0\}$ (a subgroup) or $H$ is non-empty. In this latter case, $H$ has $m \neq 0$ and inverses exist, so $H$ has a least positive integer $b > 0$. [...] Then $H \supset b\ZZ$ by closure under addition and inversion. Suppose $h \in H$. Then $h = mb + r$ by the Euclidean algorithm, and $m \in \ZZ$, $0 \leq r < b$. I claim $r=0$. Why? $r = h - mb \in H$ and $r < b$, but $b$ is the least positive element. So $H \subset b\ZZ$. ... Then $H \supset b\ZZ$ by closure under addition and inversion. 

PROOF: Show that the $(b\ZZ, +)$ for $b \in \ZZ$ exhaust the subgroups of $(\ZZ, +)$. If $H$ is a subgroup of $\ZZ$, either $H = \{0\}$ (a subgroup) or $H$ is non-empty. In this latter case, $H$ has $m \neq 0$ and inverses exist, so $H$ has a least positive integer $b > 0$. Then $H \supset b\ZZ$ by closure under addition and inversion. Suppose $h \in H$. [...]  So $H \subset b\ZZ$. ... Then $h = mb + r$ by the Euclidean algorithm, and $m \in \ZZ$, $0 \leq r < b$. I claim $r=0$. Why? $r = h - mb \in H$ and $r < b$, but $b$ is the least positive element. 
--->

THM: The subgroup of $\ZZ$ of the form $$\{ a\ZZ + b\ZZ \} = \{ n \in \ZZ : n = ar + bs \text{ for } r,s \in \ZZ\}$$ is generated by $d$, where $d$ is ... the greatest common divisor of $a$ and $b$.

PROP: Let $a,b \in \ZZ$ both not zero and let $d$ be the positive integer that generates the subgroup $a\ZZ + b\ZZ$. Why can $d$ be written as $ar + bs \text{ for } r,s \in \ZZ$? ... Because $d \in a\ZZ + b\ZZ$.

PROP: Let $a,b \in \ZZ$ both not zero and let $d$ be the positive integer that generates the subgroup $a\ZZ + b\ZZ$. Why does $d$ divide $a$ and $d$? ... Because $a \in d\ZZ$ and $b \in d\ZZ$.

PROP: Let $a,b \in \ZZ$ both not zero and let $d$ be the positive integer that generates the subgroup $a\ZZ + b\ZZ$. Why, if $k$ divides $a$ and $b$, does $k$ also divide $d$? ... Because $a, b \in k\ZZ$, and under closure $ar + bs \in k\ZZ$, alas, $d$ has this form, so $k$ divides $d$.

DEF: A subset $U$ of a group $G$ is said to generate $G$ if every element in $G$ is ... a product of a string of elements (and their inverses) in $U$.

Would be good to see [particular groups of importance](https://groupprops.subwiki.org/wiki/Category:Particular_groups) for further examples. I can't get into a catalog of group properties, and it's seemingly hopeless to memorize.

Ideas for making new groups out of old

- subspaces of a vector space
- cyclic subgroups of a single element
- *products of spaces* correspond to groups, why?

    - automorphism groups $\mathrm{Aut}(G)$
    - in impressionistic language, the "symmetries of $G$"
    - isomorphisms as "structure preserving maps"

One should verify that the inverse of an automorphism is an automorphism.

EX: What's a homomorphism from $\GL_n(\RR) \to \RR^\times = (\RR \setminus \{0\})$? ... the determinant, since it's well defined and $\det(AB) = \det(A) + \det(B)$.

> Show that there exists a bijection from $\GL_n(\RR)$ to $\RR^\times$. Show that such a bijection is certainly *not* a isomorphism.

DEF: Write the factorial $n!$ in two ways, explicitly and inductively. ... Explicitly (or imperatively) $n: = 1 \cdot 2 \cdot 3 \cdots (n-1) \cdot n$, inductively (or recursively) $n: = n(n-1)!$ for $n > 1$ and $1! = 1$.

### Week 1

Course with Nat Thiem. Still haven't hammered out the bibliography. Maybe: 

- Artin
- Hungerford
- Dummit and Foote
- R. Vakil 
- E. Riehl

I created a repo for sage projects and assignments at <http://github.com/coltongrainger/alg1>.

#### What to expect?

1. Axiomatic treatment of fundamental algebraic categories
2. Preparation for half of the examinable material on the prelim
    - chapters 1 to 9 in Dummit and Foote
    - see syllabus
3. Guidance and topic advise for grad school.
4. Evaluations
    - definition quizzes weekly
    - written homeworks weekly
    - three timed exams

#### Categorical perspective

A category is a pair of a collection of so-called objects and a collection of so-called morphisms, where each morphism is associated to a pair of objects such that reasonable properties hold.

EX: In the category of sets, the morphisms are ... functions (set homomorphisms).

EX: In the category of vector spaces, the morphisms are ... linear transformations (vector space homomorphisms).

EX: In the category of groups, the morphisms are ... group homomorphisms.

EX: In the category of rings, the morphisms are ... ring homomorphisms.

\newcommand{\FF}{\mathbf{F}}

DEF: (Naive) A vector space $V$ over a field $\FF$ is a set with functions $+ \colon V \times V \to V$ and $\cdot \colon \FF \times V \to V$ such that ... $V$ is an abelian group under vector addition $+$, and the distributive law holds for scalar multiplication $\cdot$ across addition $+$.

\renewcommand{\phi}{\varphi}

DEF: (Naive) A vector space homomorphism $\phi \colon V \to U$, also known as a linear transformation, is a function that ... respects scalar multiplication and vector addition.

DEF: A group is a set $G$ with a function $\cdot \colon G \times G \to G$ such that ... the binary operation $\cdot$ is (finitely) associative, there's a (unique) identity element $1 \in G$ such that $g1= 1g = g$ for all $g \in G$, and for each $g \in G$ there's a (unique) $g^{-1}$ where $gg^{-1} = g^{-1}g =1$. 

DEF: A group homomorphism from the group $(G, \cdot)$ to the group $(H, \circ)$ is a function ... respecting the binary operation on $G$ and $H$, that is, for all $a,b \in G$, we have $\phi(ab) = \phi(a) \circ \phi(b)$.

\newcommand{\KK}{\mathbf{K}}
\newcommand{\SS}{\mathbf{S}}

DEF: (Naive) A ring $\KK$ is a set with functions $+ \colon \KK \times \KK \to \KK$ and $\cdot \colon \KK \times \KK \to \KK$ such that ... $\KK$ is an abelian group under addition $+$ (with identity $0$), $\KK \setminus \{0\}$ is an abelian group under multiplication $\cdot$, and both multiplication and addition distribute across each other.

DEF: (Naive) A ring homomorphism $\phi \colon \KK \to \SS$  is a function that ... respecting both multiplication and addition for all elements.

What are the benefits to the categorical perspective?

- One works with shared characteristics.
    - Consider just the non-trivial structure on categories and morphisms.
- One generalizes familiar notions.
    - subobjects
    - quotient objects
    - sameness, or isomorphism classes

And what are the costs of such perspective?

- It's not pedagogically ideal.
    - Abstraction is best performed on second or third viewing.
    - Beware the lotus-eaters.
- One sweeps aside the idiosyncracies of groups, rings, etc.

We do our best to state the isomorphism theorems in categorical language.

#### Monoids and groups

Notes from [@Ja85, chapter 1].

DEF: A monoid is ... a set $M$ with an associative binary composition and a unit.

In this light, a group is a monoid each of whose elements has an inverse relative to the unit, and a ring is a pair of monoids with the same underlying set and satisfying additional properties, e.g., distributivity.

DEF: A monoid of transformations is ... a monoid on the set of functions that map some given set $X$ to itself, with composition $\circ$ as a binary operation.

Here's a [Hasse diagram](https://en.wikipedia.org/wiki/Hasse_diagram) for a partially ordering (under inclusion) from the class of monoids to the class of "groups of transformation," i.e., symmetric groups.

```
      monoids
    /         \
groups      monoids of transformations
    \         /
  groups of transformations
```

That is, the class of symmetric groups is precisely the intersection of the class of monoids of transformations with the class of groups. 

To let "composition of functions" be the binary operator underpinning our development of (monoid and) group theory, we had better rigorously define *composite functions*, and show that *composition is associative*.

We take three elementary definitions from Spivak [@Sp94].

RECALL: (Cartesian product style) A function $f$ from the domain set $A$ to the codomain set $B$ is a collection $f$ of ordered pairs in cartesian product $A\times B$ such that ... for each $a \in A$, there's a pair of the form $(a,b) \in f$; and if both $(a,b)$ and $(a,c)$ are in $f$, then $b=c$.

NOTATION: (Domain of a function) If $f$ is a function, the domain of the function is ... the set of all $a$ such If $a$ is in the domain of a function $f$, 

NOTATION: (Value of a function) If $a$ is in the domain of $f$, it follows by the definition of the function that there is ... a unique element $b$ such that $(a,b)$ is in $f$, this unique $b$ is denoted $f(a)$.

DEF: (Composite, resultant, or product of functions.) Let $\alpha \colon S \to T$ and $\beta \colon T \to U$. Then define $\beta \alpha \colon S \to U$ as the map (be rigorous) ... having the domain $S$, the codomain $U$ and graph that's the subset of $S\times U$ containing only $(s, \beta(\alpha(s))$ for each $s \in S$.

When functions factor into products of functions, e.g., if $\beta \alpha = \gamma$, we indicate this relation by saying that some triangle forms a commutative diagram. Likewise, for $\beta\alpha = \delta\gamma$, we say some rectangle is commutative. (Why not higher polygons?)

PROOF: Composition of maps satisfies the associative law. Let $\alpha \colon S \to T$, $\beta \colon T \to U$, and $\gamma \colon U to V$. Clearly $\gamma(\beta\alpha) = (\gamma\beta)\alpha$ because ... both compositions have the same domain $S$, the same codomain $V$, and the same graph $$\left\{\big(s, (\gamma(\beta\alpha))(s) = ((\gamma\beta)\alpha)(s)\big) : s \in S\right\}.$$

#### Equivalence relations, factoring a map

From Jacobson [@Ja85, chapter 0.3]:

One defines binary relations on a set $S$ as any subset of the product $S \times S$.

From Dushnik and Miller [@DM41]:

> By a system is meant a set $S$ together with a binary relation $R(x, y)$ which may hold for certain pairs of elements $x$ and $y$ of $S$. The relation $R (x, y)$ is read "$x$ precedes $y$" and is written "$x < y$".

DEF: An equivalence relation is a binary relation that's ... reflexive, symmetric, and transitive. 

Compare equivalence relations to partial orderings on a set, which are reflexive, *antisymmetric*, and transitive.

Again from [@DM41]:

> A system is called a partial order if the following conditions are satisfied. (1) If $x < y$, then $y\nless x$; and (2) if $x < y$ and $y < z$, then $x < z$. 

Bringing things up to speed, we have Rosoff's [@Ro16] definition:

DEF: (Modern poset) A set $X$ is partially ordered by the relation $\preceq$ if for each $x, y, z \in X$, we have ... (1) reflexivity, $x \preceq x$; (2) antisymmetry, $x \preceq y$ and $y \preceq x$ implies $x =y$; (3) transitivity, $x \preceq y$ and $y \preceq z$ implies $x \preceq z$.

> A partial order defined on a set $S$ is called a linear order if every two distinct elements $x$ and $y$ of $S$ are comparable, i.e., if $x< y$ or $y < x$. If the partial order $P$ and the linear order $L$ are both defined on the same set of elements, and if every ordered pair in $P$ occurs in $L$, then $L$ will be called a linear extension of $P$.

The concept of an equivalence relation is "equivalence" to that of a partition of a set.

DEF: If $S$ is a set we define a partition $\pi(S)$ to be ... a collection of non-vacuous subsets of $S$ (i.e., $\pi(S) \subset 2^S$ and $\emptyset \notin \pi(S)$) such that the blocks constituting $\pi(S)$ have empty pairwise intersection and the union of the collection is equal to $S$.

We can argue that for any partition $\pi$ there's an (natural) equivalence class $E_\pi$, and vice versa, for any $E$ there's a partition $\pi_E$; moreover, the relation between $E$ and $\pi$ is reciprocal in the sense that $\pi_{E_\pi} = \pi$ and $E_{\pi_E} = E$. (Why?)
