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

EX: What's a homomorphism from $GL_n(\RR) \to \RR^\times = (\RR \setminus \{0\})$? ... the determinant, since it's well defined and $\det(AB) = \det(A) + \det(B)$.

> Show that there exists a bijection from $GL_n(\RR)$ to $\RR^\times$. Show that such a bijection is certainly *not* a isomorphism.

DEF: Write the factorial $n!$ in two ways, explicitly and inductively. ... Explicitly (or imperatively) $n: = 1 \cdot 2 \cdot 3 \cdots (n-1) \cdot n$, inductively (or recursively) $n: = n(n-1)!$ for $n > 1$ and $1: = 1$.

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

\newcommand{\sC}{\mathscr{C}}

Notes from [@Ja84, chapter 1].

DEF: To define a category, we need  a class of objects, call it $\sC$ (containing capital letters), with two functions satisfying ... (CL1) One function assigns to each pair $(X,Y)$ of objects of $\sC$ a set $\hom(X,Y)$, an element of which is a morphism from $X$ to $Y$, written $X\xrightarrow{f} Y$; (CL2) the other function assigns to each triple $(X,Y,Z)$ of objects of $\sC$ an operation $\hom(Y,Z) \times \hom(X,Y) \to \hom(X,Z)$ called composition.

\newcommand{\id}{\mathrm{id}}

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

\newcommand{\NN}{\mathbf{N}}

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

\newcommand{\CC}{\mathbf{C}}

EX: Suppose $x$ is an nth root of unity in $\CC$. Then $C_n :=$ ... $\{1,x,x^2,\ldots,x^{n-1}\}$ with the usual product in $\CC$. Note $C_n = \langle x \rangle$.

DEF: The dihedral group $D_{2n}$ is the subgroup of $S_{C_n}$ given by ... $$D_{2n} = \left\{w \in S_{C_n} : w(x^j) = x^k \text{ implies } w(x^{j+1}) \in \{x^{k+1},x^{k-1}\}\right\}.$$

For convention, we define $r, s \in D_{2n}$ by $r(x^j) = x\cdot x^j$ and $s(x^j) = x^{-j}$. In terms of generators, if $w \in D_{2n}$, then either

- $(w(1), w(x)) = (x^k, x^{k+1})$ whence $w=r^k$, or 
- $(w(1), w(x)) = (x^k, x^{k-1})$ whence $w=r^ks$.

We see that $D_{2n} = \langle r,s \rangle$.

TODO: Represent $\CC$ as a subset of $GL_2(\RR)$ defined by $$\left\{\begin{pmatrix} a & b \\ -b & a \end{pmatrix} : a,b \in \RR\right\}$$
and show that it is "[outer automorphic](https://en.wikipedia.org/wiki/Outer_automorphism_group)". To what?


### Week 2

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

\newcommand{\sG}{\mathscr{G}}
\newcommand{\sP}{\mathscr{P}}

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

\newcommand{\id}{\mathrm{id}}

THM: If $G$ acts faithfully on $A$ then $G \cong H \leq S_A$. (Describe the injection.) ... Let $\phi \colon G \to S_A$ be the corresponding homomorphism. If $\phi(g) = \phi(h)$ then $\id_A = \phi(g)\phi(h)^{-1} = \phi(gh^{-1})$. Since $G$ is faithful, $gh^{-1} =1$, hence $g=h$, hence $\phi$ is injective, and thus an isomorphism.

We have Cayley's theorem, philosophically pleasing, yet useless.

THM: (Cayley's theorem) If $G$ is a group and $\abs{G} = n$ then ... $G \cong H \leq S_n$. That is, every finite group of order $n$ is isomorphic to a subgroup of the group of symmetries on $n$ elements.

To sketch the proof. $G$ acts on $G$ by $G \times G \to G$ where $(g,h) \mapsto g(h) = gh$. The action is faithful ("hyperfaithful") because $gh = h$ implies $g=1$.

Thus $G\cong \phi(G)$ where $\phi$ is the action's associated homomorphism $\phi\colon G \to S_G$, which we've shown is injective. Now $\phi(G) \subset S_G \cong S_n$, from whence we conclude the desired subgroup $\phi(G) \cong (?) \subset S_n$ exists.

EX: $D_{2n} \subset S_{D_{2n}} \cong S_{2n}$. However, $D_{2n}$ already acts faithfully on $\{1,\ldots,n\}$, so $D_{2n} \subset S_n$.

\newcommand{\QQ}{\mathbf{Q}}

EX: Some fields to think about ... $\RR$, $\CC$, $\QQ$, $(\ZZ/p\ZZ)^\times$, $\{\text{units in }(\ZZ/n\ZZ)^\times\}$. Note that $\ZZ$ is not a field.

\newcommand{\FF}{\mathbf{F}}

DEF: ($\FF$-module) A vector space $V$ over a field $\FF$ is a set with functions $+ \colon V \times V \to V$ and $\cdot \colon \FF \times V \to V$ such that ... (V1) $V$ is an abelian group under vector addition $+$; (V2) $\cdot \colon \FF \times V \to V$ gives an action of $\FF^{\times}$ on $V$; (V3) the distributive law holds for scalar multiplication $\cdot$ across addition $+$ and vice versa, i.e., for $r,s \in \FF$ and $u,v \in V$ we have $(r + s)(u + v) = ru + rv + su + sv$.

DEF: An action of a group $G$ on an $\FF$-module $V$ is a function $G\times V \to V$ that maps $(g,v) \mapsto u$ such that ... (M1) $G\times V \to V$ is a group action of $G$ on a set $V$ and (M2) for $g \in G$, $a,b \in F$ and $v,u \in V$ we have $$g(au + bv) = ag(u) + bg(v).$$

EX: (Permuting coordinates) For $\FF^n$ define the action $S_n \times \FF^n \to \FF^n$ by ... $$(\sigma, v) \mapsto \begin{pmatrix} v_{\sigma(1)}\\v_{\sigma(2)}\\\vdots \\v_{\sigma(1)}\end{pmatrix}$$

TODO: What's $\FF^n$?

EX: (General linear action) With $GL_n(\FF)$ the group of invertible $n \times n$ matrices, define the action $GL_n(\FF) \times \FF^n \to \FF^n$ by ... $$(g, v) \mapsto gv \quad (\text{matrix multiplication}).$$

#### G-modules

PROP: The vector space $V$ is a $G$-module if and only if ... there exists a homomorphism $G \to GL(V) = \{ \text{invertible linear transf. of $V$}\} \subset S_V$. 

To specify the homomorphism from $GL(V)$ to $S_V$ we need to choose both a *basis set* and an *order of the coordinates*. This leads to representation theory.

- How to represent a group as a set of matrices?
- What are the possible dimensions of such a matrical representation?
- What eigenvalues arise? What traces? u.s.w.

Concepts I struggled with:

- fixed point free automorphisms
- manipulating permutations as group elements 
- distinguishing elements from actions in this case
- *timeliness!*

### Week 3

We had a definition quiz on:

- functions
- homomorphisms
- group actions
- commutativity

#### Constructions

Recall if $A \subset G$ is a subset of a group $G$, then $\langle A \rangle$ is the *smallest* subgroup containing $A$ under the partial ordering inclusion.

We can construct $\langle A \rangle$ with $$W(A) = \{ b_1\cdots b_\ell : \ell \in \NN \text{ and } b_1,\ldots,b_n \in A \cup A^{-1}\}.$$

With $G$ a group and $A \subset G$, the words of $A$ coincide with the subgroup generated by $A$. That is, $W(A) = \langle A \rangle = \cup\{H : H \le G, H \supset A\}$.

#### Group actions

In the following definitions, let some group $G$ act on $B$ and fix a subset $A \subset B$. Note $G$ doesn't necessarily act on $A$ since some $g \in G$ could send element out of $A$.

\newcommand{\Stab}[2]{\mathrm{Stab}_{#1} \left( #2 \right)}

DEF: Let $G$ act on $B$ and fix $A \subset B$. The stabilizer $\Stab{G}{A}$ of $A$ in $G$ is ... the subgroup $\Stab{G}{A} = \{g \in G: g(a) = a, a \in A\}$.

If $\phi \colon G \to S_B$ is the corresponding homomorphism, then $\Stab{G}{A} = \ker(\phi)$, that is, the subgroup of $G$ for which each element fixes every $a \in A$.

- $\Stab{S_n}{\{1, n\}} \cong S_{n-2}$
- Where $x$ is an $n$th root of unity, $\Stab{D_{2n}}{\{x\}} \cong \{1, rsr^{-1}\}$.
- When $G$ acts on itself by left multiplication, $\Stab{G}{A}$ is trivial for all $A \subset G$.

Stabilizers are easy to compute; stable elements are somehow easier to find than the images of every element in $A$.

\newcommand{\Norm}[2]{\mathrm{Norm}_{#1} \left( #2 \right)}

DEF: Let $G$ act on $B$ and fix $A \subset B$. The normalizeer $\Norm{G}{A}$ of $A$ in $G$ is ... the subgroup $\Norm{G}{A} = \{g \in G: g(a) \in A, a \in A\}$.

- When $GL_n (\RR)$ acts on $\RR^2$, the normalizer $\Norm{GL_n(\RR)}{\{(x,0) : x \in \RR\}}$ is the subgroup of upper triangular matrices.
- $\Norm{S_n}{\{1,\ldots, n\}} \cong S_{n-2}\times S_2$
- Where, again, $x$ is an $n$th root of unity, $\Norm{D_{2n}}{\{x\}}  = \Stab{D_{2n}}{\{x\}} \cong \{1, rsr^{-1}\}$. Why?

DEF: The conjugation action of a group $G$ on itself is defined as ... the function $G \times G \to G$ which maps $(g,h) \to gh^g{-1}$. We write $g(h) = ghg^{-1}$ for all $g,h \in G$.

- Conjugation is a group action.
- Conjugation is not necessarily faithful.
  - Looking at faithful actions doesn't tell us much about the group.
- It's philosophically similar to changing bases in a vector space
  - Conjugation amounts to shifting a linear transformation without varying the eigenvalues, trace, etc.

\newcommand{\C}[2]{C_{#1}\left( #2\right)}

DEF: The centralizer $\C{G}{A}$ of a subset $A \subset G$ is ... the subgroup $\Stab{G}{A}$ where $G$ acts on itself by conjugation.

- Note that when $A = \{g\}$ we have $\C{G}{A} = \C{G}{\{g\}}$ the subgroup of elements $h \in G$ that commute with $g$, since $h = ghg^{-1}$ implies $hg = gh$.
- Idea: conjugation is "measuring commutation".

DEF: The center $Z(G)$ of $G$ is ... the (nonempty, perhaps trivial, definitely abelian) subgroup $Z(G) = \C{G}{G}$ which consists of every element that commutes with all elements of $G$.

- Conjugation is faithful when the center of a group is trivial.
- Conjugation is trivial when the center of a group is the group itself.

DEF: The normalizer $N_G(A)$ of a set $A \subset G$ is the subgroup $\Norm{G}{A}$ where $G$ acts on itself by conjugation.

- $N_G(G) = G$, that is, $G$ is normal in itself.

DEF: (Normalizer definition) A subgroup $H \le G$ is normal in $G$ if ... $\Norm{G}{H} = G$, in which case we write $H \triangleleft G$.

- Since $N_G(Z(G)) = G$, we have $Z(G) \triangleleft G$.

DEF! If $G$ acts on a set $A$, the orbit of $a \in A$ is ... the set $\{g(a) : g \in G\} \subset A$.

When does a group act *transitively* on a set?

- $GL_n(\FF)$ acts transitively on $\FF^n\setminus\{0\}$.
- Both $S_n$ and $D_{2n}$ act transitively on $\{1,\ldots, n\}$.
- $D_{2n}$ does *not* act transitively on $\{(i,j) : 1 \le i \le j\le n, i \neq j\}$. Action by the dihedral group preserves a metric between adjacent elements.

DEF! A right action of a group $G$ on a set $A$ is a function $$A \times G \to A\\(a,g) \mapsto (ag)$$ such that ... $(a1) = a$ for all $a \in A$ and $(agh) = ((ag)h)$ for all $a \in A$ and $g,h \in G$.

DEF! Let $G$ and $H$ be groups. A biaction of $(G,H)$ on a set $A$ is a function $$G\times A \times H \to A\\(g,a,h) \mapsto (g(a)h)$$ such that ... $(g,a) \mapsto (g(a)1)$ is a left action, $(a,h) \mapsto (1(a)h)$ is a right action, and $((g(a))h) = g(ah)$ for all $g \in G$, $a \in A$, $h \in H$.

DEF! One can convert a biaction of the group pair $(G,H)$ on $A$ to a left action by $G \times H$ on $A$ given by the mapping ... $(g, h, a) \mapsto (g(a)h^{-1})$, (The idea is to multiply by an inverse, or induce another anti-isomorphism that reverses the order of multiplication, e.g., transpose of matrices.)

DEF! Suppose $G$ is a group and $H < G$. Consider the left and right actions of $H$ on $G$. The set of left cosets $G/H$ (respectively right cosets $H \backslash G$) is ... the set of orbits of the right (respectively left) action of $H$ on $G$. 

EX! A typical element of $G/H$ is of the form ... $$gH = \{gh : h \in H\}.$$

CORO! (Lagrange's theorem) Suppose $G$ is a group and $H < G$. Then the order of $H$ divides the order of $G$.

\newcommand{\sS}{\mathscr{S}}

EX! Since membership in cosets is an equivalence relation, we often select a set of coset representatives for a subset $\sS \subset G$ such that ... $\abs{\sS \cap gH} = 1$ for all $g \in G$.

Now braid diagrams represent permutations in $S_n$, and one can consider the set of $S_n / (S_2 \times S_{n-2})$ as a set of concatenated permutations, first an element of $S_n$, then an element of $S_2 \times S_{n-2}$. (It's "philosophically easier" to work with braids rotated by $90^\circ$ counterclockwise, as then the left and right actions *flow* left or right.) How ought we to choose coset representatives from $S_2 \times S_{n-2}$? Suppose we choose to take only minimal crossing representatives. Then to which coset does a braid diagram from $S_n$ belong? Well, can reduce to a minimal crossing representative the braid diagram of an element $\sigma$ in $S_n$ by finding the (unique) element $\tau$ of $S_2 \times S_{n-2}$ for which $\tau\sigma$ has minimal crossings. We imagine the group $S_2 \times S_{n-2}$ as "vacuuming up" as many crossings as possible from $S_n$. 

In this light, row reduction of matrices is essentially picking coset representatives from a biaction. Coming up... Bruhat decomposition!

Concepts I struggled with: 

- A subgroup $M$ of a group $G$ is called a *maximal subgroup* if $M \neq G$ and the only subgroups of $G$ which contain $M$ are $M$ itself and $G$.
- A finite group with no more that two maximal subgroups is cyclic.

### Week 4

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

I started a [review group](https://github.com/coltongrainger/pro19alg1/blob/master/midterm01-review.md)!

#### Bruhat decomposition

What is [Bruhat decomposition](https://en.wikipedia.org/wiki/Bruhat_decomposition)? 

Let $B$ be the subgroup of upper triangular matrices in $GL_n(\FF)$. We want to choose double coset representatives from the set 
$$B \backslash GL_n(\FF) /B = \{BgB | g \in G\}.$$

Note that elementary matrices in $B$ perform row operations on elements $g \in GL_n(\FF)$. So, given an arbitrary $g \in G$, we choose $b \in B$ to maximize the number of leading $0$'s of the product $bg$. 

But $bg$ might not be in upper triangular (generally, echelon) form, so find a permutation (matrix) $w \in S_n \le GL_n(\FF)$ such that $wbg \in B$. So $wbg = b
' \in B$. But then $g = b^{-1}w^{-1}b' \in Bw^{-1}B$, the double coset labelled by an element of the symmetric group.


Concepts I struggled with:

- the Heisenberg group of unit upper triangular $3 \times 3$ matrices in $\FF$,

### Week 5

Concepts I struggled with:

- *timeliness!*
    - With no time to revise the problem set, I glossed over difficult-to-typeset notation I had introduced when sketching up the proofs. My hurriedness cost me clarity, and Thiem didn't really follow the arguments. (F**k! I don't really follow my arguments!)
- Fermat's little theorem
- order of groups and subgroups when factored through a quotient group
    - what relations exist between $\pi(H) < G/N$ and $H < G$?
- specifying *in which group* a subgroup is normal

