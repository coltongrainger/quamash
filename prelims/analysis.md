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

The upper sum $\sU_\sP$ is defined analogously with the supremum. We have $\sL_\sP(f)\leq  \sU_\sP(f)$ for all partitions of any real valued function defined on $[a,b]$. 

<!---
RECALL! (Upper sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The upper sum $\sU_\sP(f)$ is defined ... $\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$
--->

With these sums, we proceed to "Cauchy and Riemann's interpretation of the calculus of Newton and Leibniz".

DEF! (Lower Riemann integral) $\underline{\int}_a^b f(x)\,dx:=$ ... $\sup\{\sL_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

DEF! (Upper Riemann integral) $\overline{\int}_a^b f(x)\,dx:=$ ... $\inf\{\sU_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

Because $\sL_\sP(f)\leq \sU_\sP(f)$, it is always true that $\overline{\int}_a^b f(x)\,dx \leq \underline{\int}_a^b f(x)\,dx$. 

DEF! (The Riemann intergral) We say that $f$ is Riemann integrable over $[a,b]$ iff 
... $\overline{\int}_a^b f(x)\,dx = \underline{\int}_a^b f(x)\,dx$, that is, the lower and upper Riemann integrals (suitably defined) are equal.

What limitations should we expect of the Riemann integral?

1. It's easy to find witness functions not integrable, e.g., Dirichlet's function.[^Peter]

[^Peter]: Introduced by Dirichlet in 1829 *for the purpose* of testing the convergence of Fourier series. See *Sur la convergence des séries trigonométriques qui servent à représenter une fonction arbitraire entre des limites données*.

2. A Riemann integral function is necessarily *bounded*. We have to define improper integrals as the limit of a sequence integral values.

3. The Riemann integral is not easy to manipulate when tied up in another limiting process. (Why? We occasionally want to commute limits.)

EX! For the unbounded function $f \colon [0,1] \to \RR$ defined $f(0) = 0$ and $f(x) = x^{-1/2}$ for all $x \in (0,1]$, the improper Riemann integral of $f$ on it's domain is defined as the limit ... $\lim_{t\to 0^+}\int_t^1 x^{-1/2}\,dx$.

\newcommand{\NN}{\mathbf{N}}

For motivation, consider the sequence of functions $\{f_n \colon [a,b] \to \RR\}_{n\in \NN}$, and suppose each is Riemann integrable.

- When does the limit of Riemann integrals $\lim_{n \to \infty} \int_a^b f_n(x)\,dx$ exist?
- When does an outer limit commute with the Riemann integral's inner infima and suprema?
    - When does $\lim_{n \to \infty} \int_a^b f_n(x)\,dx =  \int_a^b\lim_{n \to \infty} f_n(x)\,dx$?
- How can we integrate Fourier series (or, generally, series representation of functions)?  
    - Does $\int_a^b \sum_{n=1}^\infty f_n\,dx =\sum_{n=1}^\infty \int_a^b f_n\,dx$?

>  When Fourier submitted his paper [*Mémoire sur la propagation de la chaleur dans les corps solides*] in 1807, the committee (which included Lagrange, Laplace, Malus and Legendre, among others) concluded: ...the manner in which the author arrives at these equations is not exempt of difficulties and [...] his analysis to integrate them still leaves something to be desired on the score of generality and even rigour. [[List of important publications in mathematics](https://en.wikipedia.org/wiki/List_of_important_publications_in_mathematics#Analysis). English Wikipedia. Retrieved September 9, 2018.]

We need (general) integrals that (i) allow reasonable interchange of sums and limits and that (ii) have values coinciding with Riemann integrals (whenever these Riemann integrals exist). Some options.

- the Lebesgue integral (1901)
- the (narrow) [Denjoy integral](https://www.encyclopediaofmath.org/index.php/Denjoy_integral) defined via transfinite induction (1912)
- the [Kinchin integral](https://en.wikipedia.org/wiki/Khinchin_integral) or "wide Denjoy integral" (1916)
- the [Perron integral](https://www.encyclopediaofmath.org/index.php/Perron_integral) defined via minor and major functions
- the [Henstock-Kurzweil integral](https://en.wikipedia.org/wiki/Henstock%E2%80%93Kurzweil_integral) or "[gauge integral](https://math.vanderbilt.edu/schectex/ccc/gauge/letter/)" (1957)
- 

THANKS! We owe the Lebesgue integral to a burst of productivity in continental Europe between ... Bernhard Riemann's 1853 *Über die Darstellbarkeit einer Function durch eine trigonometrische Reihe* and Henri Lebesgue's 1901 doctoral dissertation, *Intégrale, longueur, aire*.


