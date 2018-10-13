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

### Week 0: preliminaries

EX: The Ur monoid on a non-trivial set $S$ is ... the set of transformations of $S$ into itself, with composition of functions as the binary operation.

EX: The Ur group on a non-trivial set $T$ is ... the set of automorphisms $\mathrm{Sym}(T)$ (bijections from $T$ to itself) with composition of functions as the binary operation.

\providecommand{\RR}{\mathbf{R}}

EX: $GL_n(\RR)$ is a subgroup, properly contained in ... $\mathrm{Sym}(\RR^n)$.

> You cannot learn too much linear algebra!

EX: What is the order of the permutation group on $n$ letters? ... $S_n$ is a finite group with order $n!$.

> I recommend you never write out multiplication tables when reasoning through the problem will do.

FACT: The multiplication table of an Abelian group with $n$ elements is (what type of matrix)? ... symmetric.

\providecommand{\ZZ}{\mathbf{Z}}

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

EX: What's a homomorphism from $GL_n(\RR) \to \RR^\times = (\RR \setminus \{0\})$? ... the determinant, since it's well defined and $\det(AB) = \det(A) + \det(B)$.

> Show that there exists a bijection from $GL_n(\RR)$ to $\RR^\times$. Show that such a bijection is certainly *not* a isomorphism.

DEF: Write the factorial $n!$ in two ways, explicitly and inductively. ... Explicitly (or imperatively) $n: = 1 \cdot 2 \cdot 3 \cdots (n-1) \cdot n$, inductively (or recursively) $n: = n(n-1)!$ for $n > 1$ and $1: = 1$.

### Week 1: group axioms and examples

Course with Nat Thiem. Still haven't hammered out the bibliography. Maybe: 

- Artin
- Hungerford
- Dummit and Foote
- R. Vakil 
- E. Riehl

I created a repo for sage projects and assignments at <http://github.com/coltongrainger/fy19alg1>.

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

\providecommand{\FF}{\mathbf{F}}

DEF: (Naive) A vector space $V$ over a field $\FF$ is a set with functions $+ \colon V \times V \to V$ and $\cdot \colon \FF \times V \to V$ such that ... $V$ is an abelian group under vector addition $+$, and the distributive law holds for scalar multiplication $\cdot$ across addition $+$.

\providecommand{\phi}{\varphi}

DEF: (Naive) A vector space homomorphism $\phi \colon V \to U$, also known as a linear transformation, is a function that ... respects scalar multiplication and vector addition.

DEF: A group is a set $G$ with a function $\cdot \colon G \times G \to G$ such that ... the binary operation $\cdot$ is (finitely) associative, there's a (unique) identity element $1 \in G$ such that $g1= 1g = g$ for all $g \in G$, and for each $g \in G$ there's a (unique) $g^{-1}$ where $gg^{-1} = g^{-1}g =1$. 

DEF: A group homomorphism from the group $(G, \cdot)$ to the group $(H, \circ)$ is a function ... respecting the binary operation on $G$ and $H$, that is, for all $a,b \in G$, we have $\phi(ab) = \phi(a) \circ \phi(b)$.

\providecommand{\KK}{\mathbf{K}}

DEF: (Naive) A ring $\KK$ is a set with functions $+ \colon \KK \times \KK \to \KK$ and $\cdot \colon \KK \times \KK \to \KK$ such that ... $\KK$ is an abelian group under addition $+$ (with identity $0$), $\KK \setminus \{0\}$ is an abelian group under multiplication $\cdot$, and both multiplication and addition distribute across each other.

DEF: (Naive) A ring homomorphism $\phi \colon R \to K$  is a function that ... respecting both multiplication and addition for all elements.

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

#### Basic framework for category theory

\providecommand{\sC}{\mathscr{C}}

Notes from [@Ja84, chapter 1].

DEF: To define a category, we need  a class of objects, call it $\sC$ (containing capital letters), with two functions satisfying ... (CL1) One function assigns to each pair $(X,Y)$ of objects of $\sC$ a set $\hom(X,Y)$, an element of which is a morphism from $X$ to $Y$, written $X\xrightarrow{f} Y$; (CL2) the other function assigns to each triple $(X,Y,Z)$ of objects of $\sC$ an operation $\hom(Y,Z) \times \hom(X,Y) \to \hom(X,Z)$ called composition.

\providecommand{\id}{\mathrm{id}}

DEF: To suppose we have a class $\sC$ with a morphism and composition assigning functions. The class $\sC$ is a category if the following conditions hold. ... (CL1) if $X\xrightarrow{f}Y\xrightarrow{g}Z\xrightarrow{h}W$ are morphisms of $\sC$, then composition of morphisms is associative $(h \circ g) \circ f = h \circ (g \circ f)$; (CT2) for each object $X$ of $\sC$ there's a morphism $\id_{X}\colon X \to X$ such that $\id_X \circ f = f$ and $g\circ \id_X = g$ for each morphism $f$ and $g$ on the appropriate domains.

DEF:  A monoid is a category ... with precisely one object.

DEF:  A groupoid is a category ... where all morphisms are equivalences.

EX: Let $G$ be a group and $H$ a subgroup. Then a groupoid is defined in which the objects and morphisms are respectively ... (objects) the right cosets $Hx$ of $H$ in $G$ and (morphisms from $Hx$ to $Hy$) the elements $g \in G$ such that $Hxg = Hy$ where the composition of morphisms is given by the binary operation of $G$.

In context, consider a category $\sC$. For each object $X$ of $\sC$ the set $\mathrm{end}(X) = \hom(X,X)$ forms a monoid under composition, while the set $\mathrm{aut}(X) \subset \mathrm{end}(X)$ of equivalences of $X$ with itself forms a groupoid.

#### Monoids and groups

Notes from [@Ja85, chapter 1].

DEF: A monoid is ... a set $M$ with an associative binary composition and a unit.

Formally, we say that a monoid is a triple $(M, p, 1)$ in which $M$ is a non-vacuous set, $p$ is an associative binary composition in $M$ and $1$ is an element of $M$ such that $p(a,1) = p(1,a) = a$ for all $a \in M$. 

- Without the associativity of $p$, we obtain a system known as a *monad*. 
- Without the unit $1$, we obtain a *semigroup* ($M$,$p$).

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

#### Modular arithmetic

\providecommand{\NN}{\mathbf{N}}

We work from two intuitive examples: the additive group $\ZZ/n\ZZ$ of integers modulo $n \in \NN$ and the multiplicative group of units in $\ZZ/n\ZZ$. We need to define *residue classes* of integers as the elements in each group.

DEF: (Modulo $n$ equivalence relation) Let $n \in \NN$ be fixed. Define an equivalence relation on $\ZZ$ by ... $a \sim b$ iff $n$ divides $b-a$ iff there's a $m \in \ZZ$ such that $nm = b-a$.

DEF: (Modulo $n$ equivalence classes) For any $k \in \ZZ$ the equivalence class of $a$ is denoted $\overline{a}$, and defined ... $\overline{a} = \{a+kn : k \in \ZZ\}$.

DEF: (Integers modulo $n$) $\ZZ/n\ZZ$ is the set ... $\{\overline{0}, \ldots, \overline{n-1}\}$

DEF: The lease residue of an integer $a$ is ... the smallest non-negative integer congruent to $a$, to find such an integer we say we are reducing $a$ modulo $n$.

DEF: For residue classes $\overline{a},\overline{b} \in \ZZ/n\ZZ$, define their sum and product as ... $\overline{a}+\overline{b} = \overline{a + b}$ and $\overline{a}\cdot\overline{b} = \overline{a\cdot b}$. Both binary operations rely on a choice of representative integers from $\overline{a}$ and $\overline{b}$, but regardless of the choice, the operations are both well defined.

DEF: The multiplicative group of integers modulo $n$, denoted $(\ZZ/n\ZZ)^\times$, is defined as ... $\{\overline{a} \in \ZZ/n\ZZ : \exists \overline{c} \in \ZZ/n\ZZ \text{ with } \overline{a}\cdot\overline{c} = \overline{1}\}$.

PROP: Alternatively $(\ZZ/n\ZZ)^\times$ is the set ... $\{\overline{a} \in \ZZ/n\ZZ : \mathrm{gcd}(a,n) = 1\}$.

EX: How many elements are in $(\ZZ/n\ZZ)^\times$ for an arbitrary $n\in\NN$? ... Consider the Euler totient function $\phi$, defined for each natural number $n$ as the number of positive integers $a \leq n$ with $a$ relatively prime to $n$.

#### Naive generators and relations 

DEF: A subset $S$ of $G$ with the property that every element of $G$ can be written as a (finite) product of elements of $S$ and their inverses is called a set of ... generators of $G$.

NOTATION: We write $\langle S \rangle = G$ to indicate that ... the set of elements $S$ generates the group $G$; or that $G$ is generated by finite products of elements in $S$.

EX: $\ZZ$ in terms of generators is ... $\langle 1 \rangle$

EX: $D_{2n}$ in terms of generators is ... $\langle r, s\rangle$

In a finite group $G$, the set $S$ generates $G$ if every element of $G$ is a finite product of elements of $S$ (that is, excluding inverses of elements in $S$).

DEF: Any equations in a general group $G$ that the generators $S$ satisfy are called ... relations in $G$.

EX: In $D_{2n}$ we have the (minimal) relations ... $r^n = s^2 = 1$ and $rs = sr^{-1}$.

We aim to write relations as tersely as possible, such that any additional relations can be derived from those given.

#### Subgroups

DEF: Where $G$ is a group, a subset $H\subset G$ is a subgroup if and only if .. (S1) $1\in H$; (S2) $h \in H \implies h^{-1} \in H$; (S3) $g,h \in H \implies gh \in H$ where the binary operation is from $\cdot\colon G\times G \to G$.

Alternatively, we might think that a subset $H\subset G$ is a subgroup iff $H$ is a group under the operation of $G$, but it's trouble to define "under the operation".

THM: (Subgroup criterion) The subset $H$ of $G$ is a subgroup iff ... for each $g,h \in H$, we have $gh^{-1} \in H$.

DEF: Let $A \subset G$. The subgroup $\langle A \rangle$ generated by $A$ is ... the unique subgroup of $G$ containing $A$ such that every subgroup of $G$ containing $A$ also contains $\langle A \rangle$.

We think of $\langle A \rangle$ as the "smallest" subgroup containing $A$, or, the subgroup that's the minimal element in the poset of subgroups containing $A$ under the relation set inclusion.

EX: (Cyclic subgroup generated by an element) Let $G$ be a group and take $g\in G$. Then $\langle g \rangle :=$ ... $\{g^n : n \in \ZZ\}$.

DEF: The order $\langle g \rangle$ of an element $g \in G$ ... is the size of the subgroup $\langle g \rangle$.

DEF: A group $G$ is cyclic iff ... there's a $g \in G$ such that $G = \langle g \rangle$.

\providecommand{\CC}{\mathbf{C}}

EX: Suppose $x$ is an nth root of unity in $\CC$. Then $C_n :=$ ... $\{1,x,x^2,\ldots,x^{n-1}\}$ with the usual product in $\CC$. Note $C_n = \langle x \rangle$.

DEF: The dihedral group $D_{2n}$ is the subgroup of $S_{C_n}$ given by ... $$D_{2n} = \left\{w \in S_{C_n} : w(x^j) = x^k \text{ implies } w(x^{j+1}) \in \{x^{k+1},x^{k-1}\}\right\}.$$

For convention, we define $r, s \in D_{2n}$ by $r(x^j) = x\cdot x^j$ and $s(x^j) = x^{-j}$. In terms of generators, if $w \in D_{2n}$, then either

- $(w(1), w(x)) = (x^k, x^{k+1})$ whence $w=r^k$, or 
- $(w(1), w(x)) = (x^k, x^{k-1})$ whence $w=r^ks$.

We see that $D_{2n} = \langle r,s \rangle$.

TODO: Represent $\CC$ as a subset of $GL_2(\RR)$ defined by $$\left\{\begin{pmatrix} a & b \\ -b & a \end{pmatrix} : a,b \in \RR\right\}$$
and show that it is "[outer automorphic](https://en.wikipedia.org/wiki/Outer_automorphism_group)". To what?

DEF: A subgroup $M$ of a group $G$ is called a *maximal subgroup* if $M \neq G$ and ... the only subgroups of $G$ which contain $M$ are $M$ itself and $G$.

#### Review

I sort of scurried around between books and didn't really make a lot of head-a-way in Dummit and Foote. I ended up putting myself squarely one week behind in the reading. However, I was pleased to have at least warmed up with Benedict Gross's lectures and Margaret Morrow's JIBLM notes.

### Week 2: group homomorphisms and actions

#### Homomorphisms and isomorphisms

\providecommand{\abs}[1]{\left\lvert #1 \right\rvert}

We should have a notion of "sameness" sufficient to classify 

1. $C_n$ as $\ZZ/n\ZZ$
2. $S_{\abs{A}}$ as $S_A$
3. with $A \subset B$, relating $S_A$ to $S_B$
4. with $n$ coins in a stack, relating the symmetries of the stack to the permutations of the coins
  - there's a natural surjection from the symmetries to the permutation group $S_n$
  - there's also a natural injection---what?

DEF: A group homomorphism $\phi \colon G \to H$ from a group $G$ to a group $H$ is a function such that $\phi(ab) = \phi(a)\phi(b)$ for all $a,b \in G$.

PROP: (Structure properties) For the homomorphism $\phi \colon g \to h$, we have ... (1) $\phi(1) = 1$; (2) $\phi(g^{-1}) = \phi(g)^{-1}$ for all $g \in G$; (3) $\phi(G) \subset H$ and $\ker(\phi) \subset G$ are subgroups.

DEF: The image $\phi(G)$ of a homomorphism $\phi \colon G \to H$ is (also show it's a group) ... the set $\{\phi(g) : \text{ for all } g \in G\}$; it's a subgroup of $H$ by the criterion, for each $\phi(a), \phi(b)$ we have $\phi(a)\phi(b)^{-1} = \phi(ab^{-2}) \in \phi(G)$.

DEF: The kernel $\ker(\phi)$ of a homomorphism $\phi \colon g \to h$ is (show also it's a group) ... the inverse image of the identity in $H$, i.e., $\phi^{-1}(e_h)$; it's a subgroup of $G$ by the criterion, for each $a,b \in \ker(\phi)$, the image $\phi(ab^{-1}) = \phi(a)\phi(b)^{-1} = 1\cdot1^{-1} = 1$, whence $ab^{-1} \in \ker(\phi)$.

DEF: An isomorphism $\phi\colon G \to H$ is a (quick!) ... bijective homomorphism. 

If such an isomorphism exists, we say that $G$ and $H$ are isomorphic and write $G \cong H$. For example, 

- if $G$ is a cyclic group of order $n$, then $G \cong \ZZ/n\ZZ$;
- if $G$ is a cyclic group of infinite order, then $G \cong \ZZ$.

THM: Let $A$ be a finite set of $n$ elements. Then there exists a (non-canonical) isomorphism from $S_n$ to $S_A$ defined by ... $$\phi:S_n \to S_A \text{ where } w\mapsto \text{ the permutation } \phi(w)\colon A\to A \text{ which sends } a_j \to a_{w(j)}.$$

TODO: Find $D_{2n} \in S_{C_n}$.

Coming up, group actions!

#### Examples of homomorphisms and isomorphisms

Reading from [@DF04, chapter 1.6].

\providecommand{\sG}{\mathscr{G}}
\providecommand{\sP}{\mathscr{P}}

- We have $G \cong G$ perhaps with many isomorphisms.
- With $\sG$ any nonempty collection of groups, isomorphism $\cong$ is an equivalence relation on $\sG$.

IDEA: Classification theorems set out (naively) ... to prove that if $G$ is an object some structure and $G$ has property $\sP$ then any other similarly structured object $X$ with property $\sP$ is isomorphic to $G$.

EX: Any non-abelian group of order $6$ is isomorphic ... to $S_3$.

EX: With $\Delta$ and $\Omega$ nonempty sets, $S_\Delta \cong S_\Omega$ iff $\abs{\Delta} = \abs{\Omega}$. Why (in terms of permutations)? ... $\abs{\Delta} = \abs{\Omega}$ implies there's a bijection $\theta \colon \Delta \to \Omega$, from whence we define $\phi\colon S_\Delta \to S_\Omega$ such that if $\sigma(x) = y$ in $\Delta$, then $\phi(\sigma)(\theta(x)) = \theta(y)$ in $\Omega$.

Three criteria for an isomorphism to exist. If $\phi\colon G \to H$ is an isomorphism, then 
1. $\abs{G} = \abs{H}$.
2. $G$ is abelian if and only if $H$ is abelian.
3. For all $x \in G$, $\abs{x} = \abs{\phi(x)}$.

EX: $S_3 \not\cong \ZZ/6\ZZ$ because (quick!) ... $S_3$ is not abelian, but $\ZZ/6\ZZ$ is.

EX: $(\RR\setminus\{0\}, \times) \not\cong (\RR, +)$ because (quick!) ... in $(\RR\setminus\{0\}, \times)$ the element $-1$ has order $2$, but in $(\RR, +)$ no element has order $2$.

#### Group actions

From [@DF04, chapter 1.7].

DEF: A group action of a group $G$ on set $A$ is a map from $G\times A$ to $A$ (written $g\cdot a, \forall g\in G, \forall a\in A$) satisfying ... (GA1) $g\cdot(h\cdot a) = (gh)\cdot a, \forall g,h\in G, \forall a\in A$; (GA2) $1\cdot a$ = $a$ for all $a \in A$.

The idea of "$G$ acting on a set $A$" is that for a fixed $g \in G$, we have a permutation $\sigma_g \colon A \to A$ defined by $a \mapsto g\cdot a$. We might think that a group $G$ acts on a set $A$ if there exists a homomorphism $\phi \colon G \to S_A$. Indeed, the map $\phi \colon G \to S_A$ defined by $g\mapsto \sigma_g$ is a homomorphism because $\phi(gh) = \phi(g)\circ\phi(h)$ for all $g,h \in G$. We formalize this notion in the following proposition.

PROP: $G \times A \to A$ (where elements of the image are written $g\cdot a$) is an action iff $\phi \colon G \to S_A$ is (define and give required condition) ... a homomorphism that maps element of the group $g$ to permutations of the set $\phi(g) \colon A \to A$ such that $\phi(g)$ maps elements of the set $a$ to their images under the group action $g(a)$.

DEF: An action $G\times A \to A$ is trivial if ... $g\cdot a = a$ for all $a \in A$ and all $g \in G$.

DEF: An action $G\times A \to A$ is faithful if ... $g\cdot a = a$ for all $a \in A$ implies $g = 1$. In other words, distinct elements of $G$ induce distinct permutations of $A$.

(Such an action occurs when the associated homomorphism $\phi$ from $G$ to $S_A$ is injective (since then $\ker(\phi) = \{\mathrm{id}\}$).)

\providecommand{\id}{\mathrm{id}}

THM: If $G$ acts faithfully on $A$ then $G \cong H \leq S_A$. (Describe the injection.) ... Let $\phi \colon G \to S_A$ be the corresponding homomorphism. If $\phi(g) = \phi(h)$ then $\id_A = \phi(g)\phi(h)^{-1} = \phi(gh^{-1})$. Since $G$ is faithful, $gh^{-1} =1$, hence $g=h$, hence $\phi$ is injective, and thus an isomorphism.

We have Cayley's theorem, philosophically pleasing, yet useless.

THM: (Cayley's theorem) If $G$ is a group and $\abs{G} = n$ then ... $G \cong H \leq S_n$. That is, every finite group of order $n$ is isomorphic to a subgroup of the group of symmetries on $n$ elements.

To sketch the proof. $G$ acts on $G$ by $G \times G \to G$ where $(g,h) \mapsto g(h) = gh$. The action is faithful ("hyperfaithful") because $gh = h$ implies $g=1$.

Thus $G\cong \phi(G)$ where $\phi$ is the action's associated homomorphism $\phi\colon G \to S_G$, which we've shown is injective. Now $\phi(G) \subset S_G \cong S_n$, from whence we conclude the desired subgroup $\phi(G) \cong (?) \subset S_n$ exists.

EX: $D_{2n} \subset S_{D_{2n}} \cong S_{2n}$. However, $D_{2n}$ already acts faithfully on $\{1,\ldots,n\}$, so $D_{2n} \subset S_n$.

\providecommand{\QQ}{\mathbf{Q}}

EX: Some fields to think about ... $\RR$, $\CC$, $\QQ$, $(\ZZ/p\ZZ)^\times$, $\{\text{units in }(\ZZ/n\ZZ)^\times\}$. Note that $\ZZ$ is not a field.

\providecommand{\FF}{\mathbf{F}}

DEF: ($\FF$-module) A vector space $V$ over a field $\FF$ is a set with functions $+ \colon V \times V \to V$ and $\cdot \colon \FF \times V \to V$ such that ... (V1) $V$ is an abelian group under vector addition $+$; (V2) $\cdot \colon \FF \times V \to V$ gives an action of $\FF^{\times}$ on $V$; (V3) the distributive law holds for scalar multiplication $\cdot$ across addition $+$ and vice versa, i.e., for $r,s \in \FF$ and $u,v \in V$ we have $(r + s)(u + v) = ru + rv + su + sv$.

DEF: An action of a group $G$ on an $\FF$-module $V$ is a function $G\times V \to V$ that maps $(g,v) \mapsto u$ such that ... (M1) $G\times V \to V$ is a group action of $G$ on a set $V$ and (M2) for $g \in G$, $a,b \in F$ and $v,u \in V$ we have $$g(au + bv) = ag(u) + bg(v).$$

EX: (Permuting coordinates) For $\FF^n$ define the action $S_n \times \FF^n \to \FF^n$ by ... $$(\sigma, v) \mapsto \begin{pmatrix} v_{\sigma(1)}\\v_{\sigma(2)}\\\vdots \\v_{\sigma(1)}\end{pmatrix}$$

TODO: What's $\FF^n$?

EX: (General linear action) With $GL_n(\FF)$ the group of invertible $n \times n$ matrices, define the action $GL_n(\FF) \times \FF^n \to \FF^n$ by ... $$(g, v) \mapsto gv \quad (\text{matrix multiplication}).$$

#### Representations

PROP: The vector space $V$ is a $G$-module if and only if ... there exists a homomorphism $G \to GL(V) = \{ \text{invertible linear transf. of $V$}\} \subset S_V$. 

To specify the homomorphism from $GL(V)$ to $S_V$ we need to choose both a *basis set* and an *order of the coordinates*. This leads to representation theory.

- How to represent a group as a set of matrices?
- What are the possible dimensions of such a matrical representation?
- What eigenvalues arise? What traces? u.s.w.

To dispell any mystery surrounding considering permutations as group elements, we have (emphasis added) <https://en.wikipedia.org/wiki/Group_action>:

> A common way of specifying non-canonical actions is to describe a homomorphism $\varphi$ from a group $G$ to the group of symmetries of a set $X$. The action of an element $g \in G$ on a point $x\in X$ *is assumed to be identical to the action of its image* $\varphi (g)\in {\text{Sym}}(X)$ on the point $x$. The homomorphism $\varphi$ is also frequently called the "action" of $G$, since specifying $\varphi$ is equivalent to specifying an action. Thus, if $G$ is a group and $X$ is a set, then an action of $G$ on $X$ may be formally defined as a group homomorphism $\varphi$ from $G$ to the symmetric group of $X$. The action assigns a permutation of $X$ to each element of the group in such a way that:
>
>- the identity element of $G$ is assigned the identity transformation of $X$;
>- any product $gk$ of two elements of $G$ is assigned the composition of the permutations assigned to $g$ and $k$.

DEF: Let $G$ be a group. A permutation representation of $G$ is ... any group homomorphisms into the symmetric group $S_A$ for some nonempty set $A$. Any action of $G$ on $A$ affords or induces the associated permutation representation of $G$.

ANALOGY: The permutation representation of a group action on a set is like ... the matrix representation of a linear transformation.

PROP: Let $G$, a group, act on a nonempty set $A$. The relation on $A$ defined by $a \sim b$ iff [...] for some $g \in G$ is an equivalence relation. ... $a = g(b)$

\providecommand{\Stab}[2]{\mathrm{Stab}_{#1} \left( #2 \right)}

DEF: For each $a \in A$ the number of elements in the equivalence class containing $a$ is $\abs{G : \Stab{G}{a}}$, the index of the stabilizer in $G$.

#### Review

Concepts I struggled with:

- fixed point free automorphisms
- manipulating permutations as group elements 
- distinguishing elements from actions in this case
- *timeliness!*

### Week 3: subgroups through actions

We had a definition quiz on:

- functions
- homomorphisms
- group actions
- commutativity

#### Constructions

Recall if $A \subset G$ is a subset of a group $G$, then $\langle A \rangle$ is the *smallest* subgroup containing $A$ under the partial ordering inclusion.

We can construct $\langle A \rangle$ with $$W(A) = \{ b_1\cdots b_\ell : \ell \in \NN \text{ and } b_1,\ldots,b_n \in A \cup A^{-1}\}.$$

With $G$ a group and $A \subset G$, the words of $A$ coincide with the subgroup generated by $A$. That is, $W(A) = \langle A \rangle = \cup\{H : H \le G, H \supset A\}$.

#### More group actions

In the following definitions, let some group $G$ act on $B$ and fix a subset $A \subset B$. Note $G$ doesn't necessarily act on $A$ since some $g \in G$ could send element out of $A$.


DEF: Let $G$ act on $B$ and fix $A \subset B$. The stabilizer $\Stab{G}{A}$ of $A$ in $G$ is ... the subgroup $\Stab{G}{A} = \{g \in G: g(a) = a, a \in A\}$.

If $\phi \colon G \to S_B$ is the corresponding homomorphism, then $\Stab{G}{A} = \ker(\phi)$, that is, the subgroup of $G$ for which each element fixes every $a \in A$.

- $\Stab{S_n}{\{1, n\}} \cong S_{n-2}$
- Where $x$ is an $n$th root of unity, $\Stab{D_{2n}}{\{x\}} \cong \{1, rsr^{-1}\}$.
- When $G$ acts on itself by left multiplication, $\Stab{G}{A}$ is trivial for all $A \subset G$.

Stabilizers are easy to compute; stable elements are somehow easier to find than the images of every element in $A$.

\newcommand{\Norm}[2]{\mathrm{Norm}_{#1} \left( #2 \right)}

DEF: Let $G$ act on $B$ and fix $A \subset B$. The normalizer $\Norm{G}{A}$ of $A$ in $G$ is ... the subgroup $\Norm{G}{A} = \{g \in G: g(a) \in A, a \in A\}$.

- When $GL_n (\RR)$ acts on $\RR^2$, the normalizer $\Norm{GL_n(\RR)}{\{(x,0) : x \in \RR\}}$ is the subgroup of upper triangular matrices.
- $\Norm{S_n}{\{1,\ldots, n\}} \cong S_{n-2}\times S_2$
- Where, again, $x$ is an $n$th root of unity, $\Norm{D_{2n}}{\{x\}}  = \Stab{D_{2n}}{\{x\}} \cong \{1, rsr^{-1}\}$. Why?

DEF: The conjugation action of a group $G$ on itself is defined as ... the function $G \times G \to G$ which maps $(g,h) \to ghg^{-1}$. We write $g(h) = ghg^{-1}$ for all $g,h \in G$.

- Conjugation is a group action.
- Conjugation is not necessarily faithful.
  - Looking at faithful actions doesn't tell us much about the group.
- It's philosophically similar to changing bases in a vector space
  - Conjugation amounts to shifting a linear transformation without varying the eigenvalues, trace, etc.

DEF: The centralizer $C_G(A)$ of a subset $A \subset G$ is ... the subgroup $\Stab{G}{A}$ where $G$ acts on itself by conjugation.

- Note that when $A = \{g\}$ we have $C_G(A) = C_{G}(\{g\})$ the subgroup of elements $h \in G$ that commute with $g$, since $h = ghg^{-1}$ implies $hg = gh$.
- Idea: conjugation is "measuring commutation".

DEF: The center $Z(G)$ of $G$ is ... the (nonempty, perhaps trivial, definitely abelian) subgroup $Z(G) = C_{G}(G)$ which consists of every element that commutes with all elements of $G$.

- Conjugation is faithful when the center of a group is trivial.
- Conjugation is trivial when the center of a group is the group itself.

DEF: The normalizer $N_G(A)$ of a set $A \subset G$ is the subgroup $\Norm{G}{A}$ where $G$ acts on itself by conjugation.

- $N_G(G) = G$, that is, $G$ is normal in itself.

DEF: (Normalizer definition) A subgroup $H \le G$ is normal in $G$ if ... $\Norm{G}{H} = G$, in which case we write $H \triangleleft G$.

- Since $N_G(Z(G)) = G$, we have $Z(G) \triangleleft G$.

DEF: (Thiem) If $G$ acts on a set $A$, the orbit of $a \in A$ is ... the set $\{g(a) : g \in G\} \subset A$.

When does a group act *transitively* on a set?

- $GL_n(\FF)$ acts transitively on $\FF^n\setminus\{0\}$.
- Both $S_n$ and $D_{2n}$ act transitively on $\{1,\ldots, n\}$.
- $D_{2n}$ does *not* act transitively on $\{(i,j) : 1 \le i \le j\le n, i \neq j\}$. Action by the dihedral group preserves a metric between adjacent elements.

DEF: (Dummit) Let $G$ be a group acting on a nonempty set $A$. The equivalence class $\{g(a) \colon g \in G\}$ is called ... the orbit of $G$ containing $a$.

DEF: The action of $G$ on $A$ is called transitive if ... there's only one orbit, i.e., given any two elements $a,b \in A$, there's some $g \in G$ such that $a = g(b)$.

DEF: A right action of a group $G$ on a set $A$ is a function $$A \times G \to A\\(a,g) \mapsto (ag)$$ such that ... $(a1) = a$ for all $a \in A$ and $(agh) = ((ag)h)$ for all $a \in A$ and $g,h \in G$.

DEF: Let $G$ and $H$ be groups. A biaction of $(G,H)$ on a set $A$ is a function $$G\times A \times H \to A\\(g,a,h) \mapsto (g(a)h)$$ such that ... $(g,a) \mapsto (g(a)1)$ is a left action, $(a,h) \mapsto (1(a)h)$ is a right action, and $((g(a))h) = g(ah)$ for all $g \in G$, $a \in A$, $h \in H$.

DEF: One can convert a biaction of the group pair $(G,H)$ on $A$ to a left action by $G \times H$ on $A$ given by the mapping ... $(g, h, a) \mapsto (g(a)h^{-1})$, (The idea is to multiply by an inverse, or induce another anti-isomorphism that reverses the order of multiplication, e.g., transpose of matrices.)

DEF: Suppose $G$ is a group and $H < G$. Consider the left and right actions of $H$ on $G$. The set of left cosets $G/H$ (respectively right cosets $H \backslash G$) is ... the set of orbits of the right (respectively left) action of $H$ on $G$. 

EX: A typical element of $G/H$ is of the form ... $$gH = \{gh : h \in H\}.$$

CORO: (Lagrange's theorem) Suppose $G$ is a group and $H < G$. Then the order of $H$ divides the order of $G$.

\providecommand{\sS}{\mathscr{S}}

EX: Since membership in cosets is an equivalence relation, we often select a set of coset representatives for a subset $\sS \subset G$ such that ... $\abs{\sS \cap gH} = 1$ for all $g \in G$.

Now braid diagrams represent permutations in $S_n$, and one can consider the set of $S_n / (S_2 \times S_{n-2})$ as a set of concatenated permutations, first an element of $S_n$, then an element of $S_2 \times S_{n-2}$. (It's "philosophically easier" to work with braids rotated by $90^\circ$ counterclockwise, as then the left and right actions *flow* left or right.) How ought we to choose coset representatives from $S_2 \times S_{n-2}$? Suppose we choose to take only minimal crossing representatives. Then to which coset does a braid diagram from $S_n$ belong? Well, can reduce to a minimal crossing representative the braid diagram of an element $\sigma$ in $S_n$ by finding the (unique) element $\tau$ of $S_2 \times S_{n-2}$ for which $\tau\sigma$ has minimal crossings. We imagine the group $S_2 \times S_{n-2}$ as "vacuuming up" as many crossings as possible from $S_n$. 

In this light, row reduction of matrices is essentially picking coset representatives from a biaction. Coming up... Bruhat decomposition!

#### Congruence modulo a subgroup

Derived from [@Hu80, cosets and counting]:

DEF: Let $H$ be a subgroup of $G$, with $a,b \in G$. We say $a$ is right congruent to $b$ modulo $H$ iff ... $ab^{-1} \in H$, written $a \equiv_r b\mod H$.

Now if $G$ is abelian, we've $(ab^{-1}) \in H$ iff $ba^{-1} \in H$ iff $a^{-1}b \in H$ for all $a,b \in H$. Whence left and right congruence modulo $H$ is the same relation. 

THM: Let $H \le G$, groups. Considering the equivalence relation on $G$ given by right congruence modulo $H$, what are the equivalence classes in $G$ (and what are their cardinalities)? ... First, the equivalence class of $a \in G$ under right congruence modulo $H$ is the set $Ha = \{ha : h \in H \}$; second $\abs{Ha} = \abs{H} = \abs{aH}$ (where $aH$ is the equivalence class of $a$ in $G$ by left congruence modulo $H$) for all $a \in G$.

DEF: Let $H \le G$, groups. The index of $H$ in $G$, denoted $\abs{G: H}$ is the cardinal number of the set of distinct ... right (or left) cosets of $H$ in $G$.

PROP: If $K, H, G$ are groups with $K \le H \le G$, then $\abs{G : K} =$ ...  $\abs{G: H} \abs{H : K}$; caveat, if any two of these indices are finite, then so is the third.

#### Counting techniques for finite groups

PROP: Let $H$ and $K$ be finite subgroups of a group $G$. Then $\abs{HK}$ is equal to ... $$\frac{\abs{H}\abs{K}}{\abs{ H \cap K }}$$ where $HK$ is the set (not nec. a group) $\{hk : h \in H, k \in K\}$.

*Proof sketch*.

- $C = H \cap K$ is a subgroup of $K$ of index $n = \abs{K}/\abs{H \cap K}$.
- $K$ is the disjoint union of right cosets $Ck_1 \sqcup Ck_2 \sqcup \ldots \sqcup Ck_n$ for some $k_i \in K$. (Why?)
- Now since $HC =H$, we have $HK$ as the disjoint union $Hk_1 \sqcup Hk_2 \sqcup \ldots \sqcup Hk_n$.
- Thus $\abs{HK} = n \cdot \abs{H} = \frac{\abs{K}\abs{H}}{\abs{H\cap K}}$.

PROP: If $H$ and $K$ are subgroups of $G$, then $\abs{H : H \cap K} \le \abs{G : K}$. Moreover, if $\abs{G : K}$ is finite, then $\abs{H : H \cap K} = \abs{G : K}$ iff .. $G = HK$.

\providecommand{\sA}{\mathscr{A}}
\providecommand{\sB}{\mathscr{B}}

*Proof sketch.*

- Let $\sA$ be the set of all right cosets of $H\cap K$ in $H$ and $\sB$ be the set of all right cosets of $K$ in $G$.
- The map $\phi \colon \sA \to \sB$ given by $(H \cap K)h \mapsto Kh$, for $h \in H$, is well defined since $(H\cap K)h = (H \cap K)h'$ implies $h'h^{-1} \in H\cap K \subset K$, hence $Kh = Kh'$.
- Why is $\phi$ injective?
- Then $\abs{H : H \cap K} = \abs{\sA} \le \abs{\sB} = \abs{G : K}$.
- What if $\abs{G : K}$ is finite and $\phi$ is surjective?

PROP: Let $H$ and $K$ be subgroups of finite index in $G$. Then $\abs{G : H \cap K}$ is finite and $\abs{G : H \cap K}$ is less than or equal to (with equality when) ... $\abs{G : H}\abs{G : K}$ with equality iff $G = HK$.

To specific to cyclic subgroups.

PROP: Let $G$ be a group and $x \in G$ and $a \in \ZZ\setminus\{0\}$. If $\abs{x} = n < \infty$, then $\abs{x^a}$ is equal to ... $\frac{n}{\gcd(n,a)}$.

Concepts I struggled with: 

- the Heisenberg group of unit upper triangular $3 \times 3$ matrices in $\FF$
- A finite group with no more that two maximal subgroups is cyclic.

### Week 4: quotient groups and isomorphism theorems

#### Progress so far

Consulting Prof Thiem during office hours, we seemed to agree that, of the curriculum, 

- cyclic groups
- permutation groups
- matrix groups
- presentations
- group actions
- lattices
- subgroups
- normal subgroups
- Lagrange’s theorem
- cosets

had been covered so far and 

- group actions *applied*
    - automorphisms
    - conjugation as a group acting on itself
    - quotient groups
- Sylow’s Theorems
- isomorphism theorems

would be coming up in the next 3 weeks.

Ian, Erik, Hunter, and I tried to show that two presentations of a group are isomorphic if we bijectively identify the "correct elements" in each presentation, and show that certain relations in each presentation are satisfied. I felt hand-wavy to talk about an isomorphism of words via letters without having grounded the argument in the *set of reduced words* see [@Hu80, chapter 1.9]. 

I started a [review group](https://github.com/coltongrainger/fy19alg1/blob/master/midterm01-review.md)!

#### Bruhat decomposition

What is [Bruhat decomposition](https://en.wikipedia.org/wiki/Bruhat_decomposition)? 

Let $B$ be the subgroup of upper triangular matrices in $GL_n(\FF)$. We want to choose double coset representatives from the set 
$$B \backslash GL_n(\FF) /B = \{BgB | g \in G\}.$$

Note that elementary matrices in $B$ perform row operations on elements $g \in GL_n(\FF)$. So, given an arbitrary $g \in G$, we choose $b \in B$ to maximize the number of leading $0$'s of the product $bg$. 

But $bg$ might not be in upper triangular (generally, echelon) form, so find a permutation (matrix) $\omega \in S_n \le GL_n(\FF)$ such that $\omega bg \in B$. So $\omega bg = b' \in B$. But then $g = b^{-1}\omega^{-1}b' \in B\omega^{-1}B$, the double coset labelled by an element of the symmetric group.

Are $B \omega B$ and $B \sigma B$ the same if $\omega, \sigma \in S_n$ and $\omega \neq \sigma$?

Suppose $B \omega B$ and $B \nu B$ are equal where $\omega, \nu \in S_n$. Then there are upper triangular matrices $a,b \in B$ such that $\nu = a\omega b$, so $\omega^{-1}a^{-1}\nu \in B$. Here's the idea: the diagonal entries of an upper triangular matrix are unique. Hence if $\omega^{-1}a^{-1} \nu \in B$, then $\omega^{-1}\nu \in B$. Moreover, $\omega^{-1}\nu \in S_n \cap B = \{I\}$ (why?) so $\omega = \nu$.

THM: (Bruhat decomposition) We can write the group of general linear $n \times n$ matrices over the field $\FF$ as ... $$GL_n(\FF) = \bigsqcup_{ \omega \in S_n} B\omega B$$ where $B$ is the set of upper triangular matrices.

1. Bruhat decomposition is the "the right way" to remember row reduction
2. $\abs{B \omega B} \neq \abs{B\nu B}$ when $\FF$ is finite
    - consider $\omega = I$ and $\nu$ as a simple transposition
    - then $\abs{ B \omega B }  = \abs{ B } < \abs{B \nu B}$
    - simple transpositions flip exactly one entry pass the diagonal
3. $PLU$-decomposition is similar, but we need to factor $B$ through $\omega$.

#### Quotient groups

- Suppose $\phi \colon G \to H$ is a surjective homomorphism with kernel $K = \ker(\phi)$. 
- Does $H$ gives a group structure to $G/K$ the left cosets of $K$ in $G$. If so, how? Why?

Consider "pullbacks of images" of elements in $G$, say, for $a$ and $b$. (Alternatively, consider cosets generated by orbits of elements in $G$ under the action of $K$.) Is it true that $\phi^{-1}(\phi(ab))) = \phi^{-1}(\phi(a)))\phi^{-1}(\phi(b)))$? (That $aKbK = abK$?)

- Clearly $abK \subset aK bK$. 
- Conversely, suppose $akbh \in aKbK$. 
- Note $akbh = ab(b^{-1}kb)h$. 
- But $\phi(b^{-1}kb) = \phi(b)^{-1}\phi(k)\phi(b) = \phi(b)^{-1}\phi(b) = 1$.
- Hence $b^{-1}k b \in K$ and $akbh \in abK$.

IDEA: If $G$ is a group with $K < G$ is the operation $(aK)(bK) = abK$ on the quotient structure well-defined? ... (if and) only if $K$ normal in $G$.

THM: Suppose $K$ is a subgroup of $G$. The following are equivalent. (1) $(aK)(bK) = abK$ for all $a,b \in G$ (mid-20th century style) ... (2) $K = \ker(\phi)$ for some group homomorphism $\phi\colon G \to H$.

CORO: If $G$ acts on a set $B$ and $B \subset A$, then the subgroup $\Stab{G}{A}$ is normal in ... $\Norm{G}{A}$.

DEF: Let $N$ be a normal subgroup of the group $G$. The homomorphism $\pi \colon G \to G/N$ defined by $\pi(g) = gN$ is ... the natural projection (or homomorphism) of $G$ onto $G/N$.

DEF: If $\bar{H} \le G/N$ is a subgroup, the complete preimage of $\bar{H}$ in $G$ is the preimage of $\bar{H}$ under the natural projection.

- related to saturated? in topology? in measure theory?

PROP: The complete preimage of a subgroup $\bar{H}$ of $G/N$ contains ... $N$ and itself a subgroup of $G$.

For Monday's review, we listed our favorite equivalences to the statement $N \triangleleft G$, groups.

- The right and left cosets of $N$ in $G$ are precisely the same.
- When $G$ acts on itself by conjugation, $\Norm{G}{N} = G$.

Advice from the book [@DF04, chapter 3.1] for demonstrating normality:

- Avoid computing $gng^{-1}$ for all $n \in N$ and $g \in G$.
- If we have a set of generators, check that the conjugation action by $G$ on $N$ sends the generators to elements in $N$.
- If both the generators for $G$ and $N$ are known, just check the conjugation action on the generators of $N$ by the generators of $G$.
- Can one argue directly (or obliquely) that when $G$ acts on itself by conjugation $\Norm{G}{N} = G$?

#### Products

- Define $HK$ as $H \cdot K$, a subgroup of $G$ iff $HK =KH$.
    - This definition *not unrelated to normal subgroups*. Why?
- Now $HK$ is easy to compute---that's desirable---whereas $\langle H, K\rangle$ is finicky to handle.
    - So when is $HK = \langle H, K \rangle$?
- If $H,K$ are finite subgroups, what's the size of $\abs{HK}$?
    - The strategy here is to prove $HK$ is a subgroup by finding some subgroup of order $\abs{HK} = \abs{H}\abs{K}/\abs{H \cap K}$ that *contains* $HK$. Thereby that subgroup *must be* $HK$.

#### Orbit stabilizer

\providecommand{\Stab}[2]{\mathrm{Stab}_{#1}(#2)}
\providecommand{\Norm}[2]{\mathrm{Norm}_{#1}(#2)}

THM: (Orbit Stabilizer) Let $G$ act on $A$ and fix $a \in A$. Then the orbit containing $a$ has size $\abs{G(a)}$ given by ... $\frac{\abs{G}}{\abs{\Stab{G}{a}}}$ (idea: mod out the elements of $G$ that fix $a$).

*Proof sketch*.

- Consider the group homomorphism $\phi \colon G(a) \to G/\Stab{G}{A}$ such that $g(a) \mapsto g\Stab{G}{A}$.
- Is $\Stab{G}{a}$ is normal in $G$?
- Is $\phi$ well defined?
    - Suppose $g(a) = h(a)$. 
    - Then $a = g^{-1}h(a)$. 
    - So $g^{-1}h \in \Stab{G}{a}$.
    - Taking representatives, $g\Stab{G}{a} = g(g^{-1}h)\Stab{G}{a} = h\Stab{G}{a}$.
- Is $\phi$ injective?
    - Run the previous argument in reverse.
- Is $\phi$ surjective?
    - Note how $\phi$ is defined.

CORO: Give proof that for $H$ and $K$ subgroups of $G$ we have $$\abs{H : K} = \frac{\abs{H}\abs{K}}{\abs{H \cap K}}.$$ ... By orbit stabilizer, $$\abs{H(1\cdot K)} = \frac{\abs{H}}{\Stab{H}{1\cdot K}}$$ where $\Stab{H}{1\cdot K} = \{h \in H: hK = K\} = H \cap K$.

Which combinatorial arguments in finite group theory can be easily proven with the orbit stabilizer theorem? Certainly we find the order of $\abs{HK}$.

combinatorial principle  | group theoretic analogy
-------------------------|------------------------
additive principle       | partitions
multiplicative principle | direct products
orbit stabilizer         | "division"

But now, moreover, we can prove $${n \choose k} = \frac{n!}{k!(n-k)!}.$$ 

- $S_n$ acts on a subset of size $k$ transitively.
  - So there's only one orbit of, e.g., $\{1,\ldots, k\}$.
- The orbit in $S_n$ of a subset of size $k$ has ${n \choose k}$ distinct elements. 
    - Wait, *why?*
- What's $\abs{S_n / \Stab{S_n}{\{a_1,\ldots, a_k\}}}$?
- By Lagrange's theorem, it's $n! / (n-k)!$.
  - How does this argument conclude?

DEF: Subgroups of the symmetric group are called ... permutation groups. 

DEF: For any subgroup $G$ of $S_n$ the orbit of $G$ will refer to its orbits on ... $\{1, \ldots, n\}$. 

DEF: The orbits of an element $\sigma$ in $S_n$ will refer to ... the orbits of the group $\langle \sigma \rangle$ (which are the sets of integers comprising the cycles in its cycle decomposition).

"Dividing in counting is really looking at some kind of stabilization. If we partition $G$ into subsets that send $a$ to the same element, then they're all the same size." 

- How is the orbit stabilizer theorem fundamental (uniquely) to group theory? 
- Why don't we have a similar result in topology for quotient spaces?

#### Isomorphism theorems

THM: (First isomorphism theorem) Let $\phi \colon G \to H$ be a group homomorphism. Then ... $$\phi(G) \cong G/\ker{\phi}.$$

Commutative diagrammatically, where $\pi$ is the natural projection $G \to G/\ker{\phi}$, we have:

```
     \phi
G ---------> H
 \          ^
  \        /
   \      / 
\pi \    /
     \  /
      V/
G mod \ker{\phi}
```

What's the basis strategy in using the first isomorphism theorem?

- Desired: an isomorphism map.
- Find the kernel of some group homomorphism.
- "Mod out" by the kernel.

THM: (Second, or diamond, isomorphism theorem) Let $H, K \le G$ be a subgroup with $H \le \Norm{G}{K}$. Then ... $H \cap K \triangleleft H$ and $H / (H \cap K) \cong ( HK )/K$. (A mouthful without the diagram; key idea: what do $H$ and $K$ generate? where do they meet?)

Hence, the Hasse poset.

```
       G
       |
       |
      H K     (join)
      / \\
     /   \\
    /     \\
   H       K
   \\     /
    \\   /
     \\ /
    H \cap K  (meet)
       |
       |
      {1}
```

Normality gives the quotient group $(HK)/K$. The main result is that $H / (H \cap K) \cong (HK)/K$.

But what's the *commutative* diagram look like?

- How is on to convert a perfectly decent poset into such language?
- Maybe as a "pushout of the diagram"?

THM: (Third isomorphism theorem) Let $H$ and $K$ be normal in $G$ with $K \le H$. Then $H/K \triangleleft G/K$ and ... $\frac{G/K}{H/K} \cong G/H$. (Idea: "invert and cancel".)

*Proof sketch*.

Let $\phi \colon G/K \to G/H$ such that $gK \mapsto gH$. We'll show $\phi$ is a well-defined homomorphism, surjective onto $G/H$, with trivial kernel.

- That $\phi$ is well defined follows from $gK \subset gH$.
- Why is $\phi$ is a homomorphism?
    - Pick two elements $aK$ and $bK$ in $G/K$, apply the homomorphism.
    - Since $H$ is normal in $G$, we have $aHbH = abH = \phi(abK)$.
- That $\phi$ is surjective follows from $gH$ being a union of $gK$ cosets in $G/K$.
- By the first isomorphism theorem, $G/H \cong \frac{G/K}{\ker{\phi}}$.
- Note $\ker{\phi} = \{gK \in G/K : gH = H\} = \{gK \in G/K : g \in H\} = H/K$.

THM: (Fourth, or lattice, isomorphism theorem) Let $\phi \colon G \to H$ be a surjective homomorphism with $K = \ker \phi$ and let $$\mathrm{sbgp}_K(G) = \{ K \subset L \subset G : L \text{ a subgroup}\}$$ $$\mathrm{sbgp}(H) = \{J\subset H : J \text{ a subgroup}\}.$$ Then ... (LT1) the function $\theta \colon \mathrm{sbgp}(G) \to \mathrm{sbgp}(H)$ defined by $$L \mapsto \phi(L)$$ (where also $J \mapsto \phi^{-1}(J) \le K$) is (obvious,) well defined, and a bijection; (LT2) for $A,B \in \mathrm{sbgp}(G)$, $A \triangleleft B$ iff $\theta(A) \triangleleft \theta(B)$ and if $A \triangleleft B$, then $B/A \cong \theta(A)/\theta(B)$; (LT3) for $A, B \in \mathrm{sbgp}(G)$ we have $\theta(A \cap B) = \theta(A) \cap \theta(B)$ and $\theta(\langle A, B\rangle) = \langle \theta(A), \theta(B) \rangle$. Plausible, no?

```   
       \phi
   G --------> H
   ||         ||
   ||         ||
   ||         ||
   ||         ||
\ker\phi ---> {1}

"groupprops transferring over"
```
- From [Richard Green](https://math.colorado.edu/~rmg/): what does the fourth isomorphism theorem say to you?
- Everyone should prove the fourth isomorphism theorem at least one in their life.

*Proof sketch.*

- check $\theta$ is a bijection
- check the homomorphisms
- check that the subgroups contain the kernel

#### Review

Concepts I struggled with:

- orbit stabilizer theorem applied to the symmetric group $S_n$ acting on subsets of size $k$
- applying the isomorphism theorems
    - (from Hunter) *check Aluffi's Chapter 0!*

### Week 5: simple groups and composition series

#### Simple groups

DEF: A group is simple if $N \triangleleft G$ implies $N \in \{\{1\},G\}$.

- simple as in "atomic building blocks" of group theory
- if some group $G$ is not simple we have $N$ a normal, nontrivial, proper subgroup of $G$
    - we then "factor" $G$ into $G/N$ and $N$ 

```
   G---\
   ||  |
   ||  | \cong G/N
   ||  |
   N---<
   ||  |
   ||  | \cong N
   ||  |
   {1}-/
```

- yet the factorization is not necessarily unique
    - (therefore it's not nearly as convenient as prime factorization of natural numbers)

EX: An obvious (abelian) finite simple group is ... the cyclic group $C_p$ when $p$ is prime.

EX: An apparent (non-abelian) finite simple group is ... the alternating group $A_n$ where $A_n \triangleleft S_n$ and $n \ge 5$.

From Martin W. Liebeck [@Go08, number V.7]:

DEF: For an integer $n \ge 2$ and a field $K$, the special linear group $\mathrm{SL}_n(K)$ is ... the set of all $n \times n$ matrices with entries in $K$ and with determinant equal to $1$, together with matrix multiplication as a binary operation. (When $K$ is finite, $\mathrm{SL}_n(K)$ is a finite group.)

- For each prime power $q$, there is up to isomorphism a unique field of order $q$, and the corresponding special linear group in dimension $n$ is denoted $\mathrm{SL}_n(\FF_q)$. 
- These groups are not in general simple, since $Z = \{ \lambda I : \lambda^n = 1\}$, the subgroup of scalar matrices in $\mathrm{SL}_n(\FF_q)$, is a normal subgroup.

EX: The family of projective special linear groups is ... the collection of factor groups $\mathrm{P\mathrm{SL}}_n(\FF_q) = \mathrm{SL}_n(\FF_q)/Z$ where $Z = \{ \lambda I : \lambda^n = 1\}$, which is a family of simple groups expect when $(n,q) = (2,2)$ or $(2,3)$.

- From Chris: Are there any more simple groups as groups modulo the center?
    - Sure, take any simple group and extend it by something that's simple

#### Composition series

How to construct a composition series in the first place?

> "It's really a filtration of $G$ rather than a decomposition of $G$---a way to fill up $G$ rather than breaking it apart."

*Sketch.*

- start with the whole group as maximal in the subgroup lattice
- chip off going down the lattice
    - connections are (anyways already) defined only between groups and their maximal subgroups

*Construction*. Let $G$ be a finite group. Enumerate a sequence of subgroups of $G$ as follows.

- Let $N_0 = G$.
- Let $N_k$ be maximal in $N_{k-1}$ with the property that $N_k \triangleright N_{k-1}$. Now if $N_k ={1}$ we are done. Else repeat this step for $k+1$.

By maximality and the fourth isomorphism theorem, $N_{k-1} / N_l$ is simple, since:

```
                   \pi
        N_{k-1} ---------> N_{k-1}/N_k
         ||                    ||
  no     ||                    ||  neither
normal   ||                    ||  normal
subgps   ||                    ||  subgps
 here    ||                    ||   here 
         ||                    ||
        N_k ----------------> {1}
```

DEF: A composition series of a group $G$ is a sequence $(N_0, N_1, N_2, \ldots, N_r)$ of subgroups such that ... (CS1) $G = N_0 \triangleright N_1 \triangleright \ldots \triangleright N_r = \{1\}$ and (CS2) the factor $N_k / N_{k+1}$ is simple for $0 \le k \le r-1$.

Now the construction (which terminates in a finite number of steps) suffices as proof that a composition series exists for all finite groups (observing each maximal subgroup in the construction has order less than the group it's maximal in).

THM: (Jordan-Hölder) Let $G$ be a group with composition series $(N_0, \ldots, N_r)$ and $(M_0, \ldots, M_s)$. Then ... $r =s$ (e.g., every construction of a composition series of $G$ halts in the same number of steps) and there exists $\omega \in S_{\{0,1,\ldots, r\}}$ such that $N_{\omega(k)}/N_{\omega(k+1)} \cong M_k / M_{k+1}$ for all $0 \le k \le r -1$.

#### Solvable groups

DEF: A group $G$ is solvable if there exists a sequence of subgroups $(N_0, N_1, \ldots, N_r)$ such that ... $G = N_0 \triangleright N_1 \triangleright \ldots \triangleright N_r = \{1\}$ and for each $0 \le k \le r-1$ $N_k/ N_{k+1}$ is abelian.

EX: A solvable subgroup in $\mathrm{GL}_n(\FF)$ is ... the group $B$ of upper triangular matrices. (They're finite solvable of "Lie type".)

DEF: The commutator subgroup $[G, G]$ of $G$ is the subgroup ... generated by elements $ghg^{-1}h^{-1}$. Note the first group where $$\{xyx^{-1}y^{-1} : x,y \in G\} \neq \langle xyx^{-1}y^{-1} : x,y \in G \rangle$$ has order $96$.

Eventually we'll see a relation between nontrivial centers and proper commutators, arising from the construction of lower and upper central series.

PROP: The commutator subgroup $N$ is the smallest group of $G$ such that ... $G/N$ is abelian. 

- This should seem reasonable---we're just "dividing out" all the hairy non-commutative bits.
    - Note conjugation sends the commutator subgroup to itself.

- Solvable groups are somehow orthogonal to simple groups.
    - The only groups both simple and solvable are $(\ZZ/p\ZZ)$ for prime $p$.

PROP: Let $G$ be a group with $N \triangleleft G$. Then $G$ is solvable iff ... $N$ and $G/N$ are solvable.

*Proof sketch*. ($\Leftarrow$) 

- Suppose that $G/N$ is solvable.
    - There's a normal series $$G/N = H_0/N \triangleright H_1/N \triangleright \cdots \triangleright H_n/N = \{1\}.$$
    - Note $( H_i/N )/( H_{i+1}/N)$ is abelian.
- By the lattice (the fourth) isomorphism theorem, we have the "transferred normal series" $$G = H_0N \triangleright H_1N \triangleright \cdots \triangleright H_nN = N.$$
    - Note the subquotients are abelian
        - Why? Take the preimages. They're products.
        - What's $\{1\}/N$ in the lattice isomorphism theorem?
        - Cosets are just a right action by $N$ on some subset $$A/N = \{aN : a \in A\}$$
        - Then the pull back of $A/N$ is $AN$?
- Suppose also that $N$ is solvable. 
    - There's a normal series $$N = M_0 \triangleright M_1 \triangleright \cdots \triangleright M_s = \{1\}.$$
    - Note each subquotient $M_k/M_{k+1}$ is abelian.
    
- We conclude $$G = H_0N \triangleright H_1N \triangleright \cdots \triangleright H_nN = N = M_0 \triangleright M_1 \triangleright \cdots \triangleright M_s = \{1\}.$$


What's our goal here? 

- To find upper and lower central series. 
- Usually we'll want to limit a result to solvable groups then ratchet up. 
- We can readily handle Abelian subgroups en route to a stronger argument.

How to show a group is not solvable? 

- Show a normal with abelian subquotients can't proceed from $G$ to $\{1\}$.

#### Symmetric and alternating groups

DEF: A simple transposition in $S_n$ is a ... $2$-cycle of the form $(i, i+1)$ for $1 \le i \le n-1$. We often write $s_i = (i, i+1)$ to abbreviate.

The simple transpositions give a generating set for $S_n$.

*Proof by example.* Suppose $\sigma \in S_n$ and write $\sigma$ in braid notation. We have a poset on the crossings because the strands never turn back up the braid diagram. We can then pull out the simple transpositions by ordering the crossings on each string. Lo and behold, this method gives us the minimal number of transpositions to use.

DEF! (Sign of a permutation) TODO

DEF! (Discriminant) TODO

- What relation to eigenvalues of the action if $D$ is considered to be a subspace in $\FF[x_1, \ldots, x_n]$?

THM: Let $S_n \to \mathrm{GL}_n(\FF)$ act by left multiplication of permutation matrices. Then for any $\omega \in S_n$, we have $\det(\omega)$ given by ... $\epsilon(\omega)$.

*Proof sketch*. TODO

- what's the determinant of a simple transposition?
    - should be analogous to the *discriminant* of a simple transposition
- generalize to the set of generators of $S_n$

DEF: The alternating group $A_n$ is the subgroup ... $\ker{\epsilon} \triangleleft S_n$, the set of "even permutations", where $\epsilon\colon S_n \to \{-1,1\}$ is the sign function. ($A_n$ is normal for $n \ge 5$.)

- When is the commutator subgroup simple?
    - TODO describe some relation between commutator subgroups and simple groups

THM: Let $G$ be finite and $p$ be the smallest prime dividing the order of $G$. If $H \le G$ satisfies $\abs{G:H} = p$, ... then $H \triangleleft G$.

*Proof sketch*. TODO

#### Review

Concepts I struggled with:

- still about a week behind in the lecture notes
- *timeliness!*
    - With no time to revise the problem set, I glossed over difficult-to-typeset notation I had introduced when sketching up the proofs. My hurriedness cost me clarity, and Thiem didn't really follow the arguments. (F**k! I don't really follow my arguments!)
- Fermat's little theorem
- order of groups and subgroups when factored through a quotient group
    - what relations exist between $\pi(H) < G/N$ and $H < G$?
- specifying *in which group* a subgroup is normal

### Week 6: conjugacy classes and automorphisms

We had a definition quiz on

- bijection
- $S_n$
- cycle
- $\epsilon$

where we were assumed as known

- set (and related accouterments)
- function
- group
- homomorphism
- action
- abelian

Coming up:

- Sylow theory (6th week to 10th week)
- fundamental theorem of abelian groups

#### Conjugacy classes

Definitions from the book [@DF04, chapter 4.3]:

DEF! Two elements $a$ and $b$ are said to be conjugate in $G$ if ... there is some $g \in G$ such that $b = gag^{-1}$ (i.e., iff they are in the same orbit of $G$ acting on itself by conjugation).

- In linear algebra, "conjugate" elements of a $n\times n$ general linear group are said to be *similar*.
- Conjugation by $g$ on $G$ induces an isomorphism (*not unrelated to normality*) --- how?

EX! The conjugacy classes of an abelian group $G$ are given ... $\{\{g\} : g \in G\}$ (analogous to "totally disconnected"?)

DEF! The conjugacy classes of $G$ are ... the orbits of $G$ acting on itself by conjugation.

Cycle decomposition shines when we're handling conjugacy.

LEMMA! Let $w$ and $v$ be permutations in $S_n$. If $w = c_1c_2\cdots c_\ell$ where the $c_i$ are cycles, then $vwv^{-1}$ is given by ... $vc_1v^{-1}vc_2v^{-1}\cdots vc_\ellv^{-1}$.

LEMMA! Let $w$ and $v$ be permutations in $S_n$. If $w = (i_1, i_2, \ldots, i_\ell)$, then $vwv^{-1}$ is given by ... $vwv^{-1} = (v(i_1), v(i_2), \ldots, v(i_\ell))$.

CORO!  Let $w, v \in S_n$ have cycle decompositions $w =  c_1c_2\cdots c_k$  and $v = d_1 d_2 \cdots d_\ell$. Then $w$ and $v$ are conjugate iff ... $k = \ell$ and there exists $\omega \in S_n$ to reorder coordinates such that $$\mathrm{length}(c_{\omega(j)}) = \mathrm{length}(d_j)$$ for all $1 \le j \le \ell$.

- One can express $S_n$ acting on $\mathrm{GL}_n(\FF_q)$ by permutation matrices. 
- I hear $\mathrm{GL}_n(\CC)$ has rad matrix similarity.
- TODO: translate the above corollary for matrix representations.

DEF! An integer partition $\lambda$ of $n$ is a sequence $\lambda = (\lambda_1, \ldots, \lambda_\ell)$ such that ... (IP1) $\lambda_1 \ge \lambda_2 \ge \ldots \ge \lambda_\ell > 0$ and (IP2) $n = \lambda_1 + \lambda_2 + \ldots + \lambda_\ell$.

DEF! The cycle type of a permutation $\omega \in S_n$ is ... the unique integer partition of $n$ obtained by reordering the cycle length of the cycle decomposition of $\omega$ into nonincreasing order (a mouthful, yes).

THM! (Class equation) Let $g_1, g_2, \ldots, g_\ell \in G \ Z(G)$ be representatives for the conjugacy classes not in the center. Then, by orbit stabilizer, the order of $G$ is given by ... $$\abs{Z(G)} + \sum_{j=1}^\ell \frac{\abs{G}}{\abs{C_G(g_j)}}.$$

*Proof sketch.* TODO

- Now the number of elements in the center of $G$ is the number of singleton conjugacy classes.


#### Automorphisms

#### Characteristic subgroups

- the rule of "the"
- Burnside's lemma

### Week 7: Sylow theory
