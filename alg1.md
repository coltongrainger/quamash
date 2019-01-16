---
title: Modern Algebra 1
author: Colton Grainger
date: 2018-08-27
revised: 2018-12-01
---

## Prelim Exam syllabus

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

EX: What's a homomorphism from $GL_n(\RR) \to \RR^\times = (\RR \setminus \{0\})$? ... the determinant, since it's well defined and $\det(AB) = \det(A)\det(B)$.

> Show that there exists a bijection from $GL_n(\RR)$ to $\RR^\times$. Show that such a bijection is certainly *not* a isomorphism.

DEF: Write the factorial $n!$ in two ways, explicitly and inductively. ... Explicitly (or imperatively) $n: = 1 \cdot 2 \cdot 3 \cdots (n-1) \cdot n$, inductively (or recursively) $n: = n(n-1)!$ for $n > 1$ and $1: = 1$.

### Week 1: group axioms and examples

Course with Nat Thiem. Still haven't hammered out the bibliography. Maybe: 

- Artin (just for rotation groups)
- Hungerford (yes)
- Dummit and Foote (duh)
- R. Vakil (later)
- E. Riehl (yes)

Git repo: <http://github.com/coltongrainger/fy19alg1>.

#### What to expect?

1. Axiomatic treatment of fundamental algebraic categories
2. Preparation for half of the examinable material on the prelim
    - chapters 1 to 9 in Dummit and Foote
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

Discussion from [@Hu80, chapter II.4]:

EX: $S_n$ obviously acts on ... $I_n = \{1,\ldots, n\}$.

EX: With $G$ a group and $H$ a subgroup, an action of $H$ on the set $G$ is given by $(h,x) \mapsto hx$; the action of $h \in H$ on $G$ is called a ... left translation.

\providecommand{\sS}{\mathscr{S}}

IDEA: If $G > K$, $G>H$, and $H$ acts on $G$ by left translation, then $H$ also acts by left translation on the set $\sS$ of cosets of $K$ in $G$. The action of $H$ on $\sS$ is explicitly given by ... $(h, xK) \mapsto hxK$.

The idea of "$G$ acting on a set $A$" is that for a fixed $g \in G$, we have a permutation $\sigma_g \colon A \to A$ defined by $a \mapsto g\cdot a$. We might think that a group $G$ acts on a set $A$ if there exists a homomorphism $\phi \colon G \to S_A$. Indeed, the map $\phi \colon G \to S_A$ defined by $g\mapsto \sigma_g$ is a homomorphism because $\phi(gh) = \phi(g)\circ\phi(h)$ for all $g,h \in G$. We formalize this notion in the following proposition.

PROP: $G \times A \to A$ (where elements of the image are written $g\cdot a$) is an action iff $\phi \colon G \to S_A$ is (define and give required condition) ... a homomorphism that maps element of the group $g$ to permutations of the set $\phi(g) \colon A \to A$ such that $\phi(g)$ maps elements of the set $a$ to their images under the group action $g(a)$.

DEF: An action $G\times A \to A$ is trivial if ... $g\cdot a = a$ for all $a \in A$ and all $g \in G$.

DEF: An action $G\times A \to A$ is faithful if ... $g\cdot a = a$ for all $a \in A$ implies $g = 1$. In other words, distinct elements of $G$ induce distinct permutations of $A$.

(Such an action occurs when the associated homomorphism $\phi$ from $G$ to $S_A$ is injective (since then $\ker(\phi) = \{\mathrm{id}\}$).)

\providecommand{\id}{\mathrm{id}}

THM: If $G$ acts faithfully on $A$ then $G \cong H \leq S_A$. (Describe the injection.) ... Let $\phi \colon G \to S_A$ be the corresponding homomorphism. If $\phi(g) = \phi(h)$ then $\id_A = \phi(g)\phi(h)^{-1} = \phi(gh^{-1})$. Since $G$ is faithful, $gh^{-1} =1$, hence $g=h$, hence $\phi$ is injective, and thus an isomorphism.

We have Cayley's theorem, philosophically pleasing, yet useless.

THM: (Cayley's theorem) If $G$ is a group and $\abs{G} = n$ then ... $G \cong H \leq S_n$. That is, every finite group of order $n$ is isomorphic to a subgroup of the group of symmetries on $n$ elements.

*Proof sketch*. 

- $G$ acts on $G$ by $G \times G \to G$ where $(g,h) \mapsto g(h) = gh$. 
- The action is faithful ("hyperfaithful") because $gh = h$ implies $g=1$.
- Thus $G\cong \phi(G)$ where $\phi$ is the action's associated homomorphism $\phi\colon G \to S_G$, which we've shown is injective. 
- Now $\phi(G) \subset S_G \cong S_n$, from whence we conclude the desired subgroup exists.

EX: $D_{2n} \subset S_{D_{2n}} \cong S_{2n}$. However, $D_{2n}$ already acts faithfully on $\{1,\ldots,n\}$, so $D_{2n} \subset S_n$.


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

#### Preview of representation theory

\providecommand{\QQ}{\mathbf{Q}}

EX: Some fields to think about ... $\RR$, $\CC$, $\QQ$, $(\ZZ/p\ZZ)^\times$, $\{\text{units in }(\ZZ/n\ZZ)^\times\}$. Note that $\ZZ$ is not a field.

\providecommand{\FF}{\mathbf{F}}

DEF: ($\FF$-module) A vector space $V$ over a field $\FF$ is a set with functions $+ \colon V \times V \to V$ and $\cdot \colon \FF \times V \to V$ such that ... (V1) $V$ is an abelian group under vector addition $+$; (V2) $\cdot \colon \FF \times V \to V$ gives an action of $\FF^{\times}$ on $V$; (V3) the distributive law holds for scalar multiplication $\cdot$ across addition $+$ and vice versa, i.e., for $r,s \in \FF$ and $u,v \in V$ we have $(r + s)(u + v) = ru + rv + su + sv$.

DEF: An action of a group $G$ on an $\FF$-module $V$ is a function $G\times V \to V$ that maps $(g,v) \mapsto u$ such that ... (M1) $G\times V \to V$ is a group action of $G$ on a set $V$ and (M2) for $g \in G$, $a,b \in F$ and $v,u \in V$ we have $$g(au + bv) = ag(u) + bg(v).$$

EX: (Permuting coordinates) For $\FF^n$ define the action $S_n \times \FF^n \to \FF^n$ by ... $$(\sigma, v) \mapsto \begin{pmatrix} v_{\sigma(1)}\\v_{\sigma(2)}\\\vdots \\v_{\sigma(1)}\end{pmatrix}$$

TODO: What's $\FF^n$?

EX: (General linear action) With $GL_n(\FF)$ the group of invertible $n \times n$ matrices, define the action $GL_n(\FF) \times \FF^n \to \FF^n$ by ... $$(g, v) \mapsto gv \quad (\text{matrix multiplication}).$$

PROP: The vector space $V$ is a $G$-module if and only if ... there exists a homomorphism $G \to GL(V) = \{ \text{invertible linear transf. of $V$}\} \subset S_V$. 

To specify the homomorphism from $GL(V)$ to $S_V$ we need to choose both a *basis set* and an *order of the coordinates*. This leads to representation theory.

- How to represent a group as a set of matrices?
- What are the possible dimensions of such a matrical representation?
- What eigenvalues arise? What traces? u.s.w.

#### Review

Concepts I struggled with:

- fixed point free automorphisms
- manipulating permutations as group elements 
- distinguishing elements from actions in this case
- *timeliness!*

### Week 3: subgroups through actions

We had a definition quiz on

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

\providecommand{\Norm}[2]{\mathrm{Norm}_{#1} \left( #2 \right)}

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

AGAIN: The center of a group $G$ is the kernel of the group homomorphism $\tau \colon G \to \mathrm{Aut}(G)$ where $\tau \colon g \mapsto \tau_g \colon G \to G$ such that $x \mapsto gxg^{-1}$, i.e., $\ker \tau$ is given by $\{gxg^{-1} = x : \text{ for all } x,g \in G\}.$

*Key idea*. [@Hu80, chapter II.4] Let $G$ act on itself by conjugation. The image of the group homomorphism $\tau \colon G \to S_G$ induced by the group action is contained in $\mathrm{Aut}(G)$. Clearly, for all $x \in G$, $$g \in \ker \tau \iff \tau_g(x) = x \iff gxg^{-1} = x  \iff gx = xg.$$

- Note that conjugation is *faithful* when the center of a group is trivial, and is *trivial* when the center of a group is the group itself.

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

*Key idea.* Verify $gx = hx$ iff $g^{-1}hx = x$ iff $gh^{-1} \in \Stab{G}{x}$ iff $g \Stab{G}{x} = h\Stab{G}{x}$.

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

From Spivak:

> There are good reasons why the theorems should be easy and the definitions hard.

From Benedict Gross:

> The names are idiotic. I mean, the fundamental theorem of algebra is a result in complex analysis. But not to go on about the pretension of the names. The work is in the subgroup definition for normal and the group operation on the coset space. We've built up enough ammo to just *kill* the theorem.

THM: (First isomorphism theorem) Let $\phi \colon G \to H$ be a group homomorphism. Then ... $$\phi(G) \cong G/\ker{\phi}.$$

> "any homomorphism of groups factors uniquely through the quotient group by the kernel"

Where $\pi$ is the natural projection $G \to G/\ker{\phi}$, the following diagram commutes.

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

DEF: (Eilenberg) A short exact sequence of groups is a diagram $$1 \to H \xrightarrow{g} G \xrightarrow{f} G' \to 1$$ where $f$ and $g$ are group homomorphisms and ... the image $g(H) = \ker f$, with $g$ injective and $f$ surjective.

- By the first isomorphism theorem, $G' \cong G/H$. 
- The image is the kernel of the next map.
- Warning! The inputs $H$ and $G'$ do not determine the group $G$.
  - e.g., $S_3 \not\cong \ZZ/6\ZZ$ 
  - yet $1 \to A_3       \hookrightarrow S_3      \xrightarrow{\mathrm{sgn}} \langle \pm 1 \rangle \to 1$
  - and $1 \to 2\ZZ/6\ZZ \hookrightarrow \ZZ/6\ZZ \xrightarrow{\mod 2} \ZZ/2\ZZ \to 1$

THM: (Second, or diamond, isomorphism theorem) Let $H, K \le G$ be subgroups with $H \le \Norm{G}{K}$. Then ... $H \cap K \triangleleft H$ and $H / (H \cap K) \cong ( HK )/K$. (A mouthful without the diagram; key idea: what do $H$ and $K$ generate? where do they meet?)

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

Here's one particular application of the third isomorphism theorem, which relies on Cayley's theorem [@DF04, chapter 4.2].

PROP: If $G$ is a finite group of order $n$ and $p$ is the smallest prime dividing $\abs{G}$, then any subgroup of [?] $p$ is normal in $G$ ... index.

*Proof sketch*. 

- Suppose $H \le G$ and $\abs{G : H} = p$. 
- Let $\pi_H$ be the permutation representation $\pi \colon G \to S_p$ afforded by left multiplication of the cosets of $H$ in $G$, let $K = \ker \pi_H$, and let $\abs{H:K} = k$.
- Now $\abs{G:K} = \abs{G:H}\abs{H:K} = pk$. Since $H$ has $p$ left cosets, $G/K$ is isomorphic to a subgroup of $S_p$ by the first isomorphism theorem. 
- By Lagrange's theorem, $pk = \abs{G/K}$ divides $p = \abs{G/H}$.
- Thus $k$ divides $(p-1)!$
- But all the prime divisors of $k$ are at least as large as $p$.
- With $p$ chosen minimally, we're forced to accept $k = 1$, so $K = H$, and therefore $H \triangleleft G$.

<!---
PROP: Let $G$ be finite and $p$ be the smallest prime dividing the order of $G$. If $H \le G$ satisfies $\abs{G : H} = p$, then ... $H \triangleleft G$.

*Proof sketch*. (Thiem) I didn't really feel this was clear in lecture, so I'm opting to use Dummit and Foote's version.

- Let $G$ act on the cosets $G/N$ by left multiplication. 
- Consider the homomorphism $\phi \colon G \to S_{G/H}$ 
    - where $\phi$ is given by $g \mapsto L_g \colon G/H \to G/H$ 
    - where $\L_g$ is given by $aH \mapsto gaH$.
- What's the kernel of $\phi$? 
  - (We don't have a strong enough hypothesis to show $\ker \phi \subset H$.)
--->

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

We had a definition quiz on 

- kernel
- subgroup 
    - it's nonempty!
- laundry listing definitions of normal
    - e.g., writing $N_G(N)$ (rather than $\Norm{G}{N}$) to indicate the normalizer of $N$ in $G$ when $G$ is acting on itself by conjugation
    - one needs to defined how a set can be "fixed" by a group action
        - element- or set-wise?
- the orbit $G(a)$ of $G$ acting on $a$


#### Simple groups

DEF: A group is simple if $N \triangleleft G$ implies ... $N \in \{\{1\},G\}$.


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

- We want some relation between commutator subgroups and simple groups.
- When is the commutator subgroup simple? TODO

- Eventually we'll see a relation between nontrivial centers and proper commutators, arising from the construction of lower and upper central series.

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
- We can readily handle abelian subgroups en route to a stronger argument.

How to show a group is not solvable? 

- Show a normal with abelian subquotients can't proceed from $G$ to $\{1\}$.

#### Blocks under the action of a permutation group

DEF: Let $G$ be a permutation group acting transitively on the finite set $A$. A block is a nonempty subset $B$ of $A$ such that for all $\sigma \in G$ either ... $\sigma(B) = B$ or $\sigma(B) \cap B = \emptyset$ (where $\sigma(B)$ is the set $\{\sigma(b) : b \in B\}$).

DEF: A transitive group $G$ acting on a set $A$ is said to be *primitive* if ... the only blocks in $A$ are the trivial ones, the sets of size $1$ and $\abs{A}$.

#### Symmetric and alternating groups

DEF: A simple transposition in $S_n$ is a ... $2$-cycle of the form $(i, i+1)$ for $1 \le i \le n-1$. We often write $s_i = (i, i+1)$ to abbreviate.

The simple transpositions give a generating set for $S_n$.

*Proof by example.* Suppose $\sigma \in S_n$ and write $\sigma$ in braid notation. We have a poset on the crossings because the strands never turn back up the braid diagram. We can then pull out the simple transpositions by ordering the crossings on each string. Lo and behold, this method gives us the minimal number of transpositions to use.


- Open question: the discriminant $\Delta$ under the group action of $S_n$ on the indices of the polynomial has *what* relation to eigenvalues if $\Delta$ is considered to be a subspace inm $\FF[x_1, \ldots, x_n]$?

THM: Let $S_n \to \mathrm{GL}_n(\FF)$ act by left multiplication of permutation matrices. Then for any $\omega \in S_n$, we have $\det(\omega)$ given by ... $\epsilon(\omega)$.

*Proof sketch*. TODO (see notes 2018-10-19 #8)

We ought also to define the sign of a permutation. Here's a sketch.

- either define the determinant independent of the sign
- then ask what's the determinant of a simple transposition?
- (it's analogous to the *discriminant* of a simple transposition)
- one then generalizes to the set simple transpositions, which are generators for $S_n$

DEF: The alternating group $A_n$ is the subgroup ... $\ker{\epsilon} \triangleleft S_n$, the set of "even permutations", where $\epsilon\colon S_n \to \{-1,1\}$ is the sign function.

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
    - one really should just bite the bullet 
    - define injectivity and surjectivity
- $S_n$
    - requires "binary operation"
- cycle
    - naive attempt: "a cycle is an element of $S_n$ that cannot be factored into disjoint simple transpositions distinct form itself"
- $\epsilon$
    - the sign of a permutation
    - requires "matrix representation" or "discriminant"

Coming up:

- Sylow theory (6th week to 10th week)
- fundamental theorem of abelian groups

#### Definitions for conjugacy

Definitions from the book [@DF04, chapter 4.3]:

DEF: Two elements $a$ and $b$ are said to be conjugate in $G$ if ... there is some $g \in G$ such that $b = gag^{-1}$ (i.e., iff they are in the same orbit of $G$ acting on itself by conjugation).

DEF: If $G > H$ and $G> K$, then for $h \in H$ we have $K \cong hKh^{-1} < G$. Hence $H$ acts on the set $\sS$ of all ... subgroups of $G$ by conjugation $(h,K) \mapsto hKh^{-1}$. Note the subgroup $hKh^{-1}$ is said to be conjugate to $K$.

- In linear algebra, "conjugate" elements of a $n\times n$ general linear group are said to be *similar*.
- Conjugation by $g$ on $G$ induces an isomorphism (*not unrelated to normality*) --- how?

EX: The conjugacy classes of an abelian group $G$ are given ... $\{\{g\} : g \in G\}$ (analogous to "totally disconnected"?)

DEF: If a group $G$ acts on itself by conjugation, then the conjugacy class of an element $x \in G$ is ... the orbit $\{gxg^{-1} : g \in G \}$.

PROP: A group $G$ is simple if and only if for any $1\neq x\in G$, the conjugacy class of $x$ in $G$ ... generates the whole group $G$.

*Proof sketch*. TODO

We've already seen the centralizer of $x$ in $G$ as $C_G(x)$, now we generalize to define the centralizer of an element in a subgroup $H < G$.

AGAIN: If a subgroup $H$ of $G$ acts on $G$ by conjugation, then the stabilizer $\Stab{H}{x} = \{h \in H : h x h^{-1} = x\}$ is called ... the centralizer of $x$ in $H$, denoted $C_H(x)$.

EX: Let $H < G$, groups, and suppose $G$ acts on itself by conjugation. For each $a \in G$, the set $a H a^{-1}$ is ... a subgroup for that's is isomorphic to $H$.

#### Conjugacy classes in $S_n$

Cycle decomposition shines when we're handling conjugacy.

LEMMA: Let $w$ and $v$ be permutations in $S_n$. If $w = c_1c_2\cdots c_\ell$ where the $c_i$ are cycles, then $vwv^{-1}$ is given by ... $vc_1v^{-1}vc_2v^{-1}\cdots vc_\ell v^{-1}$.

LEMMA: Let $w$ and $v$ be permutations in $S_n$. If $w = (i_1, i_2, \ldots, i_\ell)$, then $vwv^{-1}$ is given by ... $vwv^{-1} = (v(i_1), v(i_2), \ldots, v(i_\ell))$.

CORO:  Let $w, v \in S_n$ have cycle decompositions $w =  c_1c_2\cdots c_k$  and $v = d_1 d_2 \cdots d_\ell$. Then $w$ and $v$ are conjugate iff ... $k = \ell$ and there exists $\omega \in S_n$ to reorder coordinates such that $$\mathrm{length}(c_{\omega(j)}) = \mathrm{length}(d_j)$$ for all $1 \le j \le \ell$.

- One can express $S_n$ acting on $\mathrm{GL}_n(\FF_q)$ by permutation matrices. 
- I hear $\mathrm{GL}_n(\CC)$ has rad matrix similarity.
- TODO: translate the above corollary for matrix representations.

DEF: An integer partition $\lambda$ of $n$ is a sequence $\lambda = (\lambda_1, \ldots, \lambda_\ell)$ such that ... (IP1) $\lambda_1 \ge \lambda_2 \ge \ldots \ge \lambda_\ell > 0$ and (IP2) $n = \lambda_1 + \lambda_2 + \ldots + \lambda_\ell$.

  DEF: The cycle type of a permutation $\omega \in S_n$ is ... the unique integer partition of $n$ obtained by reordering the cycle length of the cycle decomposition of $\omega$ into nonincreasing order (a mouthful, yes).


#### The class equation

As a corollary to orbit stabilizer, we have the following [@Hu80, chapter II.4].

CORO: (Justification for class equation) Let $G$ be a finite group and $K$ a subgroup of $G$. (i) The number of elements in the conjugacy class of $x \in G$ is $\abs{G : C_G(x)}$, which divides $\abs{G}$; (ii) the number of subgroups of $G$ conjugate to $K$ is $\abs{G : N_G(K)}$, which divides $\abs{G}$; (iii) if $G(x_1),\ldots, G(x_n)$ are the distinct conjugacy classes  then ... $$\abs{G} = \sum_{i=1}^n \abs{G: C_G(x_i)}.$$

*Proof sketch*. 

i. The set $G$ is partitioned into disjoint orbits under the conjugation group action of $G$ on its elements. By orbit-stabilizer, then, summing the index of each conjugacy class in $G$, we have $\abs{G}$. 
ii. $G$ also acts by conjugation on the set of its subgroups. Now $N_G(K)$ is a subgroup of $G$, so by Lagrange's theorem, $\abs{N_G(K)}$ divides $\abs{G}$. Therefore $\abs{G : N_G(K)}$ divides $\abs{G}$.
iii. $G$ is the disjoint union of such conjugacy classes.

THM: (Class equation) Let $g_1, g_2, \ldots, g_\ell \in G / Z(G)$ be representatives for the conjugacy classes not in the center of a group $G$. Then (by orbit stabilizer) the order of $G$ is given by ... $$\abs{Z(G)} + \sum_{j=1}^\ell \frac{\abs{G}}{\abs{C_G(g_j)}}.$$

- Note the number of elements in the center of $G$ is the number of singleton conjugacy classes. 
- (Categorically akin to totally disconnected components in topology? Maybe not.)

CORO: If $\abs{G} = p^k$ for $p$ prime, then $Z(G)$ is not ... trivial.

*Proof sketch*. 

- Consider the class equation: $\abs{G} = \abs{Z(G)} + \sum_{j=1}^\ell \frac{\abs{G}}{C_G(g_j)}$.
- Now $\abs{C_G(g_j)} > 1$ else we'd have $g_j \in Z(G)$.
- Hence $\abs{C_G(g_j)}$ divides $\abs{G}$.
- Therefore $\sum_{j=1}^\ell \frac{\abs{G}}{C_G(g_j)} \equiv 0 \mod p$.
- It follows that $\abs{G} \equiv \abs{Z(G)} \mod p$.
- By hypothesis, $\abs{G} \equiv 0 \mod p$.
- From last two points, together with the fact that $Z(G) \ni \{1\}$, we conclude $\abs{Z(G)} \ge p > 1$.

The style here should be familiar from J.H. McKay's proof of Cauchy's theorem. 

To give another example of the "mod $p$" style, we'll present a quick result from [@Hu80, chapter II.5].

LEMMA: If a group $H$ of order $p^n$ (where $p$ is prime) acts on a finite set $S$ and $$S_0 = \{x \in S: hx = x \text{ for all } h \in H\},$$ then $\abs{S} \equiv$ ... $\abs{S_0} \mod p$.

*Proof sketch*. 

- $S_0$ is the collection of all $x \in S$ with singleton orbits under the action of $H$, $H(x) = \{x\}$. 
- Now the orbits of $H$ partition the set $S$, and by construction of $S_0$ we can write $S = S_0 \sqcup H(x_1) \sqcup H(x_2) \sqcup \cdots \sqcup H(x_n)$ with $abs{H(x_i)} > 1$ for all $i$. 
- Hence $\abs{S} = \abs{S_0} + \sum_{i=1}^n \abs{H(x_i)}.$
- Why does $\abs{p}$ divide $\abs{H(x_i)}$? 
    - Because $\abs{H(x_i)} > 1$ and $\abs{H(x_i)}  = \frac{\abs{H}}{\abs{\Stab{H}{x}}}$ divides $\abs{H}  = p^n$.
- Therefore $\abs{S} \equiv  \abs{S_0} \mod p$.

Onwards!

#### Cauchy's theorem

THM: (Cauchy) If $G$ is a finite group whose order is divisible by a prime $p$, then $G$ contains an element ... of order $p$.

*Key idea*. $Z_p$ acts on by cyclic permutation on the set of $p$-tuples of group elements $$\{(a_1, a_2, \ldots, a_p) : a_i \in G \text{ and } a_1a_2 \cdots a_p = e\}.$$

*Proof.*^[Prompted by an exercise (3.2.9) in Dummit and Foote, derived from James McKay (*Another proof of Cauchy's group theorem*, Amer. Math. Monthly, 66(1959), p. 119)]

Let $G$ be a finite group and let $p$ be a prime dividing $\abs{G}$. Let $\sS$ denote the set of $p$-tuples of elements of $G$ the product of whose coordinates is $1$: 
$$\sS = \left\{(x_1 , x_2, \ldots, x_p) : x_i \in G \text{ and } x_1x_2 \cdots x_p = 1\right\}.$$

(a) $\sS$ has $\abs{G}^{p-1}$ elements, hence has order divisible by $p$. Why? Of $\abs{G}$ elements, choose $p-1$ with repetitions, and such that the product of the $p$ elements is $1$, we must take the unique inverse $x_p = (x_1 \cdots x_{p-1})^{-1}$. So $\abs{\sS} = \abs{G}^{p-1}$. By Fermat's little theorem, $p$ divides $\abs{G}^{p-1}$.

For notation's sake, let $C_p$ (considered as a subgroup of the symmetric group on $p$ letters) act on $\sS$ by $$\sigma(x_1, \ldots, x_p) \mapsto (x_{\sigma(1)}, \ldots, x_{\sigma(p)}).$$ Now we identify each cyclic permutation shifting $j$ entries right of every $\alpha \in \sS$ with $\sigma^j(\alpha)$ where for $j \in \ZZ$ $\sigma^j$ is the $p$-cycle $(1\, 2\, \cdots p)^j$. Now the action is faithful, and additionally for all $j \in ZZ$ and all $\alpha \in \sS$ we know $\sigma^j(\alpha) \in \sS$ since $x_p$ remains nested in cyclic order between $x_{p-1} and x_1$.

Define the relation $\sim$ on $\sS$ by letting $\alpha \sim \beta$ if $\beta$ is a cyclic permutation of $\alpha$. 

(b) We've shown a cyclic permutation of an element of $S$ is again an element of $\sS$.

(c) $\sim$ is an equivalence relation on S. Why? 

  - $\sigma^0(\alpha) = \alpha$ gives reflexivity,
  - $\sigma^{-k}(\beta) = \alpha$ whenever $\sigma^j(\alpha) = \beta$ gives symmetry, and lastly 
  - for $\sigma^j(\alpha) = \beta$, $\sigma^k(\beta) = \gamma$ then $\sigma^{k+j}(\alpha) = \gamma$.

(d) An equivalence class in $\sS$ contains a single element if and only if it is of the form $(x, x, \ldots, x)$ with $x^p = 1$.

Note that $\sigma^j$ stabilizes elements of the form $(x, x, \ldots, x)$ for all $j \in \ZZ$. Now if $\alpha \in \sS$ is not of the form $(x, x, \ldots, x)$ then the equivalence class in $\alpha$ has $p$ distinct elements, because $\sigma^j(\alpha) = \alpha$ if and only if $j \in \ZZ/p\ZZ$. There are no more distinct elements in $\alpha$'s equivalence class than those already conspicuous, namely $\alpha, \sigma(\alpha), \ldots, \sigma^{p-1}(\alpha)$.

(e) Every equivalence class has order $1$ or $p$ (note that p is a prime). Whence $\abs{G}^{p-1} = k + pd$, where $k$ is the number of classes of size $1$ and $d$ is the number of classes of size $p$.

Since $\sS$ is partitioned by $\sim$, summing the elements in each class will produce $\abs{G}^{p-1}$. Well, an $\bar{\alpha} \in \sS/\sim$ has size $1$ or $p$. Say there are $k$ classes of size $1$ and $d$ classes of size $p$. Thus $\abs{G}^{p-1} = k + dp$.

(f) Since $\{(1, 1, \ldots , 1)\}$ is an equivalence class of size $1$, from (e) there must be a nonidentity element $x$ in $G$ with $x^p = 1$, that is, $G$ contains an element of order $p$. 

Since $p$ divides $\abs{G}^{p-1}$ we must have that $p$ divides $k + dp$ hence $p | k$. Because $k > 1$, we have $k = mp$ for some integer $m \neq 0$, so there's a non-identity element $x \in G$ with $x^p = 1$. QED

#### Automorphisms

> Essential to the study of any class of algebraic objects are the functions that preserve the given algebraic structure in the following sense. [@Hu80, chapter I.2]

DEF: Let $G$ and $H$ be semigroups.  A function $f \colon G \to H$ is a homomorphism provided $f(ab) = f(a)f(b)$ for all $a,b \in G$. If $f$ is injective as a map of sets, $f$ is said to be a [1]. If $f$ is bijective, $f$ is called a [2]. A homomorphism $f \colon G \to G$ is called an [3] of $G$ and an isomorphism $f \colon G \to G$ is called an [4] of $G$. ... 1: monomorphism, 2: isomorphism, 3: epimorphism. 4: automorphism.

\providecommand{\Aut}[1]{\mathrm{Aut}\left( #1 \right)}

FACT: The set of all automorphisms $\Aut{G}$ forms ... a group under composition.

\providecommand{\inn}[1]{\mathrm{inn}\left( #1 \right)}
\providecommand{\Inn}[1]{\mathrm{Inn}\left( #1 \right)}

DEF: For each $g \in G$ we have an isomorphism $\inn{g} \colon G \to G$ given by ... $h \mapsto ghg^{-1}$ for all $h \in G$.

DEF: The set of inner automorphisms of a group $G$, denoted $\Inn{G}$, is ... $\{\inn{g} : g \in G\} \subset \Aut{G}$.

FACT: The set of inner automorphisms $\Inn{G}$ arises from ... the permutation representation of the conjugation action of $G$ on itself.

PROP: If $N \triangleleft G$, then $\Inn{N} \le$ [?] $\le \Aut{N}$ ... $\underbrace{\Inn{G}}_{\text{restricted to $N$}}$.

PROP: For an arbitrary group, $\Inn{G}$ is normal in ... $\Aut{G}$.

PROP: For an arbitrary group, $\Inn{G}$ is isomorphic to ... $G/Z(G)$.

*Proof sketch.*

- To show normality, take $g,h \in G$ and $\phi \in \Aut{G}$.
    - $(\phi \circ \inn{g} \circ \phi^{-1})(h) = \phi(g\phi^{-1}(h)g^{-1}) = \phi(g)h\phi(g^{-1}) = \inn{\phi(g)}(h)$
    - Therefore $\phi \circ \phi^{-1} \in \Inn{G}$.
- For isomorphism, consider the epimorphism $\mathrm{Inn} \colon G \to \Inn{G}$ that maps $g \mapsto \inn{g}$.
    - By the first isomorphism theorem $\Inn{G} \cong G/\ker{\mathrm{Inn}}$.
    - What's? $\ker{\mathrm{Inn}}$?
    - $Z(G) = \{g \in G : ghg^{-1} = h \text{ for all } h \in G\}$.

EX: For $n \ge 2$ with $n \neq 6$ the inner automorphisms $\Inn{S_n}$ coincide with ... $\Aut{S_n}$.

Results from the book [@DF04, chapter 4.4]:

PROP: Let $H$ be a normal subgroup of $G$. The action of $G$ on $H$ by conjugation induces permutation representation, that is a homomorphism of $G$ into $\Aut{H}$ with kernel given by ... $G/C_G(H)$. 

PROP: For any subgroup $H$ of a group $G$, the quotient group [...] is isomorphic to a subgroup of $\Aut{H}$ ... where that quotient group is $N_G(H)/C_G(H)$.


EX: Assume $G$ is a group of order $pq$, where $p$ and $q$ are primes with $p \le q$. If $p \not\vert q - 1$, then $G$ is ... abelian.

*Proof sketch*.

- If the center is nontrivial, Lagrange's theorem forces $G/Z(G)$ to be cyclic.
- Suppose then the center is trivial.
- If every non-identity element of $G$ has order $p$, the centralizer of every non-identity element has index $q$, so the class equation reads $pq = 1 + kq$, a contradiction.
- Thus $G$ contains an element of order $q$, call the subgroup it generates $H = \langle x \rangle$.
- Now $H$ has index $p$, and $p$ is the smallest prime dividing $pq$, so (prelude to Sylow theory) $H$ is normal in $G$.
- Moreover, $H$ is cyclic, thus abelian.
- Noting $H$ is maximal among abelian subgroups of $G$, for $Z(G) = 1$, we have $C_G(H) = H$.
    - <https://groupprops.subwiki.org/wiki/Self-centralizing_subgroup>
    - <https://groupprops.subwiki.org/wiki/Equivalence_of_definitions_of_maximal_among_abelian_subgroups>
    - <https://en.wikipedia.org/wiki/Centralizer_and_normalizer>
- Then $G/H = N_G(H)/C_G(H)$, which is isomorphic to a subgroup of $\Aut{H}$.
- But the order of that automorphism group is $\abs{\Aut{H}} = q-1$. 
- We obtain the contradiction $p | q-1$. 
- So $Z(G) = G$.

DEF: Let $p$ be a prime and let $V$ be an abelian group with the property that $pv = 0$ for all $v \in V$. When $\abs{V} = p^n$, $V$ is called the elementary abelian group of order $p^n$, and turns out to be ... an $n$-dimensional vector space over the field $\FF_p = \ZZ/p\ZZ$, with $\Aut{V} \cong \mathrm{GL}_n(\FF_p)$. 

EX: If $V$ is a vector space over $\ZZ/p\ZZ$ for prime $p$, then $\underbrace{\Aut{V}}_{\text{as an abelian group}}$ is isomorphic to  ... $\mathrm{GL}(V) \cong \mathrm{GL}_{\dim V}(\ZZ/p\ZZ)$.

*Proof sketch.* 

- Let $a,b  \in \ZZ/p\ZZ$, let $u,v \in V$, and let $\phi \in \Aut{V}$. 
- $\phi(au + bv) = \phi(\underbrace{u + \cdots + u}_{\text{$a$ times}} + \underbrace{v + \cdots + v}_{\text{$b$ times}}) = a\phi(u) + b\phi(v)$.
- So $\phi \in \mathrm{GL}(V)$.
- The opposite direction is obvious, consider the definition of a general linear transformation.

EX! The automorphism group of a cyclic group of order $n$ is isomorphic to ... $(\ZZ/n\ZZ)^\times$, an abelian group of order $\phi(n)$.

EX! The automorphism group of a cyclic group of order $p^n$ is isomorphic to ... the cyclic group of order $p^{n-1}(p-1)$.

EX: Expectations from $\Inn{G}$ don't politely transfer over to $\Aut{G}$, especially not to ... the group of outer automorphisms $\Aut{G}/\Inn{G}$.

#### Characteristic subgroups

DEF: A subgroup $N$ is characteristic (in $G$) if ... $\phi(N) = N$ for all $\phi \in \Aut{G}$.

PROP: If $C \subset N \triangleleft G$ and $C$ is characteristic in $N$, then $C$ is normal in ... $G$.

*Proof sketch.* 

- We assume $C$ is invariant under automorphisms in $\Aut{N}$.
- Since $N$ is normal in $G$, $\underbrace{\Inn{G}}_{\text{restricted to $N$}}$ is a subgroup of $\Aut{N}$.
- Therefore $C$ is normal in $G$.

FACT: The commutator subgroup $[G,G]$ is characteristic in $G$ because ... for $g,h \in G$, and $\phi \in \Aut{G}$, $\phi([g,h]) = [\phi(g), \phi(h)] \in G$, sending generators to generators by the lattice isomorphism theorem.

The rule of "the" states ... any subgroup that is "the subgroup of ..." will be characteristic.

- What's $[G,G]$? It's *the* smallest subgroup whose quotient with $G$ is abelian.
- What's *the* center of $G$?
- What's *the* unique maximal Sylow subgroup? 

THM: (Cauchy Frobenius) Let $G$ act on $A$, then the number of orbits in $A$ is equal to ... $$\frac{1}{\abs{G}} \sum_{g \in G} \abs{\mathrm{Fix}_A(g)}$$ where $\mathrm{Fix}_A(g) = \{a \in A: g(a) = a\}$.

How many cubes can we have under different coloring schemes? Counting orbits? Counting faces?

*Proof sketch*.

\newcommand{\sF}{\mathscr{F}}

- Let $\sF = \{(g,a) \in G \times A : g(a) = a\}$.
- On one hand, $\abs{\sF} = \sum_{g \in G} \abs{\{a \in A: g(a) = a\}} = \sum_{g \in G} \abs{\mathrm{Fix}_A(g)}$.
- On the other hand, $$\abs{\sF} = \sum_{a \in a} \abs{\{a \in A: g(a) = a\}}$$
    - which is $\sum_{a \in A} \abs{\Stab{G}{a}}$
    - which is $\sum_{a \in A} \abs{G}/\abs{G(a)}$
    - which is $\abs{G} \sum_{a \in A} \frac{1}{\abs{G(a)}}$
    - which is $\abs{G} \cdot \abs{\text{card(orbits)}}$
- Note one only needs to sum over orbits (we'll specify later to conjugacy classes).

#### Review

Moral of the first midterm: *state* and *prove*. 

To list little mistakes.

- using notation $A \le \Norm{G}{B}$ without specifying the action
- running out of time to show in the diamond isomorphism theorem that $\phi \colon AB \to A/ A \cap B$ is a group homomorphism with kernel $B$
- failing to disclaim that $\mathrm{SL}_n(\FF_q)$ is abelian when $(n,q) = (2,2)$ or $(3,2)$ (something like that)
- not proving a result I needed
    - first isomorphism theorem or Lagrange's theorem
- sloppy handwriting towards the end, running out of time, reading directions
    - not *playing it cool*

### Week 7: Sylow theory and simplicity of alternating groups

We had a definition quiz on 

- orbit (again)
- conjugacy class
    - requires conjugation
- integer partition
    - requires tuple
- cycle type
    - requires cycle, cycle decomposition, cycle length

#### Sylow's theorem

Cauchy's theorem is the "baby case", [a kind of converse to Lagrange's theorem](https://math.stackexchange.com/questions/41731/)

Here's Thiem's construction, following [@DF04, chapter 4.5] and playing off of the mnemonic

- E existence
- C conjugacy
- N number

\providecommand{\Syl}[2]{\mathrm{Syl}_{ #1 }\left( #2 \right)}

DEF: Suppose $G$ is a group with order $\abs{G} = p^n m$, where $p$ is prime and $\gcd(p,m) = 1$. A Sylow $p$-subgroup $P$ of $G$ is ... a subgroup of order $p^n$ ($n \in \ZZ_{\ge 0}$).

DEF: Let $\Syl p G$ be ... the set of all Sylow $p$-subgroups of $G$.

THM:  (Sylow via Thiem) Let $\abs{G} = p^n m$, with $p$ prime and $\gcd(p,m) = 1$. ... (E) $\Syl p G \neq \emptyset$; (C) $G$ acts transitively on $\Syl p G$ by conjugation; (N) denoting $n_p = \abs{\Syl p G}$, we have $n_p \equiv 1 \mod p$.

CORO: For $\abs{G} = p^n m$, why does $\abs{\Syl p G}$ divide $m$? ... By orbit stabilizer (where $G$ acts on its powerset by conjugation) and the Sylow theorem (part C), $$\abs{\Syl p G} = \frac{\abs{G}}{\abs{N_G(H_p)}}, \quad H_p \in \Syl p G.$$

THM:  (Sylow via Gross) If $G$ is finite of order $N = p^n \cdot m$ with $p$ prime to $m$ ... (E) there's a Sylow $p$-subgroup, (C) every two Sylow $p$-subgroups are conjugate, (N) the number $\ell$ of such subgroups satisfies both $\ell | m$ and $\ell \equiv 1 \mod p$. 

THM:  (Conjugation note) If $G$ is finite of order $N = p^n \cdot m$, by Sylow (N) the number $\ell$ of Sylow $p$-subgroups satisfies both $\ell | m$ and $\ell \equiv 1 \mod p$ and we note ... $\ell = 1$ iff $H_p \triangleleft G$.

*Proof sketch.* (TODO, see notes 2018-10-20)

How to find a normal subgroup? 

- We're set if $\abs{\Syl p G} = 1$.
- Eventually we have a stronger conclusion, that is, that a [normal sylow subgroup of a finite group is characteristic](https://math.stackexchange.com/questions/93499/normal-sylow-subgroup-of-a-finite-group-is-characteristic).
- We can expect the prelim questions to be about two levels deeper than superficial applications as fining $p$ such that $\abs{\Syl p G} = 1$.

How to find "white bread" $p$-groups?

- We find a Sylow $p$-subgroup such that $\abs{H_k} = p^k$.
- Since $Z(H_k)$ is not trivial, by Cauchy's theorem we can find a cyclic subgroup $\ZZ/p\ZZ \cong H_1 \triangleleft Z(H_k)$.
- We mod out by $H_1$ to obtain a subgroup of order $p^{k-1}$.
- And so on...

LEMMA! TODO, source: <https://math.stackexchange.com/questions/891564/>

> Since $N \trianglelefteq G $, $NP$ is  subgroup of $G$ and $[NP:P]=[N:N \cap P]$ (use that $NP/N \cong P/(N \cap P))$. Since $P \in Syl_p(G)$ and $[NP:P]$ divides $[G:P]$, the index $[N:N \cap P]$ is not divisible by $p$. This implies that the $p$-subgroup $N \cap P \in Syl_p(N)$.
>
> Conversely, if $Q \in Syl_p(N)$, then the $p$-subgroup $Q$ is contained in some $P \in Syl_p(G)$ (this is a well-known lemma). Hence $Q \subseteq N \cap P$. But we just showed that $N \cap P \in Syl_p(N)$, whence $Q=N \cap P$. In other words, all Sylow $p$-subgroups of $N$ arise by intersecting those of $G$ with $N$.

#### Sylow-theoretic classifications

EX: If $\abs{G} = pq$, where $p < q$, both prime, and $p \not| q-1$, then ... $1 = \abs{\Syl q G} = \abs{\Syl p G}$ and $G \cong Z_{pq}$.

EX: If $\abs{G} = pq$, where $p < q$, both prime, and $p | q-1$, then ... the Sylow subgroup $H_q \triangleleft G$, and we need to define a twist for the action of $H_p \in \Syl p G$ on $\Aut{H_q}$.

EX: A group $G$ of order $12$ either has a normal Sylow $3$-subgroup or ... $G \cong A_4$ in which case $G$ has a normal Sylow $2$-subgroup.

EX: A group $G$ of order $p^2 q$ where $p > q$ has a normal ... Sylow $p$-subgroup.

EX: Given a group $G$ of order $p^2 q$ where $p < q$ either ... $G$ has a normal $q$-subgroup or $p^2 q = 12$ and $G \cong A_4$, the degenerate case.

EX: Let $\abs{G} = pqr$ where $p$, $q$ and $r$ are primes with $p < q < r$. Then $G$ has ... a normal Sylow subgroup for either $p$, $q$ or $r$.

*Given.* The number of Sylow subgroups for each prime respectively denoted $n_p$, $n_q$, and $n_r$. 

*To prove.* $n_p = 1$, $n_q = 1$, or $n_r = 1$, forcing a normal Sylow subgroup. 

*Proof by contradiction.* 

- Assume $n_p, n_q$, and $n_r$ are all strictly greater than $1$. To achieve a contradiction, let $k,s,t \in \NN$ parameterize $$n_p = kp + 1,\quad n_q = sq + 1, \quad n_r = tr+1.$$ 
    - For the largest prime $r$, from $tr+1 | pq$ we deduce $tr + 1 = pq$. 
    - For the middle prime $q$, we have $sq + 1 = r \text{ or } pr$. 
      - For the least prime $p$, we don't have much restriction, and in turn $kp + 1 = q \text{ or } r \text{ or } qr$.
  - How many non-identity elements are in $G$? Exactly $pqr - 1$. 
      - We'll violate this upper bound. 
  - Since the Sylow $p,q,r$-subgroups are conjugate to each other Sylow subgroup of the same prime, and cyclic, the number of non-identity elements from the Sylow subgroups must be
  $$n_r(r-1) + n_q(q-1) + n_p(p-1).$$
      - But the number of such nonidentity elements is bounded above by $pqr -1$. 
      - Working towards contradiction, we take the most conservative possible values for $n_r, n_q$, and $n_p$, and present the inequality
  $$pqr - 1 \ge pq(r-1) + r(q-1) + q(p-1).$$
      - From which it follows that $r + q \ge rq + 1$, which is absurd, as $r, q \ge 3$.

#### $A_n$ is simple for $n \ge 5$

THM! For $n \ge 5$, notably $A_n$ is ... simple.

*Proof by induction*. TODO

- Thiem's proof (directly, combinatorial) on 2018-10-12 
- Gross's proof (via the icosahedron) on 2018-10-20

Key idea: Any normal subgroup of $A_n$ is closed under conjugation, so $A_n$ must be the union of conjugate classes.

Note also $\abs{\mathrm{PSL}_2(\ZZ/p\ZZ)} = \frac{(p^2 - 1)p}{2}$ and indeed $\mathrm{PSL}_2(\ZZ/5\ZZ) \cong A_5$.

#### Geometric interpretation

I went to office hours looking for a geometric interpretation of conjugacy classes. 

geometric interpretation | concept
--- | ---
symmetries of regular polyhedra | group actions by $S_4$ and $A_5$
conjugate rotations of polyhedra | conjugacy classes, counting arguments
products of reflections | simple transpositions
inscribing diagonals, cubes | finding a permutation representation
? | Cayley graphs
eigenspaces in $\RR^5$ | eigenvalues fixed by conjugation 
canonical forms | decompositions

Other directions?

- permuting conjugacy classes by moving to the automorphism group
- finding an orbit containing two objects of interest
- larger orbits as unions of smaller conjugacy classes, *fusion*

PROP: The number of conjugates of a subset $S$ in a group $G$ is the index of ... the normalizer of $S$, $[G : N_G(S)]$ (where $G$ acts by conjugation on its powerset).

PROP: In particular, the number of conjugates of an element $s$ of $G$ is ... the index of the centralizers of $s$, $[G:C_G(s)]$, where $N_G(\{s\}) = C_G(s)$.

PROP: The number of conjugacy classes of $S_n$ is (list them up to $n = 7$) ... the number $p(n)$ of partitions of $n$, starting with $p(0)$, they are $1, 1, 2, 3, 5, 7, 11, 15, \ldots$

\providecommand{\sK}{\mathscr{K}}

FACT: Normal subgroups of a group $G$ are the union of ... conjugacy classes of $G$, i.e., if $H \triangleleft G$, then for every conjugacy class $\sK$ of $G$, either $\sK \subset H$ or $\sK \cap H = \emptyset$.

#### Apocrypha

I don't terribly enjoy printing handouts for extra reading, but I found myself sending quite a few jobs to the printer this week. It was an eco-crime justified initially to supplement topology, but, aloof and awash in sin, I did also print the following for algebra.

- [George Bergman](https://math.berkeley.edu/~gbergman)

    - [Answers to questions asked by students in Math H113](https://math.berkeley.edu/~gbergman/ug.hndts/09Sp_H113_q+a.txt), taught from Dummit and Foote 
    - [Exercises supplementing those in Dummit and Foote's "Abstract Algebra", 3rd Edition.](https://math.berkeley.edu/~gbergman/ug.hndts/mH113_D+F_exs.ps)
    - [Sketch of proof of first sylow theorem](https://math.berkeley.edu/~gbergman/ug.hndts/#sylow)
    - [Proof that the group A_n is simple for all n ≥ 5](https://math.berkeley.edu/~gbergman/ug.hndts/#A_n_simple)

- [Schedules and form of examinations for the mathematical tripos](https://www.maths.cam.ac.uk/undergrad/course/schedules.pdf)

    - Part IA: Groups
    - Part IB: Groups, Rings, and Modules

- [Alan Beardon: Algebra and Geometry](/2005-beardon-algebra-and-geometry.pdf)

    - namely chapters 12 and 14
    - conjugation, group actions, symmetries of regular polyhedra

- [Jerry Shurman](https://www.google.com/search?q=site%3Ahttps%3A%2F%2Fpeople.reed.edu%2F~jerry%2F332%2F+*pdf)

    - [The Sylow Theorems](https://people.reed.edu/~jerry/332/13sylow.pdf)
    - [Group Products](https://people.reed.edu/~jerry/332/11product.pdf)
    - [The Three Isomorphism Theorems](https://people.reed.edu/~jerry/332/09isom.pdf)

- [Keith Conrad](http://www.math.uconn.edu/~kconrad/blurbs/)

    - [Subgroup series I](http://www.math.uconn.edu/~kconrad/blurbs/grouptheory/subgpseries1.pdf)

- [Robert Friedman](https://www.math.columbia.edu/~rf/)

    - [Simple Groups](https://www.math.columbia.edu/~rf/simplegps.pdf)

#### Review

We've at least touched on all the topics for the prelim exam, though I would like get more rote practice (e.g., in Bergman's supplemental exercises) with finite groups while we're in the muck.

Other directions

- universal properties for products and quotients
- ramping up vocabulary endo- and automorphisms
- symmetries of regular polyhedra
- topological groups?

### Week 8: products of groups and series

#### Direct (sums and) products

From Jerry Shurman, [Group Products](https://people.reed.edu/~jerry/332/11product.pdf), we define a product by its characteristic mapping property.
Our goal? 

> A viewpoint of direct products in which there's literally no difference between internal and external definitions.

DEF: (Miracle of producthood) Let $G_1$ and $G_2$ be groups. A product of $G_1$ and $G_2$ is ... a group $G$ and homomorphisms  $G \xrightarrow{\pi_i} G_i$ for $i \in \{1,2\}$ (called projections) having the following property: for any passerby group $\tilde{G}$ with homomorphisms $\tilde{G} \xrightarrow{f_i} G$ for $i \in \{1,2\}$ there exists a unique homomorphism $f \colon \tilde{G} \to G$ such that $f_i = f \circ \pi_i$, to wit, any collection of homomorphisms from a passerby group into the productands factor uniquely through the product.

DEF: The external direct product of groups $G_1$ and $G_2$ is ... the cartesian product $G = G_1 \times G_2$ equipped with the obvious component-wise multiplication.

DEF: The internal direct product $G = G_1G_2$ of groups $G_1$ and $G_2$ is defined when ... $G_1 \cap G_2 = \{e\}$ and both $G_1$ and $G_2$ are normal in $G$.

Notation to straighten out

- projection homomorphisms
- $S_n$ acting by permutations of indices (preludes the wreath product)
- identifying $(x_1,\ldots,x_n)^k$ with $x_1^k\cdots x_n^k$
- identifying $i$th components with the coordinate axis subgroups

More examples

- products of subgroups of $S_n$
- groups of order $pq$, where $p$ and $q$ are primes, $p < q$, and $p | 1 - 1$

#### Semidirect products

In lecture, I asked about [permutable complements](https://groupprops.subwiki.org/wiki/Permutable_complements) without much success. See also [“Complement to normal subgroup is isomorphic to quotient group - Groupprops”](https://groupprops.subwiki.org/wiki/Complement_to_normal_subgroup_is_isomorphic_to_quotient_group).

Often we want to know when $H \triangleleft G$ how $H$ can be acted upon by some subgroup of $G$. If $H$ is abelian but not contained in $Z(G)$, then there's a element $g \in G\setminus H$ such that conjugation restricted to $H$ is not an inner automorphism of $H$. Consider $V_4 \le A_4$ and any $3$-cycle conjugating $V_4$.

Here's a case (?) in which every conjugation restricted to $H$ is an inner automorphism of $H$.

- Suppose $H \cong Z_2$. 
- Then $\Aut{Z_2} = 1$.
- We must have that $N_G(H)/C_G(H) \cong 1$.
- Therefore $N_G(H) = C_G(H)$.
- Suppose we know $H \triangleleft G$, then $G = C_G(H)$.
- So element $g \in G$ commutes with every $h \in H$.
- Therefore $H \le Z_(G)$.

DEF: Let $H$ and $K$ be groups with $\phi \colon K \to \Aut{H}$ a homomorphism. The semidirect product $K \ltimes_\phi H$ induced by $\phi$ is ... the cartesian product $K \times H$ equipped with multiplication $(k, h)(k', h') = (kk', h[\phi(k)(h')])$.

What if $\ker\phi = \mathrm{id}_K$? 

- then $K \ltimes_\phi H \cong K \times H$, and 
- the "twist" is straightened out for free, $\phi(k)(h') = h'$

Do we have a different semidirect product for different automorphisms? 

- Yes, provided that $H$ and $K$ are not already nested in a larger group.
- If $H, K \le G$ are already subgroups with $K \le N_{G}(H)$, then the action of $K$ on $H$ will necessarily be by conjugation.

To list examples.

- $D_{2n} = C_n \rtimes_\phi C_2 = \langle r \rangle \rtimes \langle s \rangle$ 

      - define $\phi \colon \langle s \rangle \to \Aut{\langle r \rangle}$ by $\phi(s)(r) = r^{-1}$

- the wreath product
- upper triangular matrices
- $S_n = A_n \rtimes C_2$

    - Consider $S_n \ge A_n$. 
    - Does $A_n$ have a complement? 
    - Yes, it's $C_2  = \langle (1,2) \rangle$, the set of coset representatives of $S_n / A_n$.

- $\abs{G} = pq$ with $p < q$ primes and $q \equiv 1 \mod p$.

    - Let $G = P \times Q$, $P \in \Syl q G$, and $Q \in \Syl q G$.
    - Consider $\phi \colon P \to \Aut{Q} \cong C_{q-1}$.
    - Since $P$ is simple $\ker \phi = P$ or $1$.
    - If $\ker \phi = P$, then $G \cong P \times Q$.
    - Else if $\ker \phi =1$, all the non-abelian semidirect products are isomorphic.

#### Classification theorems revisited

Recall the familiar setup, where $G$ is a group of order $\abs{G} = pq$ and $p < q$ are primes. There exist Sylow subgroups $H_p$ and $H_q$ of order $p$ respectively $q$ (with $H_q \triangleleft G$).

- As a *set*, with $\langle \sigma \rangle = H_q$ and $\langle \tau \rangle = H_p$, we have $G = H_p H_q = \{\tau^a \sigma^b : 0 \le a \le p, 0 \le b \le q\}$. 
- *Why?* Consider that $G = \bigcup_{ 0 \le a \le p} \tau^a H_q.$
- We want to show the cosets are distinct.
- Let $\tau, \tau' \in H_p$, and suppose that $\tau H_q = \tau' H_q$. 
- Then $\tau(\tau')^{-1} \in H_q$.
- Therefore $\tau(\tau')^{-1} \in H_q \cap H_p = \{1\}$.

To construct a group, all we need to do is devise a multiplication for $(\tau^a \underbrace{\sigma^b)(\tau^{a'}}_{\text{to commute?}}\sigma^{b'})$. 

- Now the Sylow subgroup $H_q$ for the bigger prime $q$ is normal in $G$.
- So $\tau\sigma\tau^{-1} = \sigma^a$ as an element of $H_q$.
- Hence $\tau\sigma = \sigma^a\tau$.
- We see that $a \in \ZZ$ determines the group!
- In general, $a^p \equiv 1 \mod q$.

For example, suppose $\abs{G} = 2 \times q$. 

- Then $H_q  = \langle 1, \sigma, \sigma^2, \sigma^{q-1} \rangle$, and
- $H_p = \langle 1,   \tau \rangle$.
- Either $\tau \sigma \tau^{-1} = \sigma$ and $G \cong \ZZ/2q\ZZ$.
- Or     $\tau \sigma \tau^{-1} = \sigma^{-1}$ and $G \cong D_{2q}$.

    - To wit, $\tau^2 \sigma \tau^{-2} = \tau(\sigma^a)\tau^{-1} = \underbrace{\sigma^a \cdots \sigma^a}_{\text{$a$ times}} = \sigma^{a^2}$.
    - On the other hand, $\tau^2 = e$, so $\sigma^{a^2} = \sigma$.
    - Thus $a^2 \equiv 1 \mod q$ and so $a \equiv \pm 1 \mod q$.

        - Where $q | a^2 - 1$ iff $q | (a-1)(a+1)$.

Further in this direction?

- Coxeter presentations
- classification of groups of order $12$
- intuition for semidirect products

(We also introduced subgroup series, but I've moved those notes to next week.)

#### Review

To list concepts I struggled with.

- applications of Sylow's theorem
    - what helped was reviewing proofs from Thiem, from [@DF04], from Artin, from Gross, from Judson.
- timeliness, to some extent
- getting buried in lecture notes
    - wriggled out of this one by [writing a script](https://github.com/coltongrainger/dotfiles/blob/master/.local/bin/scripts/revcat.sh) to compile and view specified date ranges as single pdfs

Over the weekend, I caught up with [Benedict Gross's lectures](http://www.math.harvard.edu/archive/122_fall_03/), namely:

- Week 6. Isometries of plane figures. Cyclic and dihedral groups. Finite and discrete subgroups of symmetry groups.
- Week 7. Group actions. Basic properties and constructions. Groups acting on themselves by left multiplication. Groups acting on themselves by conjugation.
- Week 8. A5 and the symmetries of an icosahedron. Sylow theorems. Study of permutation groups.
- here's a [study-sheet](http://courses.dce.harvard.edu/%7Emathe222/study-sheet.pdf) for that course

### Week 9: Nilpotence, series again, and finitely generated abelian groups

We had a definition quiz on

- subgroup
- [composition series](https://en.wikipedia.org/wiki/Composition_series)
- derived series
- semi-direct products

DEF: A normal series is ... a chain of subgroups of a group $G$, with least element $\{e\}$ and greatest element $G$, such that each intermediate term is normal in the next.

DEF: A normal series $$\{e\} = G_0 \triangleleft G_1 \triangleleft \cdots \triangleleft G_n = G$$ is said to be nontrivially refinable if ... a factor $G_{i+1}/ G_i$ is not a simple group, as then we may find a nontrivial normal subgroup $N/G_i$ for which $G_i \triangleleft N \triangleleft G_{i+1}$.

DEF: A composition series is ... an unrefinable normal series that includes no repetitions.

Open question: How is one to construct subgroup series?

- <https://groupprops.subwiki.org/wiki/Inductive_proof_methods_for_the_ascending_series_corresponding_to_a_subgroup-defining_function>
- we either ask for subquotients (as with the upper central series)
- or specify the subgroups (e.g., some characteristic subgroups)

From Keith Conrad's [Subgroup series I](http://www.math.uconn.edu/~kconrad/blurbs/grouptheory/subgpseries1.pdf), our motivation is

- to generalize the commutator subgroup with 
  
    - the derived series $G^{(i)}$
    - the lower central series $\gamma_i(G)$

        - both define a chain of subgroups starting at $G$ and tending *down lower* to $\{e\}$
        - the lower central series stabilizes at the *hypocenter*
        - the intersection of all numbers of the derived series is a group's [perfect core](https://groupprops.subwiki.org/wiki/Perfect_core)

- and to generalize the center $Z(G)$ with

    - the upper central series $Z_i$

        - which defines a chain of subgroups starting at $\{e\}$, tending *on upwards* to $G$, and stabilizing at the *hypercenter*.

#### Derived series

- <https://groupprops.subwiki.org/wiki/Derived_series>

DEF: For $j \in \ZZ_{\ge 0}$, let $G^{(0)} = G$, and $G^{(j)} = [G^{(j-1)},G^{(j-1)}]$. The derived series of $G$ is ... $G = G^{(0)} \triangleright \ldots \triangleright G^{(j)} \triangleright \ldots \triangleright \{1\}$.

- we're as greedy as possible, choosing large commutators for small abelian subquotients (?)

THM: A group is solvable iff ... $G^{(m)} = \{1\}$ for some $m \in \ZZ_{\ge 0}$.

#### Upper central series

DEF: For $j \in \ZZ_{\ge 0}$, let $Z_0(G) = \{1\}$, and $Z_j(G) = \pi^{-1}(Z(G/Z_{j-1}(G)))$. The upper central series of $G$ is ... $G = Z_0(G) \triangleleft Z_1(G) \triangleleft \ldots \stackrel{?}{=} G$. (Either the series terminates at $G$ or stabilizes.)

- e.g., the upper triangular matrices over $\FF$ have a terminating upper central series

DEF: A group $G$ is nilpotent with nilpotent class $c$ if ... $Z_c (G) = G$ and $Z_{c-1}(G) \neq G$.

EX: The upper triangular matrices $UT_n(\FF)$ are nilpotent with nilpotent class ... $n-1$.

- In fact, if $\FF$ is a finite field, then $UT_n(\FF)$ is a $p$-subgroup, so we get nilpotence from a more general result.
- TODO: show the special linear matrices are trivially nilpotent.

#### Lower central series

DEF: The lower central series of $G$ is the sequence $G = G_0 \triangleright G_1 \triangleright \ldots $ where ... $G_j = [G, G_{j-1}]$ and $G_0 = G$.

- The lower central series might be thought "more likely to stall out" when compared to the derived series.

- The upper series completes iff lower central series completes.

For the group of upper triangular matrices, $UT_4(\FF)$, the upper and lower central series are the same up, to reversing the order.

THM: Let $G$ be a group. (a) If $\gamma_c(G) = \{1\}$ for some $c \in \ZZ_{\ge 0}$, then $G$ is [...]; (b) Moreover $\gamma_c(G) = \{1\}$ iff [...]. ... $G$ is nilpotent; the upper central series terminates $Z_c(G) = G$.

*Proof sketch.* 

- (a) follows from (b).
    - TODO (see notes 2018-10-24 #1)

- For (b), assume $G$ is nilpotent with nilpotence class $c$. 
- We'll show that $\gamma_j(G) \subset Z_{c-j}(G)$.
- We induct on $\gamma_j(G)$ for $j \ge 0$. 
    - TODO (see notes 2018-10-22 #2)

#### Structure of $p$-groups

THM: If $G$ is a nontrivial $p$-group, then the center ... $Z(G) \neq 1$.

THM: If $G$ is a $p$-group and $H \triangleleft G$ is a nontrivial normal subgroup, then $H$ meets ... the center nontrivially $H \cap Z(G) \neq 1$.

THM: If $G$ is a $p$-group, $H \triangleleft G$, and $p^a$ divides the order of $H$, then $H$ has a subgroup ... of order $p^a$.

THM: If $G$ is a $p$-group and $H < G$ is a proper subgroup, then the normalizer $N_G(H)$ of $H$ in $G$ is strictly ... larger than $H$.

THM: If $G$ is a $p$-group and $H < G$ is maximal, then ... $H \triangleleft G$.

*Proof sketch.* TODO (see notes 2018-10-22 #3)

FACT: If $p$ is the least prime dividing the order of $G$, then any subgroup $H$ of index ... $p$ is normal in $G$.

*Proof sketch.* TODO

#### Structure of nilpotent groups

THM: Let $G$ be a finite group. TFAE: (a) $G$ is nilpotent; (b) if $H < G$ is a proper subgroup, then so too $H < N_G(H)$ (properly); (c) if $Q \in \Syl p G$, then $Q \triangleleft G$; (d) [...] ... if $p_1 < p_2 < \ldots < p_\ell$ are the primes dividing $\abs{G}$, and $Q_j \in \Syl{p_j}{G}$, then $G \cong Q_1 \times Q_2 \times \cdots \times Q_\ell$.

<!---

THM: Let $G$ be a finite group. TFAE: (a) [...]  (b) if $H < G$ is a proper subgroup, then so too $H < N_G(H)$ (properly); (c) if $Q \in \Syl p G$, then $Q \triangleleft G$; (d) if $p_1 < p_2 < \ldots < p_\ell$ are the primes dividing $\abs{G}$, and $Q_j \in \Syl{p_j}{G}$, then $G \cong Q_1 \times Q_2 \times \cdots \times Q_\ell$. ... $G$ is nilpotent;

THM: Let $G$ be a finite group. TFAE: (a) $G$ is nilpotent; (b) [...]  (c) if $Q \in \Syl p G$, then $Q \triangleleft G$; (d) if $p_1 < p_2 < \ldots < p_\ell$ are the primes dividing $\abs{G}$, and $Q_j \in \Syl{p_j}{G}$, then $G \cong Q_1 \times Q_2 \times \cdots \times Q_\ell$. ... if $H < G$ is a proper subgroup, then so too $H < N_G(H)$ (properly);

THM: Let $G$ be a finite group. TFAE: (a) $G$ is nilpotent; (b) if $H < G$ is a proper subgroup, then so too $H < N_G(H)$ (properly); (c) [...] (d) if $p_1 < p_2 < \ldots < p_\ell$ are the primes dividing $\abs{G}$, and $Q_j \in \Syl{p_j}{G}$, then $G \cong Q_1 \times Q_2 \times \cdots \times Q_\ell$. ... if $Q \in \Syl p G$, then $Q \triangleleft G$;  
--->

*Proof sketch.* TODO (see notes 2018-10-24, 2--3)

CORO: If $G$ is abelian and finite, then it's the direct product of ... its Sylow subgroups.

#### Frattini argument

PROP: (Frattini argument) Let $G$ be finite and $H \triangleleft G$. For $P \in \Syl p H$, we have that ... ($\abs{G/H}$ divides $\abs{N_G(P)}$ and) $G = HN_G(P)$.

*Proof sketch.* TODO (notes 2018-10-26)

CORO: A finite group $G$ is nilpotent iff all its maximal subgroups are ... normal.

#### Elementary abelian $p$-groups

DEF: A finite abelian $p$-group $A$ is elementary if ... $a^p = 1$ for all $a \in A$. (We view elementary abelian $p$-groups as a vector space over $\FF_p$).

PROP: If $A$ is elementary abelian and $a \in A$, then there exists $A' \le A$ such that ... $A \cong A' \times \langle a \rangle$.

*Proof sketch* TODO (notes 2018-10-26)

CORO: IF $A$ is an elementary abelian $p$-group (of order $p^n$), then $A$ is isomorphic to ... $\underbrace{C_p \times \cdots \times C_p}_{n \text{ times}}$.

THM! (FTFGAG) Let $A$ be an abelian group of order $$p_1^{k_1}p_2^{k_2}\cdots p_\ell^{k_\ell}$$ with $p_1 < \ldots < p_\ell$ primes. Then (a) $$A \cong A_1 \times A_2 \times \cdots \times A_\ell$$ with $\abs{A_j} = p_j^{k_j}$, (b) for each $1 \le j \le \ell$ there's an integer partition $\lambda$ of $k_j$ such that ... $$A_j \cong C_{p_j}^{\lambda_1} \times C_{p_j}^{\lambda_2} \times \cdots \times C_{p_j}^{\lambda_r}.$$

*Proof sketch* TODO (notes 2018-10-26)

#### Review

To list concepts I struggled with.

- Applying Frattini's argument.

### Week 10: Sylow theory for medium order, Free groups

\providecommand{\N}[2]{N_{ #1 }\left( #2 \right)}

We had a definition quiz on 

- quotient group
- center
- nilpotent
- elementary abelian

#### Techniques for groups of medium order

0. Factor into primes and obtain $n_{p_i}$ for all $p_i \mid G$
1. Count elements
2. Exploit subgroups of small index
3. Permutation representations
4. Playing $p$-groups off each other
5. Studying normalizers of intersections of Sylow $p$-groups

To outline absolutely fundamental points we'll leverage later. Let $H_p \le G$ be a Sylow $p$-subgroup of $G$. Then:

- $H_p$ is normal in $G$ iff $n_p(G) = 1$.
    - Consider that $V_4 \triangleleft A_4$ as $n_2(A_n) = 1$.

-  $[G : \N G {H_p}] = n_p(G)$.
    - Consider that $[A_4 : H_3] = n_3(A_4) = 4$.

-  If $\abs{G} = pm$ for prime $p \nmid m$, then the number of elements of order $p$ in $G$ is $n_p(G)(p-1)$.
    - The number of order $3$ elements in $A_4$ is $n_3(A_4)(3-1) = 8$.

> Exploiting subgroups of small index.

PROP: If $G$ is a simple group, why does $\abs{G} \mid n_p!$ for all $p \mid \abs{G}$? ... Let $G$ act on the coset space $G/N_G(H_p)$ nontrivially. Suppose $\phi \colon G \to S_{n_p}$ is the permutation representation. Since $G$ is simple, $\ker \phi = \{1\}$ and so $G \le S_{n_p}$. By Lagrange, $\abs{G} \mid n_p!$.

PROP: If $G$ is a finite simple group and $k$ is the least integer such that $\abs{G} \mid k!$, then ... $G$ contains no *proper* subgroups of index less than $k$, via Cayley and Lagrange.

> Permutation representations, working in the alternating group.

PROP: Let $G \le S_k$. If $G \le A_k$, then ... $\abs{G \cap A_k} = \abs{G \setminus A_k}$.

PROP: Let $G \le S_k$. If $G$ has no index $2$ subgroup, then ... $G \le A_k$.

PROP: Let $G \le S_k$. If $P \in \Syl p {S_k}$ and $p$ is an odd prime, then ... $P \in \Syl p {A_k}$ and $\frac12 \abs{ N_{S_k}(P) } = \abs{ N_{A_k}(P)}$.

> Playing p-groups off eachother.

LEMMA: Let $p \mid \abs{G}$ and $p^e \mid \abs{P / (P \cap Q)}$ for all $P, Q \in \Syl p G$ with $P \neq Q$. Then ... $\Syl p G \equiv 1 \mod p^e$.

*Proof sketch.* (See notes 2018-10-29 #4)

CORO: If $\abs{\Syl p G} \not\equiv 1 \mod p^2$, then there exists $P, Q \in \Syl p G$ with $P \neq Q$ and ... $\abs{\frac{P}{P\cap Q}} = P$.

LEMMA: Let $p < q$ with $q \not\equiv 1 \mod p$. Let $p \in \Syl p G$ and $Q \in \Syl q G$ with $\abs{P} = p$ and $\abs{Q} = q$. If $p \mid \abs{N_G(Q)}$, then ... $q \mid \abs{N_G(P)}$.

*Proof sketch.* (It's pretty slick. Just a diagram. See 2018-10-29 #5.)

#### Free groups

During the discussion of free groups, I was reminded of Jorge Luis Borges's *Library of Babel* <https://libraryofbabel.info/libraryofbabel.html>.

> To construct a vector space, we merely insist that some set is a basis for a vector space.

DEF: Let $S$ be a set. The free group $F(S)$ is the unique group such that ... (F1) there's an injective function $\iota \colon S \to F(S)$ and (F2) if $G$ is a group and $\tau \colon S \to G$, there's a unique homomorphism $\pi \colon F(S) \to G$ such that $\pi \circ \tau = \tau$.

- Uniqueness and existence are not obvious. 

- We've defined $F(S)$ with a universal property alone. (Though, some constructive schema should fall out of the requirement, just as we have the [product topology generated by a subbase](topology#new-spaces-from-old-products)).

- We say $F(S)$ has minimal relations by (F2).

- If $\tau$ is injective and $G = \langle \tau(S) \rangle$, then $G \cong F(S) / \ker \pi$.

> What should we add to a set in order to produce a free object in the category?

We defined $F(S)$ as the set of words $W(S \sqcup S^{-1})$ together with the appropriate binary operation and reduction. Uniqueness follows from the universal property.

#### Presentations

DEF: A presentation $\langle S \vert R \rangle$ of a group $G$ is a subset $S \subset G$ and a subset $R \subset F(S)$ such that ... if $N \triangleleft F(S)$ is the smallest normal subgroup of $F(S)$ that contains $R$, then $G \cong F(S) / N$. 

> It's tricky to find $N$---we want $\pi$ to have kernel generated by $R$. 
>
> How to find $N$ such that $G \cong F(S)/N$ is abelian? $N$ had better be large...
>
> Is $F(S)$ simple? No. Even if $\abs{S} = 1$, then $F(S) \cong \ZZ$, which is not simple.

IDEA: The commutator group in $F(S)$ for $\abs{S} > 1$ is ... nontrivial.

EX: The presentation of the dihedral group as $\langle S | R \rangle$ is ... $\langle \{r, s\} | \{r^n, s^2, srsr\}\rangle$.

What $N$ is generated by $r^n, s^2, srsr$? It's a pain to actually show.

Check this definition: 

- <https://www.encyclopediaofmath.org/index.php/Coxeter_group>
- <https://groupprops.subwiki.org/wiki/Coxeter_group>

DEF: A Coxeter group $G$ is a group with a subset $S \subset G$ such that $$G = \langle S | \{(st)^{m(s,t)}: s, t \in S, m(s,t) \in \NN, m(s,s) = 1 \forall s \in \S\} \rangle.$$

EX: What's the Coxeter presentation for $S_n = \langle s_1, \ldots, s_{n-1} \rangle$ where the $s_i$ are simple transpositions $s_i = (i, i+1)$? ... Consider three cases: $s_i^2 =1$ (transpositions invert themselves), $s_is_j = s_js_i$ if $\abs{i - j} > 1$ (they commute if disjoint), $s_is_{i+1}s_i = s_{i+1}s_is_{i+1}$ (they satisfy the braid relation). Whence define the Coxeter matrix $m(s_i, s_i) = 1$, $m(s_i, s_j) = 2$, and $m(s_i, s_{i+1}) = 3$.

EX: What's the Coxeter presentation of $D_2n$? ... It's generated by two elements $\langle s, t \rangle$ subject to a Coxeter matrix  of the form $$\begin{pmatrix} 1 & n \\ n & 1 \\\end{pmatrix}.$$

> The group of symmetries of a coin stack (i.e., the wreath product with a cyclic group $C_n$ acting on $S_n$) admits a Coxeter presentation.

#### Category of Rings

(Notes 2018-11-02)

#### Review

What did I struggle with?

- Splitting attention between summative review and new material.
    - Having a long back-log of proofs to-do taxes me whenever I start into new (i.e., *current*) material.

- Prof Stange described "getting one's sea-legs", which I think for me will look something like:
    - *more urgently* dealing with topical material, 
    - wherever possible, making *executive* summaries,
    - knowing how to stash away interesting problems for later,
    - prioritizing applications over explorations or refinement of already solid material,

- Chris described the tendency (in problem solving) to make a straightforward application of the given definitions as "being dense, using brute force". 

To take some motivation for brute force from Brian Conrad's <http://math.stanford.edu/~conrad/210APage/> Math 210A syllabus:

> This material is **absolutely basic** for anything in advanced pure mathematics which involves algebraic concepts. This course will move rapidly, so please **don’t let yourself fall far behind.**

### Week 11: Rings and Ideals

DEF! A ring $R$ is a set with two functions $$\cdot \colon R \times R \to R \quad \text{and}\quad + \colon R \times R \to R$$ such that ... (R1) $(R, +)$ is an abelian group, (R2) multiplication is associative, (R3) for $r,s,t,v \in R$ we've $(r + s)(t + v) = rt + rv + st + sv$.

DEF! A ring homomorphism $\phi \colon R \to S$ is a function from a ring $R$ to a ring $S$ such that ... for each $r, s \in R$, $\phi(rs) = \phi(s)\phi(r)$ and $\phi(r + s) = \phi(r) + \phi(s)$.

DEF! The kernel of a ring homomorphism is ... the preimage of the additive identity.

DEF! A ring $R$ is said to be commutative if ... $rs = sr$ for all $r, s \in R$.

DEF! Let $\{X_i\}_1^n$ be a set of indeterminants, and let $R$ be a commutative ring with identity. Consider the monoid $S  = \prod_1^n \{X_i^r : r \ge 0\}$. We define the set of polynomials $B[X_1, \ldots, X_n]$ as ... the set of functions $S \to R$ which are equal to $0$ except for a finite number of elements of $S$.

We further defined: 

notation | set
--- | ---
$R(x_1, \ldots, x_n)$ | the ring of polynomials including negative powers of $x_1, \ldots, x_n$
$R[x_1, x_2, \ldots]$ | $\cup_{n \ge 0} R[x_1, \ldots, x_n]$
$R[[x_1, \ldots, x_n]]$ | the ring of [formal power series](https://en.wikipedia.org/wiki/Formal_power_series) allowing infinite sums, not infinite products
$R((x_1, \ldots, x_n))$ | the ring of [formal Laurent series](https://en.wikipedia.org/wiki/Formal_power_series#Formal_Laurent_series)

Why should we care?

> When is the root of a polynomial in $R[x]$ in $R$? What if $R = \FF$ is a field?

From [@La05, II.3]:

> There are polynomials over a finite field which cannot be identified with polynomial functions in that field. One needs polynomials with integer coefficients, and one needs to reduce these polynomials mod $p$ for primes $p$. One needs polynomials over arbitrary commutative rings, both in algebraic geometry and in analysis, for instance the ring of polynomial differential operators.

#### Ring actions

Recall if $G$ acts on a set $A$, we obtain a homomorphism $G \to S_A$. In general, however, rings *don't* act one sets.

- What should the addition of two functions be?
- The symmetric group doesn't have two operations available---just one, that's composition.

DEF! If $A$ is an abelian group, then an action of $R$ on $A$ is a function $R \times A \to A$ such that ... for all $r,s \in R$ and all $a \in A$ (A1) $r(s(a)) = (rs)(a)$, (A2) $(r+s)(a) = r(a) + s(a)$, (A3) if $1 \in R$ then $1(a) = a$.

\providecommand{\Hom}[1]{\mathrm{Hom}\left( #1 \right)}
\providecommand{\End}[1]{\mathrm{End}\left( #1 \right)}

Notably, $\Hom{A, A} = \{ \text{group endomorphisms from $A$ to $A$}\}$ is a ring and we've a ring homomorphism (multiplication as composition, addition as sums of images) $\phi \colon R \to \Hom{A,A}$. 

DEF! A ring action on a vector space $V$ is ... a ring homomorphism $\phi \colon R \to \End{V}$.

Examples:

- matrix groups from group actions on vector spaces
    - We'll define matrix group from *ring* actions on vector spaces.
- endomorphisms of vector spaces
    - For a given vector space $V$, let $\End{V}$ be the set of linear transformations $\{ \phi : \phi \colon V \to V\}$.
    - If we specify a basis of $V$, then $\End{V} \cong M_{\dim V}(\FF)$.
- group rings
    - $R \rtimes_\phi G := \{ \sum_{g\in G} r_g g : r_g \in R\}$ 
    - It's a ring of formal linear combinations! (If $\abs{G} = \infty$ we require all but finitely many coefficients to be $0$.)
    - Here's addition $\sum_{g \in G} r_g g + \sum_{g \in G} s_g g = \sum_{g \in G}(r_g + s_g) g$.
    - Here's multiplication $\left(\sum_{g \in G} r_g g\right)\left(\sum_{h \in G} s_h h\right) = \sum_{k \in G} \left(\sum_{g \in G} r_g \phi(g)(s_{g^{-1}k})\right) k$ where $k = gh$.
    - If $G \le \ker \phi$, then we commute ring elements. Else the action of $G$ on $R$ requires us to twist elements of $R$ past elements of $G$.
        - In this case we merely write $RG$ for  $R \rtimes_\phi G$.
    - When $R = \FF$ is a field and $G \le \ker \phi$ then we've a "group algebra".
        - It's a vector space with basis $G$.
        - (A vector space with a ring is an algebra?)
        - Studying the actions of groups on vector spaces is equivalent to the study of the action of $\FF G$ on vector spaces.

#### Elements in Rings

In general if $r \in R$, then $r$ is not necessarily (multiplicatively) invertible (especially if $R$ fails to contain the multiplicative identity $1$).

DEF! If $R$ is a ring with unity $1$, then $R^\times$ is ... $\{r \in R : r^{-1} \in R\}$, the group of invertible elements.

\providecommand{\sM}{\mathscr{M}}

EX! What's $\sM_n(\FF)^\times$? ... It's just $\mathrm{GL}_n(\FF)$.

On the other extreme.

DEF! A zero divisor $r \in R$ is a nonzero element for which ... there's a nonzero element $s \in R$ such that either $rs = 0$ or $sr = 0$.

- In this case $s$ is also a zero divisor.
- If $r \in \RR^\times$, then $r$ is not a zero divisor.
- The converse fails to hold, e.g., consider the units $\{\pm\} =  \ZZ^\times$ of $\ZZ$, an integral domain.

Two examples of zero divisors:

- For $A = \begin{pmatrix}0 & 1\\ 0 & 0\end{pmatrix} \in \sM_2(\FF)$, $AA = \begin{pmatrix}0 & 0\\0 &0 \end{pmatrix}$.
- In a group ring $\ZZ G$, $(1- h)\sum_{g \in G} g = 0$.
    - Note that in a group ring the identity is $1_R \cdot 1_G = 1$.

EX! What's the group ring $\ZZ\ZZ$? ... It's the set of formal Laurent series with integer coefficients, $\left\{ \sum_j n_j x^j : \text{$n_j = 0$ for all but finitely many $j$}\right\}$.

note that the group elements and the ring elements don't interact---it's a *formal sum*.

DEF! A ring $R$ with a unit $1$ is an integral domain if it's commutative and has no zero divisors.

- the integers $\ZZ$
- if $R$ itself is an integral domain, then the ring of polynomials $R[x]$ is too
    - $\ZZ[x_1, \ldots, x_n]$

DEF! (From the integral domain perspective) A field $\FF$ is a ... commutative ring with unity and $\FF^\times = \FF \setminus \{0\}$.

PROP! If $R$ is a finite integral domain, then ... $R$ is a field.

*Proof sketch.* (2018-11-05 #4)

Fields are fairly well-behaved, and we'll see more of them in Algebra II.

#### Substructures

DEF! Let $S$ be a ring. An additive subgroup $R \subset S$ is a subring if $r \cdot t \in R$ for all $r, t \in R$. (Note Thiem doesn't require that subrings have units!)

For groups there was a distinguished class of subgroups called normal subgroups---they allowed construction of quotient subgroups, whence composition series and so on. What's the analogue of a normal subgroup in the category of rings? Well, what are the kernels of ring homomorphisms?

In vector spaces, the kernel of a linear transformation is a *subspace*. Moreover, all subspaces of a given vector space can be written as the kernel of some linear transformation. A "quotient" in the category of vector spaces is the *orthogonal complement*.

DEF! The kernel, denoted $\ker \phi$, of a ring homomorphism $\phi \colon R \to S$ is the subring $\ker \phi = \{r \in R: \phi(r) = 0\}$.

- Under the convention that rings have an identity, then $\ker \phi$ is not generally a subring.
- Kernels of ring homomorphisms have stronger "normality" properties than we'd expect from our intuition with normal subgroups.

### Week 12: Broken hand

While biking to class the morning after finishing the problem set for *Further Topics in Group Theory* (Ch 6), I took a spill and [fractured the fifth metacarpal](https://www.orthobullets.com/hand/6037/metacarpal-fractures) in my right hand. Boo. Chris and Hunter allowed me to take copies of their notes until I had a wrist brace that I could write with (around 2018-11-15). I ended up taking off the brace early (around 2018-11-26 as the bone had mended into an alignment that was good enough for me) so that I could type unobstructed. However, having my dominant hand wrapped up for a solid 20 days put into focus the utter amount of bullshittery I had been using it for. I'll share a few observations, seeing as they're meta-relevant to the style of these notes:

- javascript for mathjax loads *way too slow* for this page to be useful to me
- I *scarcely* used mnemosyne as I had hoped to
    - rote memorization turns out to be [mildly ill-advised](http://math.colorado.edu/~kstange/gradstudy.pdf)
    - I think I did a fine job writing up prompts, but the workflow (notes to cards to review) was just *way too infrequent* to be useful, 
    - e.g., I *needed* my notes *right away* to complete the weekly assignments
- so why the big fuss to get it all typed up? 
    - why not just [work by hand](https://usesthis.com/interviews/jean.yang/)? 
    - there are anyways *[lovely](https://postalco.net/onlineshop/20124_regular/)* A5 notebooks from Postalco
    - see also [Oliver Smithies' notebooks](https://smithies.lib.unc.edu/notebooks)

I have no good answers, aside from a (very) weak appeal to the longevity of digital content and its accessibility.

Anyways, I'm not going to run these notes to Week 16 (their expected completion). The gap from 2018-11-07 until 2018-12-01 can be summarized: 

    - [@DF04, chapters 7, 8, 9]
    - polynomial rings in Lang's *Undergraduate Algebra*
    - more lectures from Benedict Gross

<!---
In algebra: We defined a principal ideal, a finitely generated ideal, a maximal ideal, and a prime ideal. We recognize when an ideal is generated by a set in three different ways: Firstly, we recognize an ideal is generated if any ideal contained in the generated ideal and containing the generating set is equal to the generated ideal. Secondly, we can think of a generated ideal is a finite sum of products of  elements in the ring and elements in the set in a certain order such that the generated ideal is closed under multiplication from the left and the right by any element in the ring. Thirdly we can think of the generated ideal as the intersection of all ideals containing the set. 

Nathaniel introducing  Zorn's Lemma as a means to show that every ideal proper is contained in the maximal ideal. As familiar from Benedict's lectures the direct sum of finitely many principle ideals in the ring of integers is just the ideal generated by their greatest common divisor. One should consider the quotient of a ring by  both maximal and prime ideals. Quotients by maximal ideals create fields and quotients prime ideas create integral domains. It's necessary and sufficient. In a finite field prime and maximal ideals coincide.

As far as the broken hand goes, I'm contemplating some workflow involving voice to text,  structural macros for the proofs, as well as  symbol free sections, which are for whatever  statements definitions I might need to expand on later.  I'm not remapping my keyboard because it is such a hassle to get X-monad to work right in the first place. Today I listened to Philip Guo’s  podcast about slowing down or How I broke my foot. Turns out wrist injuries are deplorable for computer scientists---I don't think they're that bad  in mathematics. Especially because the quality of output for first-year students is not expected to be great. I think it's important for first-years  to assimilate content in whatever personal synthetic manner also decently reflects the curriculum on the syllabi for the preliminary exams.

I'm concerned that the written assignments are too high fidelity to be adequately handled without a dominant right hand. Some of the exploration, the indices, the finicky multiplication is best seen written out. Hence “manipulating equations”. For this I really do miss working at a chalkboard with my dominant hand and typing up the solutions in vim.

I'm working a bit with my left hand on the rest of the algebra assignment which lo and behold is a bunch of polynomial manipulation---indices all over the place and my handwriting is s***.
---> 

### Week 16: "Dead week"


Let's talk about *sets*, baby. (Problem sets.)

To scaffold myself, here's a series of exams meant to be taken by advanced undergrads. (Anyways, I'm a fan of each author's writing; each of these packets are slick.)

- James McKernan
    - [18.703 exams](https://github.com/coltongrainger/fy19alg1/search?q=filename%3A18703&unscoped_q=filename%3A18703)
- Hiro Lee Tanaka
    - [Fall 2014 Math 122 exams](https://github.com/coltongrainger/fy19alg1/search?q=filename%3A2014-fall*&unscoped_q=filename%3A2014-fall*)
- Ravi Vakil
    - [Math 120 exams](https://github.com/coltongrainger/fy19alg1/search?q=filename%3Avakil&unscoped_q=filename%3Avakil) (no solutions)
- Evan Dummit
    - [Summer Enhancement Program 2014](https://github.com/coltongrainger/fy19alg1/search?q=filename%3A2014_algebra_sep*&unscoped_q=filename%3A2014_algebra_sep*)

Measuring with Dummit and Foote: we made it to Gauss' lemma and the Eisenstein criterion. That's just chapter 1--9. Pretty canonical. Everything above should be approachable. What's below is a little denser---meant for drilling.

- J.A. Beachy
    - [A Study Guide for Beginners](http://www.math.niu.edu/~beachy/abstract_algebra/review/contents.html)
    - [Review Problems on Groups and Galois Theory](http://www.math.niu.edu/~beachy/abstract_algebra/guide/contents.html)
- James Wilson
    - [Algebra quals notes](http://www.math.colostate.edu/~jwilson/math/Algebra.pdf)
- [CU Algebra prelims 2006 and older](https://github.com/coltongrainger/fy19alg1/search?q=filename%3Acu-boulder&unscoped_q=filename%3Acu-boulder)
    - The solutions are *gross* (just hardcopies in MATH 350).
