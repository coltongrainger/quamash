---
title: Modern Algebra 2
author: Colton Grainger
date: 2018-12-01
---

\setcounter{section}{-1}

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

We should expect, according to Dr. Green, 

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

### Introduction

To take intuition from Herstein.

> Solutions to physical and geometric problems are often parameterized as vector spaces.

IDEA! What homs exist from an $\FF$-vector space $V$ to itself? ... Each nonzero $\alpha \in \FF$ defines $v \mapsto \alpha v$, an injective linear transformation $V \to V$.

- How are [groups with operators](https://en.wikipedia.org/wiki/Group_with_operators) related to vector spaces?

    > A group with operators is also a mapping $$\Omega\rightarrow\operatorname{End}_{\mathbf{Grp}}(G),$$ where $\operatorname{End}_{\mathbf{Grp}}(G)$ is the set of group endomorphisms of $G$. 

- Let $F$ be a field and $V = F[x]$; ignoring polynomial multiplication, $V$ is a vector space over $F$.
- Let $\mathcal{P}_n \subset F[x]$ be the set of polynomials of degree less than $n$. Then $\mathcal{P}_n$ is a vector space over $F$, in fact isomorphic to $F^n$.

SLOGAN! Modules are generalizations of both ... abelian groups and vector spaces.

Modules impose additional structure on abelian groups. Impressionistically:

object | structure | morphisms
--- | --- | ---
topological spaces | their open sets | continuous maps
groups  | their binary operations | group homomorphisms
abelian groups  | commutative binary operations | group homomorphisms
vector spaces | fields acting on abelian groups | linear transformations
modules | rings acting on abelian groups | $R$-linear transformations

TODO: how far is it possible to demonstrate that $R[x]$-modules for a commutative ring $R$ have the same properties as $F[x]$-modules? (See <https://math.berkeley.edu/~gbergman/ug.hndts/mH113_D+F_exs.ps> for an alternative development of the ring of fractions, which seems to build machinery to work with $R$-linear combinations, dropping the condition that $F$ is a field.)

