---
title: Analysis for prelims
author: Colton Grainger
date: 2018-08-27
---

## Exam syllabus

### Calculus

- foundations
    - properties of ordered fields
    - functions and graphs
    - limits and continuity
    - images of compact maps
    - "[three hard theorems](http://homepages.math.uic.edu/~marker/mtht530/)"
- elementary functions
    - convexity and concavity
- derivatives and integrals
    - parametric representation of curves
    - Riemann sums
    - Fundamental theorem of calculus
- implicit and inverse function theorems
- infinite sequences and infinite series
    - approximation by polynomial functions
    - uniform convergence and power series
    - manipulating sequences of functions

### Metric spaces

- basic properties
    - completeness
    - compactness
    - connectedness
- metrizable topological spaces
- equicontinuous families of functions
- the Arzela-Ascoli Theorem
- the Stone-Weierstrass Theorem

### Lebesgue measure and integration

- measurable sets
- Lebesgue measure
    - measurable functions
- integration
    - Riemann
    - Lebesgue
    - Lebesgue-Stieltjes
- convergence theorems
- functions of bounded variation
- absolute continuity 
- differentiation
    - monotone functions
    - integrals
    - Lebesgue points

### General measure and integration theory

- measure spaces
- measurable functions
- Lusin’s Theorem
- Egoroff’s Theorem
- Fatou’s Lemma
- monotone and dominated convergence
- convergence in measure
- dense subspaces of $L^1$
    - simple functions
    - continuous functions with compact support
- integration convergence theorems
- signed measures
- the Radon-Nikodym Theorem
- product measures
- Fubini’s Theorem
- Tonelli’s Theorem.

### Functional analysis

- $L^p$-spaces and their conjugates
    - Hoelder and Minkowski inequalities
    - completeness of $L^p$
    - dense subspaces of $L^p$
- the Riesz-Fisher theorem
- the Riesz representation theorem
    - bounded linear functionals on $L^p$ and $C(X)$
    - just for $C(X)$
- the Hahn-Banach Theorem
- the Closed Graph and Open Mapping Theorems
- the Principle of Uniform Boundedness
- Alaoglu’s Theorem
- Hilbert spaces
- orthogonal systems
- Fourier series
    - $L^2$ convergence
- Bessel’s inequality
- Parseval’s formula
- convolutions
- Fourier transform
- distributions
- Sobolev spaces

## Fall semester notes

### Week 1

The course is under professor Judith Packer. I created a repo for assignments at <https://github.com/coltongrainger/ana1>. We'll cover Folland [@Fo99] up to chapter 3, with the goal of defining measures sufficient for general spaces while, along the way, treating the foundations of measure theory and Lebesgue integration.

We'll be evaluated on:

- three timed exams
- biweekly homework

We assume rudiments of set theory and the axiomatic derivation of the real numbers are known.

Immediately, we're looking to address

\newcommand{\RR}{\mathbf{R}}

- Lebesgue measures and their relation to integration on $\RR^n$
- "high powered calculus"
- integration beyond the Riemann integral

#### Riemannian interpretation

\newcommand{\sP}{\mathscr{P}}
\newcommand{\sU}{\mathscr{U}}
\newcommand{\sL}{\mathscr{L}}

RECALL! (Lower sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The lower sum $\sL_\sP(f)$ is defined ... $$\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$$

The upper sum $\sU_\sP$ is defined analogously with the supremum. We have $\sU_sP(f) \geq \sL_\sP(f)$ for all partitions of any real valued function defined on $[a,b]$. With these sums, we proceed to "Cauchy and Riemann's interpretation of the calculus of Newton and Leibniz".

<!---
RECALL! (Upper sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The upper sum $\sU_\sP(f)$ is defined ... $$\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$$
--->

DEF! (Lower Riemann integral) $\underline{\int}_a^b f(x)\,dx:=$ ... $\sup\{\sL_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.
