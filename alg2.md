---
title: Modern Algebra 2
author: Colton Grainger
date: 2018-12-01
nonumbering: true
bibliography: /home/colton/coltongrainger.bib
---

\setcounter{section}{-1}

\providecommand{\ZZ}{\mathbf{Z}}
\providecommand{\QQ}{\mathbf{Q}}
\providecommand{\RR}{\mathbf{R}}
\providecommand{\CC}{\mathbf{C}}
\providecommand{\NN}{\mathbf{N}}
\providecommand{\FF}{\mathbf{F}}
\providecommand{\sK}{\mathscr{K}}
\providecommand{\sM}{\mathscr{M}}
\providecommand{\sP}{\mathscr{P}}
\providecommand{\abs}[1]{\left\lvert #1 \right\rvert}
\renewcommand{\phi}{\varphi}
\renewcommand{\emptyset}{\varnothing}
\providecommand{\Hom}{\operatorname{Hom}}
\providecommand{\End}{\operatorname{End}}

## MATH 6140 Syllabus 

Instructor: [Dr. Richard Green](https://math.colorado.edu/~rmg/)

Website: <https://math.colorado.edu/~rmg/6140/>

Git repo: <http://github.com/coltongrainger/fy19alg2>. 

Here're the changes I hope to make in contrast with my Algebra 1 notes.

- More discussion, reflection, narration, and reference. 
- Less mathjax bloat, rote memorization, agony.

### Grading

The total grade is out of 500.

- 14 Assignments. 100 points. Best 10 of 14 count. Should be conceptual, long, and belabouring as practice for the midterms. Only 3 problems graded.
- 2 Midterms. 100 points each. Weeks 5 and 10. Should be preparation for the final.
- Final. 200 points. 2019-05-07 4:30pm. Should be preparation for the prelim. 

### Textbooks

- Dummit and Foote chapters 10 -- 14 is canonical. 
    - We're encouraged to stick to it, with the goal of stating the fundamental theorem of Galois theory. I asked about supplemental reading, yet was discouraged apparently because Dummit and Foote is just *so big*. Regardless.

- Topics in Algebra, Herstein
- Elements of Modern Algebra, Hu
- Finite Dimensional Vector Spaces, Halmos
- Algebra, Hungerford
- Undergraduate/Graduate Algebra, Lang

### Prerequisites

Here are exams from Algebra 1, Fall 2017, the last time Dr. Green instructed: [ring theory](http://math.colorado.edu/~rmg/6130/p6130f.pdf), [further topics group theory](http://math.colorado.edu/~rmg/6130/p6130b.pdf), and [basic group theory](http://math.colorado.edu/~rmg/6130/p6130a.pdf).

I talked a bit with Dr. Thiem about preparing for modules, field theory, Galois theory, etc. Our consensus: one must *know* linear algebra. (One can never know enough linear algebra!) 

The [undergraduate handbook](https://warwick.ac.uk/fac/sci/maths/undergrad/ughandbook/year3/ma377/) for MA337 the University of Warwick suggests:

> MA106 Linear Algebra, familiarity with elementary group theory and the ring theory part of MA249 Algebra II: Groups and Rings is desirable.

### Prelim exam topics

Here's an outline for questions 4--6 on the CU algebra prelim exam. See also [the first half](alg1).

We should expect, according to Dr. Green:

prelim problem | topic | DF04 chapter
--- | --- | ---
4 | canonical forms | 12
5 | field theory | 13
6 | Galois theory | 14

- Modules and linear algebra

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
    - ~~language of categories and functors~~
    - minimal polynomial of a transformation
    - Cayley-Hamilton theorem over a commutative ring
    - direct sums and products
    - ~~free, projective, injective modules~~
    - duality
    - multilinear forms
    - determinants
    - canonical forms
        - Jordan
        - rational
        - primary rational
    - invariant factors
    - elementary divisors
    - ~~localization of modules~~

- Field theory

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

- Additional Algebra

    - applications of Zorn’s lemma
    - tensor products
        - algebras
    - chain conditions
        - Artinian and Noetherian rings and modules
        - Hilbert basis theorem
    - Nullstellensatz

## Week 1

### Intuition and axioms

From Herstein.

> Solutions to physical and geometric problems are often parameterized as vector spaces.

IDEA: What homomorphisms exist from an $\FF$-vector space $V$ to itself? ... Each nonzero $\alpha \in \FF$ defines $v \mapsto \alpha v$, an injective linear transformation $V \to V$.

From Green.

> We have a module $M$ for a ring $R$, where if $R = F$ is a field, then $M$ is a vector space.

SLOGAN: Modules are generalizations of both ... abelian groups and vector spaces.

Modules impose additional structure on abelian groups.

object | structure | morphisms
--- | --- | ---
topological spaces | their open sets | continuous maps
groups  | their binary operations | group homomorphisms
abelian groups  | commutative binary operations | group homomorphisms
vector spaces | fields acting on abelian groups | linear transformations
modules | rings acting on abelian groups | $R$-linear transformations

Or, from the perspective of representation theory.

algebraic structure | representation object | action
--- | --- | ---
$G$, a group | $A$, a $G$-set | $g.v \in A$, a group action
$F$, a field | $V$, a vector space | $\lambda.v \in V$, scalar multiplication 
$R$, a ring | $M$, a module | also scalar multiplication

(A fourth item could go on this list, but I'm not sure where. How do [groups with operators](https://en.wikipedia.org/wiki/Group_with_operators) resemble vector spaces? "A group with operators is also a mapping $\Omega\rightarrow\operatorname{End}_{\mathbf{Grp}}(G),$ where $\operatorname{End}_{\mathbf{Grp}}(G)$ is the set of group endomorphisms of $G$.")

We want *four conditions* for the (left) action of a ring $R$ on a abelian group $M$. With $m, m_1, m_2$ arbitrary in $M$ and $r, r_1, r_2$ arbitrary in $R$ it should be that

1. $(r_1 +_R r_2).m = r_1.m +_M r_2.m$, e.g., acting then adding scalars in $R$ is the same as adding then acting;
2. $(r_1 r_2).m  = r_1.(r_2.m)$, which gives a left module action;
3. $r.(m_1 +_M m_2) = r.m_1 +_M r.m_2$, e.g., acting then adding scalars in $M$ is the same as adding then acting.;
4. $1_R.m = R$, forcing unital modules for the course to avoid pathologies (the categories are cleaner?).

EX: In $\sM_n(\RR)$, what's the significance of $\text{diag}(1, \ldots, 1, 0)$? ... It's idempotent.

EX: Say $S$ is entire and $\phi \colon R \to S$ is a ring homomorphism. What is  $\phi(1_R)$? ... It's idempotent in $S$, so either $0$ or $1$.

Right modules are just left modules in a mirror. In particular, left and right modules coincide when the ring $R$ acting is commutative.

### Examples

To work with a category of modules, we have to fix a ring. Here are rings we'll commonly see acting on abelian groups.

- fields $\FF$ (maybe finite), 
- the integers $\ZZ$, 
- and PIDs $\FF[x]$.

EX: If $\FF$ is a field, any unital module $M$ over $\FF$ is a vector space. Conversely if an $R$-module $M$ is a vector space, then ... $R = \FF$ is a field acting by scalar multiplication.

EX: Let $F$ be a field and $V = F[x]$; ignoring polynomial multiplication, $V$ is a vector space over $F$.

EX: Let $\mathcal{P}_n \subset F[x]$ be the set of polynomials of degree less than $n$. Then $\mathcal{P}_n$ is a ... vector space over $F$, in fact isomorphic to $F^n$.

NONEX: $\ZZ/3\ZZ$ is *not* a module over $\QQ$.

EX: $\ZZ$-modules are the same as ... abelian groups.

PROP: The action of $\ZZ$ on $A \in \text{AbelianGp}$ is completely determined by ... our unital ring axiom for modules, $1.a = a$ for all $a \in A$.

Here's a safe place to practice "extending linearly".

- We've setup by axiom that $1.a = a$.
- Mixing additive and multiplicative structures, both $0.a = 0_A$ and $(-1).a = -a$.
- $\ZZ$ has a single generator, so by induction and with distributivity, for each $n \in \ZZ$, we determine $n.a$.
- Lastly, we check the ring axioms hold for $m, n \in \ZZ$ in cases by trichotomy.

PROP: Suppose $M$ is a left $R$-module. Say $\phi \colon S \to R$ is a unital ring homomorphism. We have $M$ as an $S$-module by defining $S \times M \to M$ such that ... $s.m = \phi(s).m$.

Here's a monomorphism between rings: $S \hookrightarrow R$.

EX: When $S \le R$ is a unital subring, $R$ can be seen as ... an $S$-module, with $S$ acting by left multiplication $s.r = sr$. 

Considering the action of a subring is dubbed "restricting scalars". E.g., $\RR \le \CC$, so while $\CC$ is a $\CC$-vector space of dimension $1$, we had a different object $\CC$ as an $\RR$-vector space of dimension $2$, with generators $i$ and $1$. 

Conversely, given an $S$-module and $S \le R$ as rings, extending to an $R$-module is difficult. (Unlike passing from an entire ring to it's field of fractions. Someone mentioned not every abelian group is a vector space. I don't see immediately what their comment portends.)

CAUTION: A submodule $N$ of an $R$-module $M$ is not obtained by ... restricting scalars. 

Rather, in the language of linear algebra, we have to trim down the set of *vectors* to obtain *linear subspaces*.

EX: Name a subgroup of a vector space that's not a linear subspace. ... the lattice $\ZZ^2$ is a subgroup of $\RR^2$ yet not a subspace.

Now consider an epimorphism of rings: for a two sided ideal $I \triangleleft R$, the natural projection $\phi \colon R \to R/I$. In these clean circumstances, any $R/I$ module can be recognized as an $R$-module by lifting $r.m = (r+I).m$. 

EX: In one word explain both how any $\ZZ/n\ZZ$-module is a $\ZZ$-module and any $F[x]/(x)$ module is an $F[x]$-module. ... Lifting.

IDEA: Suppose $M$ is an $R$-module and $I \triangleleft R$. Can we make $M$ into an $R/I$ module via $(r + I).m = r.m$? ... iff $I$ annihilates $M$. 

DEF: We say an $R$-module $M$ is annihilated by an ideal $I \triangleleft R$ when ... for all $m \in M$ and $i \in I$, $i.m = 0$.

As an aside, Green posed:

- How is one to construct an finite field of characteristic $p$? 
- Why are there no finite fields of order $p^n m$ where $p$ is prime and $\gcd(p, m) = 1$. 
    - Hint: count column vectors.

To borrow the statement of the problem from <https://math.stackexchange.com/questions/1942821>. (See also <https://proofwiki.org/wiki/Field_of_Prime_Characteristic_has_Unique_Prime_Subfield>.)

> Let $F$ be a field. The intersection of all subfields of $F$ is a subfield which is isomorphic to $\mathbb{Q}$ if $\operatorname{char}(F)=0$, and isomorphic to $F_p$ if $\operatorname{char}(F)=p$.

Green argued: any field is a vector space over any of its subfields. We'll eventually show a field of order $p^n$ exists for all $p$ prime and $n \in \NN$, and that each field of order $p^n$ is unique.

### $F[x]$-modules

EX: $\FF$-vector spaces $V$ equipped with a linear transformation $T \colon V \to V$ are the same as $F[x]$-modules, knowing ... how each constant polynomial $\lambda \in F \subset F[x]$ and the indeterminate $x$ act.

*Proof sketch.* 

- ($\Rightarrow$) Consider an $F[x]$-module $M$. By restriction to constant polynomials, $M$ is seen to be an $F$-vector space. Let $\alpha, \beta \in F$ be constant polynomials, let $m,n \in M$, and let $x$ be the indeterminate. Observe that $x$ acts linearly on each $F$-linear combination: $$x.(\alpha.m + \beta.n) = x.(\alpha.m) + x.(\beta.n) = \alpha x.m + \beta x.n.$$

- ($\Leftarrow$) Conversely, say we're given an $F$-vector space $V$ and a linear map $T\colon V \to V$. Let $u,v \in V$ and $\alpha, \beta \in F$. By induction, if $T^{n-1}$ is linear, then $$T^n(\alpha u + \beta v) = T ( \alpha T^{n-1}(u) + \beta T^{n-1}(v) ) = \alpha T^n(u) + \beta T^n(v),$$ whence $T^n$ is linear. 

- Define an action of $\{x^n : n \in \NN\}$ on $V$ by $x^n.v = T^n(v)$, then extend this definition linearly to obtain an action of $F[x]$ on $V$. Knowing that compositions, sums, and $F$-scalar multiples of the linear transformation $T$ are $F$-linear, we can prattle off a verification of the module axioms. 

    - $(V, +)$ is an abelian group. 
    - $F[x]$ is a unital ring. 
    - For any $p(x), q(x) \in F[x]$, and any $u,v \in V$, the action $F[x] \times V \to V$ satisfies

        - $p(x).(u + v) = p(x).u + p(x).v$ (by linearity)
        - $p(x)q(x).(u) = p(x).(q(x).u)$ (visibly)
        - $( p(x) + q(x) ).u = p(x).u + q(x).u$ (also visibly)
        - $1.u = u$ (from the vector space axioms). 

NONEX: Consider the non-ring $C(\RR)$ endowed with pointwise addition and composition as multiplication. That $(\sin \theta + \cos \theta)^2$ and $\sin^2 \theta + \cos^2 \theta = 1$ are not identical functions violates which ring axiom? ... Distributivity of multiplication over addition.

So $F[x]$-modules encode vector spaces and their endomorphisms. Why do we care? Well, the machinery of undergraduate linear algebra cannot answer "are these two matrices similar?" With it, we could find traces, determinants, characteristic polynomials, and yet could not hope to determine 

> Given $A, B \in \sM_n(\FF)$ does there exist $P \in \sM_n(\FF)$ such that $A = PAP^{-1}$?

Apparently the problem is tractable in the language of rings and modules. 

- Consider a basis, then compare $A$ and $B$ as linear transformations of the $\FF$-vector space $V \to V$. 

We'll have to develop a sufficiently general theory for $R$-linear maps between modules.

- What should a *canonical form* for matrices look like?
    - e.g., Diagonal matrices, Jordan normal form, Smith normal form
    - see <https://en.wikipedia.org/wiki/Category:Matrix_normal_forms>

Sam asked: How far is it possible to demonstrate that $R[x]$-modules for a commutative ring $R$ have the same properties as $F[x]$-modules? (See <https://math.berkeley.edu/~gbergman/ug.hndts/mH113_D+F_exs.ps> for an alternative development of the ring of fractions, which seems to build machinery to work with $R$-linear combinations, dropping the condition that $F$ is a field.) TODO

### Duality

After my office-mate Ulrich gave me a little introduction to the interplay between Gabor transforms and locally compact abelian groups, I think it's safe to quote [“module in nLab”](https://ncatlab.org/nlab/show/module). Retrieved January 26, 2019. “Motivation for and role of modules: generalized vector bundles”:

> The theory of monoids or rings and their modules, its "meaning" and usage, is naturally understood via the duality between algebra and geometry:
> 
> 1. a ring $R$ is to be thought of as the ring of functions on some space,
> 
> 1. an $R$-module is to be thought of as the space of sections of a vector bundle on that space.
> 
> A classical situation where this correspondence holds precisely is topology, where
> 
> 1. the Gelfand duality theorem says that sending a compact topological space $X$ to its C-star algebra $C(X,\mathbb{C})$ of continuous functions with values in the complex numbers constitutes an equivalence of categories between compact topological spaces and the opposite category of commutative $C^\ast$-algebras;

### Submodules

SLOGAN: A submodule is a subgroup that's ... stable under the ring action.

Given a subset $N$ of a unital $R$-module $M$, we need only check 

- For each pair $n_1, n_2 \in N$, we have additive closure $n_1 + n_2 \in N$ (so $N$ is an additive monoid).
- For each $r \in R$, and each $n \in N$, we have closure under the ring action $r.n \in N$.
    - Since $R$ is a unital ring, closure under the ring action gives $-1.n = -n \in N$,
    - in which case $N$ is an abelian subgroup of $M$.

EX: Consider a unital ring $R$ as a module over itself. What are the submodules of $R$? ... Exactly the ideals $\mathfrak{a}_i \subset R$.

In an $F[x]$-module, the $F$-subspaces are not necessarily $F[x]$-submodules. But here's an example in which the categorical subobjects coincide [@DF04, number 10.1.20].

- *Given.* Let $F = \RR$, let $V = \RR^2$, and let $T$ be the linear transformation from $V$ to $V$ that is rotation clockwise about the origin by $\pi$ radians. 
- *To demonstrate.* Every subspace of $V$ is an $F[x]$-submodule for this $T$.
- *Demo.* Say $\RR^2$ is an $\RR[x]$-module with the action of $x \in \RR[x]$ given by $$x.v = Av \quad \text{ where } \quad A = \begin{bmatrix} -1 & 0 \\ 0 & -1\end{bmatrix} \quad \text{ w.r.t. the standard basis.}$$ The property of being an $\RR[x]$-submodule is stronger than that of being an $\RR$-linear subspace, so the submodules of $\RR^2$ are all subspaces. Conversely, if $V \subset \RR^2$ is a subspace, then $V$ is an abelian group. For any $v \in V$, the image of $v$ under the action of $x$ is $x.v = -v$. So $V$ is stable under the linear transformation; whence $V$ is an $\RR[x]$-submodule.

This exhibits a rather stupid phenomenon. From the PCM [@GBLP08, section III.43], in discussion of Jordan Normal Form

> Is every matrix diagonalizable? Over the reals, the answer is no for uninteresting reasons, since there need not even be any eigenvectors: for example, a rotation in the plane clearly has no eigenvectors. So let us restrict our attention to matrices and linear maps over the complex numbers.

### Generating sets of a module

(It seems to me, after revision, that the arguments in this section are cyclic. I'll likely revisit the discussion of direct sums and direct products in Week 2 or 3.) Recall that extending linearly is just appealing to the universal property of free objects. Beaudry sets up the process as follows:

> If $S$ is a set and $A$ is an abelian group, then there's a bijection $$\{\text{Functions $S \to A$}\} \leftrightsquigarrow \{\text{Homomorphisms $\ZZ\{S\} \to A$}\},$$ which sends $g \colon S \to A$ to $$\left(\sum_{s \in S} n_s s\right) := \sum_{s \in S}n_s g(s).$$ We call this *extending linearly*.

To consider *generated submodules*, we'll pull a number of equivalent characterizations from <https://en.wikipedia.org/wiki/Generating_set_of_a_module> and [@Lan02, section III.3]:

DEF: Let $M$ be a module over a ring $R$, let $S \subset M$. We say $N$ is the submodule of $M$ generated by $S$ (denoted $M\{S\}$ or $M\langle S\rangle$) when ... $N$ is the set of all $R$-linear combinations $$\sum_{x \in S} r_x x \subset M$$ of elements in $S$.

SLOGAN: A generating set $G$ of a module $M$ over a ring $R$ is ... a subset of $M$ such that the smallest submodule of $M$ containing $G$ is $M$ itself.

PROP: A subset $G$ generates an $R$-module $M$ iff there's a surjection ... $$\bigoplus_{g \in G} R \to M, \, r_g \mapsto r_g g.$$

DEF: A module $M$ is said to be finitely generated (or of finite type, or finite over $R$) if ... it has a finite number of generators.

Here's a finite coproduct of modules. (And it should feel like Euclidean space.)

EX: For a unital ring $R$, we can view the abelian group $\bigoplus_1^n R := R^n$ as a left $R$-module by ... defining $r.(a_1, \ldots, a_n) = (r.a_1, \ldots, r.a_n)$.

Regarding "rank", we'll borrow definitions from <https://ncatlab.org/nlab/show/rank>.

DEF: For a unital ring $R$ and an $R$-module $M$, we say that $M$ has a basis $\{e_i\} \subset M$ if ... for each $m \in M$ there's a unique set $\{\alpha_i\} \subset R$ such that $\alpha_i = 0$ for all but finitely many $i$ and $m = \sum_i \alpha_i e_i$.

DEF: If an $R$-module $M$ has a basis, it's called ... a free module (over $R$). 

DEF: If the cardinality of a basis $\{e_i\}$ for an $R$-module $M$ is independent of choice of basis, then $\abs{\{e_i\}}$ called ... the rank of $M$ over $R$.

DEF: A subset $S$ of a module $M$ is linearly independent (over $R$) if whenever we have a linear combination $\sum_{x \in S} r_x x$ that's equal to zero, then ... $r_x = 0$ for all $x \in S$. [@Lan02, ch. III.3]

Green cautioned us not to assume we would always be working with invariant basis number rings, and, in the case that we are, to at least be wary of zero divisors when finding unique $R$-linear combinations. He mentioned that finding such combinations is easy when the ring $R$ is an integral domain, as then we can work in the field of fractions. (See also <https://math.stackexchange.com/questions/220186/ideas-of-linear-independence-in-the-context-of-modules-and-vector-spaces>.)

EX: If we consider $\ZZ$ as a module over itself, what's a set that spans $\ZZ$ but does not contain a basis? ... $\{2,3\}$.

EX: With $\ZZ$ as a module over itself, what's a linearly independent set that cannot be extended to a basis? ... $\{2\}$.

EX: List the linearly independent subsets of $\ZZ/n\ZZ$ as a $\ZZ$-module. ... Just $\emptyset$.

### Factor modules

Lecture ended with "the standard yoga" of defining the quotient in the category of modules.

IDEA: The ring action $r.(m +N)$ of $R$ on the equivalence classes $M/N$ is well defined iff ... $N$ is a submodule of $M$.

*Proof.* 20 push-ups.

PROP: Let $M$ be a module with submodule $N$. The canonical additive group homomorphism $$f \colon M \to M/N$$ is also a module homomorphism; it is universal in the category of ... homomorphisms of $M$ whose kernel contains $N$. [@Lan02, ch III.3]

We stated the rank-nullity theorem for maps tween finite dimensional vector spaces, then proved it by decategorifying the "ammo built up" in the definition of a quotient module.

### Algebras

To list definitions for algebras. (It's convenient to assume in this setting that both the rings and the ring homs are unital.)

DEF: For a comm. unital ring $R$, an $R$-algebra is a unital ring $A$ with ... a unital ring hom $f \colon R \to A$ such that $f(R) \subset Z(A)$.

We can quotient by the kernel to obtain the working definition.

SLOGAN: An $R$-algebra is a unital ring $A$ with ... $R$ at its center.

Green also set out a (provisionally) equivalent definition.

DEF: For a comm. unital ring $R$, an $R$-algebra is an $R$-module with ... an $R$-bilinear associative multiplication $$r.m \times s.n = (rs).mn.$$

NONEX: Why is $\RR^3$ with a bilinear multiplication defined by the cross-product not an $\RR$-algebra? ... Because cross-products are not associative. 

- The field $F \hookrightarrow F[x]$, so the PID $F[x]$ is an $F$-algebra.
- For $G$ a finite group and $R$ a comm. unital ring, the *group ring* $RG$ is an $R$-algebra. 
    - In fact $RG$ is a free $R$-module, where any element of $RG$ is a linear combination $\sum_{g \in G} r_g g$. 
    - With $R$ in the center of $RG$, the bilinear product is well defined.
    - See [comments from Thiem](/alg1#ring-actions) on group rings.

Green asked: what's the dimension of the center of $\CC G$? Here's a hint from [@DF04, number 7.2.13].

- *Given.* Let $\sK$ be one of the conjugacy classes (which will be denoted $\sK_1, \ldots, \sK_r$) of the finite group $G$. Let $R$  be a commutative ring with unity. Consider the group ring $RG$, with center $Z = Z(RG)$.
- *To demonstrate.* (a) $K = \sum_{k_i \in \sK} k_i \in Z$. (b) $\alpha \in Z$ if and only if $\alpha = \sum a_iK_i$ for $a_i \in R$.
- *Demo.* 

    (a) Each element $\sum r_gg \in RG$ commutes with $K$ if and only if $gK = Kg$ for all $g \in G$. The conjugation action of $G$ on its powerset $\sP(G)$ is an inner automorphism on elements, so the conjugacy class $\sK$ is fixed. Because $G$ is finite, conjugation permutes the elements in $\sK$. Thus $gKg^{-1} = K$. 

    (b) Suppose $\alpha = \sum a_iK_i$. Then $$\sum_i a_iK_i\sum_g r_g g = \sum_i \left( \sum_g r_g a_i K_i g \right) = \sum_i \left( \sum_g r_g a_i g K_i \right) = \sum_g r_g g\sum_i a_iK_i$$ so $\alpha \in Z$. 
    
        Conversely, say $\alpha \in Z$. We can write $\alpha$ as the sum over conjugacy classes $\{k_{n_i}\}$ of elements in $G$: $$\alpha = \sum_i \left(\sum_{n_i} a_{n_i} k_{n_i}\right).$$ For each $i$, $G$ acts transitively on by conjugation on $\{k_{n_i}\}$. Fix $i$. For all $n_i$, transitivity of conjugation implies $a_{n_i} = a_i$ for some $a_i \in R$. We conclude $\alpha = \sum a_i K_i$.

## Week 2

### Categorification

I'm now confused. Do we generalize to modules (from vector spaces and abelian groups) in order to *decategorify* or *categorify*? To give *proof* seems an act of decategorification:

- Taking the smooth chain rule from Banach spaces down to $\RR^n$. [@AE08, ch. VII]
- Arguing that $\dim_V = \dim W + \dim V/W$ is a special case of $\dim V = \dim \ker f + \dim \mathrm{im} f$ by taking for $f$ the canonical map. [@Lan02, III.5]

I feel I have some practice in this direction. On the other hand, I'm not at all sure how to categorify, especially after considering the argument in [“What is Categorification? | The n-Category Café”](https://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html).

DEF: To categorify a set $S$ is to find a category $C$ and a function $p \colon \mathrm{Decat}(C) \to S$. What's $\mathrm{Decat}$? ... It's the set of isomorphism classes of objects of $C$.

EX: How to categorify the natural numbers with the category of finite sets? ... Use cardinality.

EX: How to categorify the natural numbers with the category of finite-dimensional vector spaces? ... Use dimension.

EX: If we categorify the natural numbers to the category of finite sets, addition gets categorified to ... disjoint union.

EX: How did Emmy Noether categorify the concept of Betti number? ... With $\NN$, the category of finitely generated abelian groups, and the rank function.

Green mentioned that so far we're working in *concrete categories*. E.g., categories where we may pretend that the objects are sets, and that the morphisms are set functions with additional properties. Well, it's about time to define the additional properties for maps between modules.

### Homomorphisms

DEF: By a module-homomorphism one means a map $f \colon M \to M'$ of one module into another (over the same ring $R$), which is ... an additive group homomorphism, and such that $f(rx) = rf(x)$ for all $r \in R$ and $x \in M$. [@Lan02, ch. III.1]

To call attention to the parent ring of the category, we may also refer to module homomorphisms as $R$-linear maps, or $R$-homomorphisms. For example, it's necessary to distinguish $F$-linear and $F[x]$-linear maps. Say that $M, N$ are $F$-vector spaces and we're given $F$-linear endomorphisms 
\begin{align*}
S &\colon M \to M, \, S(m) =: x.m\\
T &\colon N \to N, \, T(n) =: x.n
\end{align*}
In terms of $S$ and $T$, what should we expect from an $F[x]$-homomorphism $\phi \colon M \to N$? Green argued that $\phi$ will have to "intertwine the action of the ring", e.g., $$\phi((x^3 + x).m) = T^3(\phi(m)) + T(\phi(m)).$$ 

PROP: If $\phi \colon M \to N$ is a module homomorphism between $F[x]$-modules $M$ and $N$ with endomorphisms $S$ and $T$ respectively, sketch the commutative square for $\phi$. ... $$\begin{CD} M @>{\phi}>> N\\ @VV{S}V @VV{T}V\\ M @>{\phi}>>N \end{CD}$$

(Knowing the square commutes, we might also see $M$ and $N$ sequences of vector spaces with $S$ and $T$ transition maps, such that $\phi$ is a homomorphism between the sequences.)

Green mentioned that in algebra, inverses of bijective homomorphisms are usually homomorphisms in turn, whereas in $\mathsf{Top}$ the inverse of a continuous bijection need not be continuous. Whence:

DEF: A module isomorphism is a ... bijective module  homomorphism (as the inverse function will always be a module hom).

PROP: A module hom $\phi \colon M \to N$ between $F[x]$-modules with endomorphisms $S$ and $T$, is an isomorphism if and only if ... $\phi^{-1} \circ T \circ \phi = S$.

DEF: Say $M, N$ are $R$-modules. Declare $\Hom_R(M, N)$ to be ... the set $\{\phi \colon M \to N : \phi \text{ is $R$-linear}\}$.

PROP: $\Hom_R(M, N)$ is an abelian group, where the sum of $f, g \in \Hom_R(M, N)$ is defined ... pointwise, $(f+g) \colon m \mapsto f(m) + g(m)$.

PROP: Say $R$ is a commutative unital ring. $\Hom_R(M, N)$ is an $R$-module, where $r \in R$ acts on $f \in \Hom$ by ... $r.f \colon m \mapsto r.(f(m))$. 

PROP: Under composition, if $f \in \Hom_R(M,N)$ and $g \in \Hom_R(N, L)$, then $g \circ f$ is in ... $\Hom_R(M, L)$, i.e., $R$-module homomorphisms are morphisms in the category $\mathsf{Rmod}$.

PROP: How is $\End_R(M)$ a unital (perhaps non-commutative) ring? ... $\End_R(M)$ is an abelian group, with addition pointwise. Multiplication of $f, g \in \End_R(M)$ is given by function composition $gf = g \circ f$.

PROP: Why, if $R$ is a commutative unital ring, is $\End_R(M)$ an $R$-algebra? ... We can map $\phi \colon R \to \End_R(M)$ by $\phi \colon r \mapsto r.\mathbf{1}_M$ into the center of $\End_R(M)$.

From [@Lan02, section III.2]

IDEA: We can also view $\Hom_R$ as a functor. Let $X, X', Y$ be in $\mathsf{Rmod}$ and let $X' \xrightarrow{f} X$ be an $R$-linear map. Then we get an induced homomorphism ... $$\Hom_R(f, Y) \colon \Hom_R(X, Y) \to \Hom_A(X', Y)$$ (reversing the arrow!) given by $g \mapsto g \circ f$.

IDEA: To visualize $\Hom_R$ as a functor $$\Hom_R(f, Y) \colon \Hom_R(X, Y) \to \Hom_A(X', Y)$$ given by $g \mapsto g \circ f$, consider ... $$X' \xrightarrow{f} X \xrightarrow{g} Y.$$

### Isomorphism theorems

> I know nothing more contemptible in a Writer than the Character of a Plagiary; which he here fixes at a venture, and this, not for a Passage, but a whole Discourse, taken out from another Book only *mutatis mutandis.* [1710 Swift Tale Tub (ed. 5) Author's Apology]

IDEA: (Isomorphism theorems in $\mathsf{Rmod}$) Given the corresponding isomorphisms in $\mathsf{Ab}$, just check that ... they're $R$-linear.

PROP: Say $N \le M$ as $R$-modules and we define $\pi_N \colon x \to x + N$. There's a bijection between ... $\{ \text{submodules $N$ of $M$} \} \leftrightsquigarrow \{\text{isom classes of $R$-hom images of $M$}\}$.

PROP: (Rmod iso I) Say $N \le M$ as $R$-modules and $\pi_N \colon x \to x + N$. We have a short exact sequence ... $0 \to N \to M \xrightarrow{\pi} M/N \to 0$.

To mash up Stange's lecture with Lang's exposition [@Lan02, section III.1]

THM: (Rmod iso II) Let $N$ and $N'$ be two submodules of a module $M$. Then $N + N'$ is also a submodule, and we have an isomorphism ... $$N/(N \cup N') \cong (N + N')/N'.$$

*Proof.* Noting the quotient is well defined, the map $\phi \colon N \to (N + N')/N'$ such that $n \mapsto n + N'$ is [isomorphism of abelian groups](alg1#isomorphism-theorems). Let $r \in R$. Does $\phi$ intertwine the action of the ring? Yes, because $$\phi(r.n) = r.n + N' = r.(n + N') = r.\phi(n).$$

THM: (Rmod iso III) If $M \supset M' \supset M''$ are modules, then we needn't ever think about ... $(M/M'')/(M'/M'')$, because it's isomorphic to $M/M'$.

*Proof.* The map $\phi \colon M/M' \to M/M''$ such that $m + M' \mapsto m + M''$ is an [additive homomorphism](alg1#isomorphism-theorems) with $\ker \phi = M'/M''$. To verify $\phi$ is $R$-linear, take any $r \in R$ and observe $\phi(r.(m + M')) = r.m + M'' = r.(\phi(m + M'))$.

THM: (Rmod iso IV) If $f \colon M \to M'$ is a module-homomorphism, and $N'$ is a reference submodule of $M'$, then $f^{-1}(N')$ is a submodule of $M$ and we have a canonical injective homomorphism ... $\bar{f} \colon M/f^{-1}(N') \to M'/N'$, which is an isomorphism if $f$ is surjective.

Sam ended class with a brainteaser (which Wise happened answer on [mathoverflow in 2009](https://mathoverflow.net/a/47)).

> Can a vector space over an infinite field be a finite union of proper subspaces?

## Week 3

EX: (Decategorification) Let $k$ be a field, let $V$, $W$ be finite $k$-vector spaces. Why should $$\dim(V + W) = \dim(V) + \dim(W) - \dim(V \cap W)?$$ ... Note $$\frac{V + W}{V} = \frac{W}{V \cap W}$$ and apply rank-nullity.

Again, I asked "what's categorification?" Green remarked, to start, it takes *skill*. He gave us a combinatorial example.

EX: (Categorification) By argument with red and blue balls, why is $$2^n = \sum_{k=1}^n {n \choose k}?$$ ... There are $2^n$ distinct arrangements of $n$ balls (either blue or red), which can be found by counting arrangements contiguously from a ratio of $0:5$ red/blue balls up to $5:0$.

### Sums and linear combinations

Green asked us to "show some constraint" when summing. (But, my dude, can't we sum two elements from a product of infinitely many abelian groups?)

IDEA: Infinite linear combinations often should be accompanied with (what? why?) ... a topology, to determine whether a sequence of partial sums converges.

DEF: Consider a finite collection $\{N_i\}_1^k$ of submodules of $M$. The sum $N_1 + \ldots + N_k$ is defined to be ... the submodule $\{n_1 + \ldots + n_k : n_i \in N_i\}$.

IDEA: The sum of submodules is analogous to ... the span of a set of vectors.

- We won't (necessarily) be able to find a linearly independent spanning set.
- Moreover, a module $M$ need not have a minimal generating set.
- Lastly, if a module *does* have a minimal generating set, then perhaps another exists with different cardinality.
    - TODO *How*?

PROP: Let $N\subset M$ be $R$-modules. Then $RN$ is the smallest submodule of $M$ containing $N$. Give two constructions of $RN$. ... Either form $R$-linear combinations or intersect all submodules containing $N$.

EX: For $R \in \mathsf{CRing}$, $R$ is a module over itself. What are the cyclic submodules of $R$? ... They're the principal ideals of $R$.

PROP: If $R \in \mathsf{CRing}$ is seen as a module over itself, then $x$ in $R$ is a unit iff ... $R = R\{x\}$ (i.e., $\{x\}$ is a generating set for $R$).

construction | called what in $\mathsf{Gp}, \mathsf{Ab}$ | application
--- | --- | ---
products | direct products | power series
coproducts | direct sums | polynomials

## Week 4

Taking a pause.

