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

Immediately, we're looking to address

\newcommand{\RR}{\mathbf{R}}
\newcommand{\NN}{\mathbf{N}}

- Lebesgue measures and their relation to integration on $\RR^n$
- "high powered calculus"
- integration beyond the Riemann integral

#### Riemannian interpretation of the calculus

\newcommand{\sP}{\mathscr{P}}
\newcommand{\sU}{\mathscr{U}}
\newcommand{\sL}{\mathscr{L}}

RECALL: (Lower sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The lower sum $\sL_\sP(f)$ is defined ... $$\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$$

The upper sum $\sU_\sP$ is defined analogously with the supremum. We have $\sL_\sP(f)\leq  \sU_\sP(f)$ for all partitions of any real valued function defined on $[a,b]$. 

<!---
RECALL: (Upper sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The upper sum $\sU_\sP(f)$ is defined ... $\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$
--->

With these sums, we proceed to "Cauchy and Riemann's interpretation of the calculus of Newton and Leibniz".

DEF: (Lower Riemann integral) $\underline{\int}_a^b f(x)\,dx:=$ ... $\sup\{\sL_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

DEF: (Upper Riemann integral) $\overline{\int}_a^b f(x)\,dx:=$ ... $\inf\{\sU_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

Because $\sL_\sP(f)\leq \sU_\sP(f)$, it is always true that $\overline{\int}_a^b f(x)\,dx \leq \underline{\int}_a^b f(x)\,dx$. 

DEF: (The Riemann intergral) We say that $f$ is Riemann integrable over $[a,b]$ iff ... $\overline{\int}_a^b f(x)\,dx = \underline{\int}_a^b f(x)\,dx$, that is, the lower and upper Riemann integrals (suitably defined) are equal.

#### Historical motivation for Lebesgue integration

What limitations should we expect of the Riemann integral?

1. It's easy to find witness functions not integrable, e.g., Dirichlet's function.

    - Introduced by Dirichlet in *Sur la convergence des séries trigonométriques qui servent à représenter une fonction arbitraire entre des limites données* (1829) for the purpose of testing the convergence of Fourier series approximations to general functions.

2. A Riemann integral function is necessarily *bounded*. We have to define improper integrals as the limit of a sequence integral values.

3. The Riemann integral is not easy to manipulate when tied up in another limiting process. (Why? We occasionally want to commute limits.)

EX: For the unbounded function $f \colon [0,1] \to \RR$ defined $f(0) = 0$ and $f(x) = x^{-1/2}$ for all $x \in (0,1]$, the improper Riemann integral of $f$ on it's domain is defined as the limit ... $\lim_{t\to 0^+}\int_t^1 x^{-1/2}\,dx$.

For motivation, consider the sequence of functions $\{f_n \colon [a,b] \to \RR\}_{n\in \NN}$, and suppose each is Riemann integrable.

- When does the limit of Riemann integrals $\lim_{n \to \infty} \int_a^b f_n(x)\,dx$ exist?
- When does an outer limit commute with the Riemann integral's inner infima and suprema?
    - When does $\lim_{n \to \infty} \int_a^b f_n(x)\,dx =  \int_a^b\lim_{n \to \infty} f_n(x)\,dx$?
- How can we integrate Fourier series (or, generally, series representation of functions)?  
    - Does $\int_a^b \sum_{n=1}^\infty f_n\,dx =\sum_{n=1}^\infty \int_a^b f_n\,dx$?

>  When Fourier submitted his paper [*Mémoire sur la propagation de la chaleur dans les corps solides*] in 1807, the committee (which included Lagrange, Laplace, Malus and Legendre, among others) concluded: ...the manner in which the author arrives at these equations is not exempt of difficulties and [...] his analysis to integrate them still leaves something to be desired on the score of generality and even rigour. [[List of important publications in mathematics](https://en.wikipedia.org/wiki/List_of_important_publications_in_mathematics#Analysis). English Wikipedia. Retrieved September 9, 2018.]

We need (general) integrals that (i) allow reasonable interchange of sums and limits and that (ii) have values coinciding with Riemann integrals (whenever these Riemann integrals exist).

THANKS: We owe the Lebesgue integral to a burst of productivity in continental Europe between ... Bernhard Riemann's 1853 *Über die Darstellbarkeit einer Function durch eine trigonometrische Reihe* and Henri Lebesgue's 1901 doctoral dissertation, *Intégrale, longueur, aire*.

Some generalizations of the Lebesgue integral include

- the (narrow) [Denjoy integral](https://www.encyclopediaofmath.org/index.php/Denjoy_integral) defined via transfinite induction (1912)
- the [Kinchin integral](https://en.wikipedia.org/wiki/Khinchin_integral) or "wide Denjoy integral" (1916)
- the [Perron integral](https://www.encyclopediaofmath.org/index.php/Perron_integral) defined via minor and major functions
- the [Henstock-Kurzweil integral](https://en.wikipedia.org/wiki/Henstock%E2%80%93Kurzweil_integral) or "[gauge integral](https://math.vanderbilt.edu/schectex/ccc/gauge/letter/)" (1957)

We now aim to rigorously define the Lebesgue measure, the Lebesgue integral, and it's relation to differentiation (we are happy with the differentiation's naive definition). By the end of the semester, we should be able to make an analogous statement of the fundamental theory of calculus for Lebesgue integration.

#### Assumed background

We assume the rudiments of set theory and an axiomatic derivation of the real numbers are known.

\newcommand{\QQ}{\mathbf{Q}}

DEF: (Naive) The real numbers are ... elements of the complete ordered field $\RR$ containing $\QQ$; they are, to be hand-wavy, Dedekind cuts.

But what are Dedekind cuts? Well, real numbers, defined as so [@Sp94 chapter 29].

> A real number is a set $\alpha$ of rational numbers, with the following properties.
> 
> 1. if $x$ is in $\alpha$ and $y$ is a rational number with $y < x$, then $y$ is in $\alpha$
> 2. $\alpha \neq \emptyset$
> 3. $\alpha \neq \QQ$
> 4. there is no greatest element in $\alpha$, i.e., if $x$ is in $\alpha$, then there's some $y$ in $\alpha$ with $x < y$.


<!---
DEF: (Dedekind cuts) A real number is a set $\alpha$ of rational numbers, with the following properties [...] (2) $\alpha \neq \emptyset$; (3) $\alpha \neq \QQ$; (4) there is no greatest element in $\alpha$, i.e., if $x$ is in $\alpha$, then there's some $y$ in $\alpha$ with $x < y$. ... (1) if $x$ is in $\alpha$ and $y$ is a rational number with $y < x$, then $y$ is in $\alpha$;
DEF: (Dedekind cuts) A real number is a set $\alpha$ of rational numbers, with the following properties (1) if $x$ is in $\alpha$ and $y$ is a rational number with $y < x$, then $y$ is in $\alpha$; [...] (3) $\alpha \neq \QQ$; (4) there is no greatest element in $\alpha$, i.e., if $x$ is in $\alpha$, then there's some $y$ in $\alpha$ with $x < y$. ... (2) $\alpha \neq \emptyset$;
DEF: (Dedekind cuts) A real number is a set $\alpha$ of rational numbers, with the following properties (1) if $x$ is in $\alpha$ and $y$ is a rational number with $y < x$, then $y$ is in $\alpha$; (2) $\alpha \neq \emptyset$; [...]  (4) there is no greatest element in $\alpha$, i.e., if $x$ is in $\alpha$, then there's some $y$ in $\alpha$ with $x < y$. ... (3) $\alpha \neq \QQ$;
DEF: (Dedekind cuts) A real number is a set $\alpha$ of rational numbers, with the following properties (1) if $x$ is in $\alpha$ and $y$ is a rational number with $y < x$, then $y$ is in $\alpha$; (2) $\alpha \neq \emptyset$; (3) $\alpha \neq \QQ$; [...] ... (4) there is no greatest element in $\alpha$, i.e., if $x$ is in $\alpha$, then there's some $y$ in $\alpha$ with $x < y$.
--->

We ought also to define the order $<$ we've imposed on the field.

\newcommand{\FF}{\mathbf{F}}

DEF: An ordered field is a field $\FF$ with operations $+$ and $\cdot$ together with a certain subset $P$ of $\FF$ (the positive elements) with the following properties ... First, for all $a \in \FF$ one and only one of the following hold (i) $a = 0$, (ii) $a$ is in $P$, (iii) $-a$ is in $P$. Second, if $a$ and $b$ are in $P$, then their sum $a + b$ is in $P$. Lastly, if $a$ and $b$ are in $P$, then their product $a \cdot b$ is in $P$.

We are now in a position to give the traditional definition of the real numbers.

DEF: (Axiom of completeness) The set of real numbers is ... the ordered field with the least upper bound property, i.e., if $A$ is a set of real numbers, $A \neq \emptyset$, and $A$ is bounded above, then $A$ has a least upper bound.

Other definitions of the reals might require

- [Constructing the real numbers via Cauchy sequences](https://math.stackexchange.com/questions/11923) 
- adjoining two elements? (yuck)

DEF: State the axiom of completeness for the extended reals $\overline{\RR} = \RR \cup \{-\infty, + \infty\}$. ... Every subset of the extended reals has a supremum (whence also an infimum). Note that $\sup \emptyset = \infty$ and $\inf \emptyset = -\infty$.

FACT: Suppose $\{x_n\}$ is a sequence of extended real numbers. Then $\limsup x_n$ and $\liminf x_n$ both ... always exist.

<---!
DEF: The limit superior (of a sequence of elements $x_n$ in a linearly ordered set) is denoted $\limsup x_n$ and defined ... $\limsup x_n := \inf_{k\geq 1}\left(\sup_{n\geq k} x_n \right)$.

DEF: The limit inferior (of a sequence of elements $x_n$ in a linearly ordered set) is denoted $\liminf x_n$ and defined ... $\liminf x_n := \sup_{k\geq 1}\left(\inf_{n\geq k} x_n \right)$.
--->

#### Products

Notes from [@Fo99, chapter 0].

Open question: how is one to firm up the circular definition (in terms of functions, which are themselves defined as subsets of Cartesian products) of Cartesian products of infinite families?

DEF: If $\{X_\alpha\}_{\alpha \in A}$ is an indexed family of sets, their Cartesian product $\prod_{\alpha \in A}$ is defined as ... the set of all maps $$f\colon A \to \bigcup_{\alpha \in A} X_\alpha$$ such that $f(\alpha) \in X_\alpha$ for every $\alpha \in A$. (Usually we write $x$ instead of $f$.)

DEF: Suppose $X = \prod_{\alpha \in A}$. We define the $\alpha$th coordinate projection (or coordinate map) $\pi_\alpha \colon X \to X_\alpha$ by ... $\pi_\alpha(f) = f(\alpha)$. (Usually we write $x_\alpha$ instead of $f(\alpha)$.)

DEF: If the sets $X_\alpha$ for all $\alpha \in A$ are all equal to some fixed set $Y$, then the Cartesian product $\prod_{\alpha \in A} X_\alpha$ is just ... the set of all mappings from $A$ into $Y$, denoted $Y^A$. If $A = \{1, \ldots, n\}$, we write $Y^A$ as $Y^n$ and identify it with n tuples of elements of $Y$.

#### Orderings

Recall that a partial ordering on a nonempty set $X$ is a relation that's reflexive, antisymmetric, and transitive.

DEF: A linear (or total) ordering on a set $X$ is ... a partial ordering on $X$ with the additional requirement that any two distinct elements are comparable.

EX: Let $E$ be a set and $\sP(E)$ its powerset. There's a natural partial order on $\sP(E)$ by the relation ... $\subset$ (set inclusion).

EX: $\RR$ and $\QQ$ are (linearly) ordered fields by the relation ... $\leq$ (less than or equal to).

DEF: Two partially ordered sets $X$ and $Y$ are order isomorphic if there's a bijection $f \colon X \to Y$ such that ... for all points $x_1$ and $x_2$ in $X$, we have $x_1 \leq x_2$ iff $f(x_1) = f(x_2)$.

DEF: If $X$ is partially ordered by $\leq$ a maximal (minimal) element of $X$ is an $x \in X$ such that ... the only $y \in X$ satisfying $x \geq y$ (resp $y\leq x$) is $x$ itself.

- A maximal (resp minimal) element may not exist.
- It also may not be unique, unless the ordering is *linear*.

DEF: With $X$ a poset and $\leq$ the relation on $E \subset X$, we define an upper (lower) bound for $E$ as an element $x \in X$ such that ... $y\leq x$ (resp $x \leq y$) for all $y \in E$.

- An upper (resp lower) bound may not exist.
- It may not be an element of $E$.
- It may not be a maximal (resp minimal) element of $E$, unless the ordering is *linear*.

DEF: If $X$ is linearly ordered by $\leq$ and every nonempty subset of $X$ has a (necessarily unique) minimal element, $X$ is said to be ... well ordered by $\leq$ and $\leq$ is called (in defiance of the laws of grammar) a well ordering on $X$.

#### Set theoretic rudiments

As much as I think these are funny, I do have to list them here.

Some motivation from [Jerry Bona](https://en.wikipedia.org/wiki/Jerry_L._Bona):

> The Axiom of Choice is obviously true, the Well–ordering theorem is obviously false; and who can tell about Zorn’s Lemma?

<!---
RECALL: From Jerry Bona: The Axiom of Choice is [...], the Well–ordering theorem is [...]; and who can tell about Zorn’s Lemma? ... The Axiom of Choice is obviously true, the Well–ordering theorem is obviously false; and who can tell about Zorn’s Lemma?
--->

PROP: The Hausdorff maximal principle states ... every partially ordered set has a maximally linearly ordered subset. (In other words, there exists a subset $B$ of a poset $A$ with the relation $\prec$ such that no subset of $A$ that properly contains $B$ is linearly ordered by $\prec$.)

The next example taken verbatim from [@Mu00, section 11]:

\newcommand{\sA}{\mathscr{A}}

If $\sA$ is any collection of sets, the relation $\subsetneq$ (is a proper subset of) is a strict partial order on $\sA$. 

EX: Suppose that $\sA$ is the collection of all circular regions (interiors of circles) in the plane, ordered by $\subsetneq$. Name two maximal totally ordered sub-collections of $\sA$. ... (1) All circular regions with centers at the origin; (2) all circular regions bounded by circles tangent from the right to the $y$-axis at the origin.

One more organic example ($C^k(D)$ notation from <http://mathworld.wolfram.com/C-kFunction.html>):

EX: Consider the continuous functions $C^0(\RR)$ with the relation $f \prec g$ iff $f(x) < g(x)$ for all points $x \in \RR$. Name a maximal totally ordered collection of functions of $C^0(\RR)$. ... Fix a function $h \in C^0(\RR)$ and let $\lambda \in \RR$ parameterize the constant functions $c_\lambda \in C^0(\RR)$. Then the collection $\{ h + c_\lambda : \lambda \in \RR\}$ is maximal and totally ordered.

PROP: Zorn's lemma states ... if $X$ is a poset and every linearly ordered subset of $X$ has an upper bound then $X$ has a maximal element.

- Usually applied for non-constructive proofs of existence theorems.
- See Keith Conrad's [Zorn's lemma and some applications](https://www.math.uconn.edu/~kconrad/blurbs/zorn1.pdf).

PROP: The Well Ordering Principle states ... every nonempty set $X$ can be well ordered.

PROP: The axiom of choice states ... if $\{X_\alpha\}$ is a nonempty family of nonempty sets, then the Cartesian product $\prod_{\alpha \in A} X_\alpha$ is nonempty.

- Will eventually be invoked in the proof of [Tychonoff's theorem](https://en.wikipedia.org/wiki/Tychonoff%27s_theorem).



