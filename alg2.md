---
title: Modern Algebra 2
author: Colton Grainger
date: 2018-12-01
nonumbering: true
---

\setcounter{section}{-1}
\providecommand{\ZZ}{\mathbf{Z}}
\providecommand{\RR}{\mathbf{R}}
\providecommand{\CC}{\mathbf{C}}

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

### Intuition

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

### Axioms

We want *four conditions* for the (left) action of a ring $R$ on a abelian group $M$. With $m, m_1, m_2$ arbitrary in $M$ and $r, r_1, r_2$ arbitrary in $R$ it should be that

1. $(r_1 +_R r_2).m = r_1.m +_M r_2.m$, e.g., acting then adding scalars in $R$ is the same as adding then acting;
2. $(r_1 r_2).m  = r_1.(r_2.m)$, which gives a left module action;
3. $r.(m_1 +_M m_2) = r.m_1 +_M r.m_2$, e.g., acting then adding scalars in $M$ is the same as adding then acting.;
4. $1_R.m = R$, forcing unital modules for the course to avoid pathologies (the categories are cleaner?).

<!---
EX: In $\sM_n(\RR)$, what's the significance of $\text{diag}(1, \ldots, 1, 0)$? ... It's idempotent.
EX: Say $S$ is entire and $\phi \colon R \to S$ is a ring homomorphism. What is  $\phi(1_R)$? ... It's idempotent in $S$, so either $0$ or $1$.
--->

Right modules are just left modules in a mirror. In particular, left and right modules coincide when the ring $R$ acting is commutative.

### Canonical examples

To list archetypical rings that we'll see everywhere acting on abelian groups:

- fields $\FF$ (maybe finite), 
- the integers $\ZZ$, 
- and the PID $F[x]$.

EX: If $\FF$ is a field, any unital module $M$ over $\FF$ is a vector space. Conversely if an $R$-module $M$ is a vector space, then ... $R = \FF$ is a field acting by scalar multiplication.

EX: Let $F$ be a field and $V = F[x]$; ignoring polynomial multiplication, $V$ is a vector space over $F$.

EX: Let $\mathcal{P}_n \subset F[x]$ be the set of polynomials of degree less than $n$. Then $\mathcal{P}_n$ is a ... vector space over $F$, in fact isomorphic to $F^n$.

NONEX: $\ZZ/3\ZZ$ is *not* a module over $\QQ$.

EX: $\ZZ$-modules are the same as ... abelian groups.

PROP: The action of $\ZZ$ on $A \in \text{AbelianGp}$ is completely determined by ... our unital ring axiom for modules, $1.a = a$ for all $a \in A$.

In this safe space, it's good to practice "extending by linearity".

- We've setup by axiom that $1.a = a$.
- Mixing additive and multiplicative structures, both $0.a = 0_A$ and $(-1).a = -a$.
- $\ZZ$ has a single generator, so by induction and with distributivity, for each $n \in \ZZ$, we determine $n.a$.
- Lastly, we check the ring axioms hold for $m, n \in \ZZ$ in cases by trichotomy.

Prior to a discussion of $F[x]$-modules, we really ought to define the maps between modules as objects. It's foreseeable that some maps won't be onto, so we'd also better define our subobjects.

### Changing scalars and trimming vectors

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


### $F[x]$-modules

EX: $\FF$-vector spaces $V$ equipped with a linear transformation $T \colon V \to V$ are the same as $F[x]$-modules, knowing ... how each constant polynomial $\lambda \in F \subset F[x]$ and the indeterminate $x$ act.

$F[x]$-modules encode vector spaces and their endomorphisms. Why do we care? Well, the machinery of undergraduate linear algebra cannot answer "are these two matrices similar?" With it, we could find traces, determinants, characteristic polynomials, and yet could not hope to determine 

> Given $A, B \in \sM_n(\FF)$ does there exist $P \in \sM_n(\FF)$ such that $A = PAP^{-1}$?

Apparently the problem is tractable in the language of rings and modules. One needs only to consider a basis, then compare $A$ and $B$ as linear transformations of the $\FF$-vector space $V \to V$. Along the way, we'll develop a sufficiently general theory with $R$-modules.

TODO: How far is it possible to demonstrate that $R[x]$-modules for a commutative ring $R$ have the same properties as $F[x]$-modules? (See <https://math.berkeley.edu/~gbergman/ug.hndts/mH113_D+F_exs.ps> for an alternative development of the ring of fractions, which seems to build machinery to work with $R$-linear combinations, dropping the condition that $F$ is a field.)

