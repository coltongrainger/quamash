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

### Week 1: preliminaries

The course is under professor Judith Packer. I created a repo for assignments at <https://github.com/coltongrainger/pro19ana1>. We'll cover Folland [@Fo99] up to chapter 3, with the goal of defining measures sufficient for general spaces while, along the way, treating the foundations of measure theory and Lebesgue integration.

We'll be evaluated on:

- three timed exams
- biweekly homework

Immediately, we're looking to address

\newcommand{\RR}{\mathbf{R}}
\newcommand{\NN}{\mathbf{N}}

- Lebesgue measures and their relation to integration on $\RR^n$
- "high powered calculus"
- integration beyond the Riemann integral

#### Riemannian interpretation

\newcommand{\sP}{\mathscr{P}}
\newcommand{\sU}{\mathscr{U}}
\newcommand{\sL}{\mathscr{L}}

RECALL: (Lower sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The lower sum $\sL_\sP(f)$ is defined ... $$\sum_{i=1}^n \inf\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$$

The upper sum $\sU_\sP$ is defined analogously with the supremum. We have $\sL_\sP(f)\leq  \sU_\sP(f)$ for all partitions of any real valued function defined on $[a,b]$. 

<!---
RECALL: (Upper sum) Suppose $f$ is a bounded function on $f\colon [a,b] \to \RR$. Let $a < b$ and fix $\sP = \{a, x_1, \ldots, x_{n-1}, b\}$ a partition of the set $[a,b]$. The upper sum $\sU_\sP(f)$ is defined ... $\sum_{i=1}^n \sup\{f(x): x \in [x_{i-1}, x_i]\}\cdot(x_i - x_{i-1}).$
--->

With these sums, we proceed to "Cauchy and Riemann's interpretation of the calculus of Newton and Leibniz".

DEF: (Lower Riemann integral) $\underline{\int}_a^b f(x)\,dx:=$ ... $\sup\{\sL_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

DEF: (Upper Riemann integral) $\overline{\int}_a^b f(x)\,dx:=$ ... $\inf\{\sU_\sP(f) : \sP \text{ is a partition of $[a,b]$}\}$.

Because $\sL_\sP(f)\leq \sU_\sP(f)$, it is always true that $\overline{\int}_a^b f(x)\,dx \leq \underline{\int}_a^b f(x)\,dx$. 

DEF: (The Riemann intergral) We say that $f$ is Riemann integrable over $[a,b]$ iff ... $\overline{\int}_a^b f(x)\,dx = \underline{\int}_a^b f(x)\,dx$, that is, the lower and upper Riemann integrals (suitably defined) are equal.

#### Historical motivation (Lebesgue integration)

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

DEF: The limit superior (of a sequence of elements $x_n$ in a linearly ordered set) is denoted $\limsup x_n$ and defined ... $\limsup x_n := \inf_{k\geq 1}\left(\sup_{n\geq k} x_n \right)$.

DEF: The limit inferior (of a sequence of elements $x_n$ in a linearly ordered set) is denoted $\liminf x_n$ and defined ... $\liminf x_n := \sup_{k\geq 1}\left(\inf_{n\geq k} x_n \right)$.

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

### Week 2: more preliminaries, the Borel sigma algebra 

#### Metric Spaces

We'll primarily be concerned with the metric space $\RR^n$.

\providecommand{\abs}[1]{\lvert #1 \rvert}

IDEA: The endpoints of open and closed intervals in $\RR$ are ought to be measured by the distance function $\abs{x-y}$, and this turns out to be a metric on $\RR$.

Some intuitive properties of the distance function on $\RR$:

0. $\abs{x-y} \ge 0$ for all $x, y \in \RR$ (non-negativity)
1. $\abs{x-y} = 0$ iff $x = y$ (identical points have no distance)
2. $\abs{x-y} = \abs{y-x}$ (symmetry)
3. $\abs{x-z} \le \abs{x-y} + \abs{y-z}$ for all $x,y \in \RR$ (triangle inequality)

Note that metrics and vector norms are not generally compatible. There are "more" metrics on $\RR^n$ than those induced by vector space norms.^[ [“Difference between metric and norm made concrete: The case of Euclid”](https://math.stackexchange.com/questions/38634/difference-between-metric-and-norm-made-concrete-the-case-of-euclid/38638#38638). Mathematics Stack Exchange. Retrieved September 24, 2018.]

> The metric $d(u,v)$ induced by a vector space norm has additional properties that are not true of general metrics. These are:
> 
> **Translation Invariance:** $d(u+w,v+w)=d(u,v)$
> 
> **Scaling Property:** For any real number $t$, $d(tu,tv)=|t|d(u,v)$.
> 
> Conversely, if a metric has the above properties, then $d(u,0)$ is a norm.
> 
> More informally, the metric induced by a norm "plays nicely" with the vector space structure.  The usual metric on $\mathbb{R}^n$ has the two properties mentioned above.  But there are metrics on $\mathbb{R}^n$ that are *topologically equivalent* to the usual metric, but not translation invariant, and so are not induced by a norm.

\providecommand{\norm}[1]{\lVert #1 \rVert}

To list some intuitive "distances" we care about.

- distances between points and sets 
- distances between sets

DEF: $(X, \rho)$ be a metric space, $A \subset X$ and $b \in X$. The distance from the point $b$ to the set $A$ is ... the number $\rho(b,A) = \inf\{\rho(b,a) : a \in A\}$.

DEF: Let $A$ and $B$ be two bounded subsets in a metric space $(X, \rho)$. We define the Hausdorff distance between $A$ and $B$ as ... $$d_\rho(A,B) = \max\left\{\sup_{a \in A}\rho(a, B), \sup_{b \in B}\rho(b, A)\right\}.$$

- euclidean norms $d(x,y) = \norm{x - y} = \left(\sum_1^n (x_i - y_i)^2\right)^{1/2}$
- complex distances (e.g., by conjugation)
- the Minkowski norms $\ell_p$ of a point $x \in \RR^k$ for any $1 \leq p \leq \infty$, $$\norm{x}_p = \left(\sum_1^n \abs{x_i}^p\right)^{1/p}$$

DEF: (Hölder inequality) Let $x, y \in \RR^n$, and take real number $p,q >0$ such that $1/p + 1/q =1$. Then the sum $$\sum_1^n x_i y_i$$ is less than or equal to the product ... $$\left(\sum_1^n x_i^p\right)^{1/p} \left(\sum_1^n y_i^q\right)^{1/q}.$$

- the "length of a shortest path in the set"
- the supremum of the pointwise distance between continuous functions on a compact set
- metrics on product spaces
- metrizable topological spaces

We showed that open balls in a metric spaces generate a topology. We *did* need finiteness to show that the intersection of so many open balls is again an open ball. Whence we appealed to the notions of "largest" and "smallest" (under set containment) to get interiors, closures, denseness, and nowhere denseness.

DEF: For a metric space $(X, \rho)$, the interior of a set $E \subset X$ is ... $$E^\circ = \bigcup\{ U \subset X \text{ such that } U \subset E \text{ is open}\}.$$

DEF: For a metric space $(X, \rho)$, the closure of a set $E \subset X$ is ... $$\overline{E} = \bigcap\{ F \subset X \text{ such that } E \subset F \text{ where $F$ is closed}\}.$$

DEF: A set $E$ in a topological space is called dense in $X$ if ... $\overline{E} = X$. 

DEF: A set $E$ in a topological space is called nowhere dense in $X$ if ... $(\overline{E})^\circ = \emptyset$. 

DEF: A metric space $(X, \rho)$ is said to be separable if ... $X$ has a countable dense subset.

DEF: A sequence in a metric space $(X, \rho)$ is called Cauchy if ... $\rho(x_n,x_m) \to 0$ as $n,m \to \infty$.

DEF: A subset $E$ of a metric space $X$ is called complete if ... every Cauchy sequence in $E$ converges and its limit is in $E$. (E.g., $\RR^n$ is complete, $\QQ^n$ is not.)

DEF: A set $E$ in a metric space is said to be totally bounded if ... for all $\epsilon >0$, $E$ can be covered by finitely many balls of radius $\epsilon$.

THM: If $E$ is a subset of the metric space $(X,\rho)$, the following are equivalent: $E$ is complete and totally bounded. ... (Bolzano Weierstrauss property) Every sequence in $E$ has a subsequence that converges to a point of $E$; (Heine-Borel property) If $\{V_\alpha\}_{\alpha \in A}$ is a finite cover of $E$ by open sets, there is a finite set $F \subset A$ such that $\{V_\alpha\}_{\alpha \in F}$ covers $E$.

#### Naive counter examples

From [@Go08, number III.55]: suppose we have a sequence of intervals in $[0,1]$, say $[a_i, b_i]$ with $\sum_1^n (b_i - a_i) < 1$, it is possible that their union $\cup_1^n [a_i, b_i] = [0,1]$? Why not?

Same question, but consider $[a_i,b_i]$ for $i \in I$ an infinite index set? Perhaps?

- Consider $[0,1] \cap \QQ$. 
- Take intervals with lengths $1/4$, $1/8$, $1/16$, and so forth. 
- Then $\sum_1^i (b_i - a_i) = 1/2$.
- Yet since $\QQ$ is countable, we can just enumerate the rationals in $[0,1]$ as $q_1, q_2, \ldots$ and put an interval of the aforementioned lengths around each, covering the set, whence there's some infinite set of intervals such that $$\cap_1^\infty [a_i, b_i] \supset [0,1] \cap \QQ.$$

DEF: As a naive attempt, we could take the length of a set $A \subset \RR$ to be ... the infimum of the length of a finite union of intervals that cover $A$, i.e., $$\inf\left\{ \sum_1^n (b_i - a_i) \text{ for all finite unions of intervals $[a_i,b_i]$ that cover $A$}\right\}.$$

But then $[0,1] \cap \QQ$ would have length $1$, also $[0,1] \cap \RR \setminus \QQ$: Such a "measure" of length is poorly behaved. 

Now, we want a notion of length that 

1. applies to all sets we know and love, and 
2. is *additive* (with the appropriate definition)

Here's the key idea. Allow *countable* covers of $A$, then we have

DEF: To be more sophisticated, let the length of a set $A \subset \RR$ be ... the infimum of the length of a countable union of intervals that cover $A$, i.e., $$\inf\left\{ \sum_1^\infty (b_i - a_i) \text{ for all countable unions of intervals $[a_i,b_i]$ that cover $A$}\right\}.$$

Now by this definition, $\QQ \cap [0,1]$ has zero length, as does any countable set, as does even the uncountable Cantor set. Why?

Take as a warning, even with the key idea, some sets $A$ and $B$, though disjoint, have the property that the measure of $A \cup B$ is not the sum of the measures of $A$ and $B$. 

DEF: One says that a subset $A$ of $[0,1]$ is measurable if ... the measures of $A$ and of its complement $A^c$ add up to $1$.

#### The Borel sigma algebra

Q: What is the Borel $\sigma$-algebra on $\RR$? ... It's the smallest $\sigma$-algebra $\mathcal{B}_\RR$ that contains all $\RR$ standard open intervals.

\newcommand{\sT}{\mathscr{T}}

Note, since all open sets in $\RR$ *can be written* as the union of countably many open intervals, we have $\mathcal{B}_\RR \supset \sT_{std}$ the standard topology on $\RR$.

- Constructing a Borel $\sigma$-algebra requires some topology on the underlying set.
    - Note that, in general, a $\sigma$-algebra and a topology on a set are not comparable.

- How do we construct Borel sets? 
    - In descriptive set theory, Borel sets are *easily describable* (lol). 
    - They're countable unions and intersections of open and closed intervals.
    - They are generated by a smaller "semi-algebra" (or "elementary family") than the Lebesgue measurable sets. Why?
    - An arbitrary set of measure zero is not necessarily a Borel set. Why?

Here's more motivation for Lebesgue integration.

EX: Working in $[0,1]^2$ we define the measure of a set to be the least total area of a sequence of rectangles that covers the set. Whence for a function $f \colon [0,1] \to [0,1]$ we (naively) take the Lebesgue integral to be ... the Lebesgue measure of the set $\{(x,y) \colon y \in f(x)\}$.

EX: Considering a sequence of Lebesgue integrable functions $f_n \colon [0,1] \to [0,1]$, where $f_n \to f$ pointwise, we expect ... $f$ to be Lebesgue integrable with the series of Lebesgue integrals of the $f_n$ converging to the Lebesgue integral of $f$.

\newcommand{\sA}{\mathscr{A}}

DEF: An algebra of sets on $X$ is ... a nonempty collection $\sA \subset 2^X$ that's closed under finite unions and complements.

\newcommand{\sM}{\mathscr{M}}

DEF: (Folland) A $\sigma$-algebra of sets on $X$ is ... an algebra (usually denoted $\sM$) on $X$ that's closed under countable unions and complements.

\newcommand{\sE}{\mathscr{E}}

IDEA: If $\sE$ is any collection of subsets of $X$, then there's a unique $\sigma$-algebra $\sM(\sE)$ containing $\sE$, namely ... the intersection of all $\sigma$-algebras containing $\sE$.

DEF: Let $X = \prod_{\alpha \in A}$ be an indexed collection of non-empty sets, $X = \prod_{\alpha \in A} X_\alpha$ their product, and $\pi_\alpha \colon X \to X_\alpha$ the coordinate maps. If $\sM_\alpha$ is a $\sigma$-algebra on $X_\alpha$ for each $\alpha$, the product $\sigma$-algebra on $X$ is generated by ... $$\left\{\pi_\alpha^{-1}(E_\alpha) \colon E_\alpha \in \sM, \alpha \in A\right\}$$ and is denoted by $\otimes_{\alpha \in A} \sM_\alpha$ (or in the finite case, by $\otimes_1^n \sM_j$).

- How can we form a $\sigma$-algebra on $X\times Y$? 
- Naively, we might guess that $\sM = \{ A \times B : A \in \sM_S, B \in \sM_Y\}$. 
- But, for example, if $A = B = \RR$ and both are endowed with the Borel $\sigma$-algebra $\mathcal{B}_\RR$, then the set $(-\infty, a) \times (-\infty, b)$ is in $\sM$ but not its complement.
- But couldn't the naive attempt generate a $\sigma$-algebra?
    - It *does* when the Cartesian product is countable, but fails when the product is uncountable.

PROP: If $A$ is a countable index set, then $\otimes_{\alpha\in A} \sM_\alpha$ is indeed the $\sigma$-algebra generated by $$\left\{\prod_{\alpha \in A} E_\alpha : E_\alpha \in \sM_\alpha\right\}.$$

\newcommand{\sB}{\mathscr{B}}

PROP: Let $X_1, \ldots, X_n$ be metric spaces and let $\prod_1^n X_j$ equipped with the product metric (coordinate max), then the product $\sigma$-algebra of each Borel $\sigma$-algebra on the $X_j$ is ... a subset  $\otimes_{j=1}^n \sB_{X_j} \subset \sB_X$ with equality iff the $X_j$ are each separable.

### Week 3: measure spaces

#### Elementary families

DEF: An elementary family (or semi-algebra) on a set $X$ is a nonempty collection of subsets of $X$ such that ... (SA1) $\emptyset \in \sE$; (SA2) if $E, F \in \sE$, then $E\cap F \in \sE$; (SA3) if $E \in \sE$, then $E^c = X \setminus E$ can be written as a finite disjoint union of elements of $\sE$.

- Find an elementary family.
- Generate an algebra from that elementary family.
- Generate the smallest sigma algebra containing that algebra.

Riemann–Stieltjes measures arise when $f \colon \RR \to \RR$ is monotone, increasing, bounded, (and right continuous?) and we take as a elementary family $$\sE = \{f^{-1}((a,b]), f^{-1}(\emptyset), f^{-1}(\RR) : -\infty\le a < b \le \infty\}.$$

PROP: If $\sE$ is an elementary family of subsets of $X$, then the collections $\sA$ of finite disjoint unions of members of $\sE$ is ... an algebra of subsets of $X$.

- check $\emptyset \in \sA$
- check if $A, B \in \sA$, then $A \cup B \in \sA$ (try $A \cup B = [A \cap B^c] \sqcup B$)
- check if $A \in \sA$, then $A^c \in \sA$
    - requires induction
    - complements of elements in an elementary family are disjoint?
    - do something awful, distribute the intersection over the union
    - then $\sE$ is closed under intersection 
    - ... and Bob's your uncle.

Coming up: outer measures on algebras!

#### Definitions

DEF: Let $X$ be a set and $\sM$ a $\sigma$-algebra on $X$. A measure on $\sM$ is a function $\mu \colon \sM \to [0,\infty]$ such that ... (M1) the empty set is a null set, i.e., $\mu(\emptyset) = 0$; (M2) $\mu$ is countably additive, i.e., $\{E_j\}_1^\infty$ is a sequence of disjoint sets in $\sM$, then $$\mu\left(\bigsqcup_1^\infty E_j \right) = \sum_1^\infty \mu(E_j)$$ where it's possible that both sides are infinite.

\newcommand{\ZZ}{\mathbf{Z}}

For example, consider the counting measure on the measurable space $(\ZZ, 2^\ZZ)$

- fix $f \colon \ZZ \to [0,\infty]$
- define $\mu_f(E) = \sum_{n \in E} f(n)$ as a measure (verify)
- if $f(n) =1$ for all $n \in \ZZ$ then $\mu_1(E) = \mathrm{card}(E)$
- if $E$ is uncountable, we have no fancy notation 
- just map $\mu_1 \colon E \mapsto +\infty$

Now we usually leave $(\RR, \sB_\RR)$ on the corner of the board to indicate where (in which space and $\sigma$-algebra) we're working.

Ian asked a question about signed measures (or complex measures?). Packer immediately jumped to $C^*$ algebras(?) and mentioned that we have complex measures, usually *finite*, but that we can also consider (the projections of?) bounded operators that are self-adjoint and idempotent.

DEF: A measure space is ... a triple consisting of a set, a $\sigma$-algebra on that set, and a measure defined on that $\sigma$-algebra, $(X, \sM, \mu)$.

DEF: A probability space is ... a "normalized" measure space $(X, \sM, \mu)$ where $\mu(X) = 1$.

DEF: A finite measure space is ... a measure space $(X, \sM, \mu)$ where $\mu(X) < \infty$ [and thus for all $E \in \sM$ we have $\mu(E) < \infty$].

DEF: Now if some measure space can be written as the union $X = \cup_1^\infty X_n$ with each $X_n \in \sM$ (for all $n \in \NN$) and $\mu(X_n) < \infty$ we say that $(X, \sM, \mu)$ is ... $\sigma$-finite ($\sigma$ for "Somme").

EX: The counting measure on the integers as a measure space $(\ZZ, 2^\ZZ, \mu_1)$ is $\sigma$-finite because ... $\mu(\ZZ) = \infty$ yet $$\ZZ = \bigcup_{-\infty}^\infty \{n\} \text{ and } \mu(\{n\}) = 1 < \infty.$$

DEF: We say $(X, \sM, \mu)$ is semifinite if whenever $E \in \sM$ such that $\mu(E) = \infty$ there's a ... measurable set $F \in \sM$ where $F \subset E$ and $\mu(F) < \infty$.

We can find sets of finite measure in a semifinite measure space *as large as we want*.

EX: $(\RR, 2^\RR, \mu_1)$ is the measure space of real numbers with the counting measure. It's semifinite because ... if $\mu(A) = \infty$ then $A \neq \emptyset$ and so we can find $r \in A$ with $\mu_1(\{r\}) = 1 < \infty$.

In general any $\sigma$-finite measure space is semifinite. Now, as we want Fubini's theorem, we'll likely work in $\sigma$-finite spaces.

#### Properties

THM: Let $(X, \sM, \mu)$ be a measure space. Then $\mu$ has four basic properties ... monotonicity, countable subadditivity, continuity from below, and continuity from above (with finiteness restriction).

DEF: What's monotonicity of $\mu$ in a measure space? ... If $E, F \in \sM$ then $E \subset F$ and $\mu(E) \le \mu(F)$. (key idea: order preserving)

DEF: What's countable subadditivity of $\mu$ in a measure space? ... For any countable sequence $E_1, E_2, E_3, \ldots$ of (not necessarily disjoint) measurable sets, $$\mu\left(\bigcup_1^\infty E_j \right) \le \sum_1^\infty \mu(E_j).$$

DEF: What's continuity from below of $\mu$ in a measure space? ... If $E_1, E_2, E_3, \ldots$ are measurable sets and $E_j$ is a subset of $E_{j+1}$ for all $j \in \NN$, then the union of the sets $E_j$ is measurable, and $$\mu\left(\bigcup_1^\infty E_j \right) = \lim_{n \to \infty}\mu(E_n).$$ (key idea: nested-ness)

DEF: What's continuity from above of $\mu$ in a measure space? ... If $E_1, E_2, E_3, \ldots$ are measurable sets and $E_j \supset E_{j+1}$ for all $j \in \NN$, then the intersection of the sets $E_j$ is measurable; futhermore, if at least one of the $E_n$ has finite measure, then $$\mu\left(\bigcap_1^\infty E_j \right) = \lim_{n \to \infty}\mu(E_n).$$ (key idea: one of the sets down the line needs be finite)

For example, in the measure space $(\ZZ, 2^\ZZ, \mu)$, if we take sets $E_n = \{n , n + 1, \ldots\}$ for all $n \in \NN$, then 
$$0 = \mu(\emptyset) = \mu\left(\bigcap_1^\infty E_n \right) \neq \lim_{n \to \infty}\mu(E_n) = \infty.$$

#### Null sets and complete measures

DEF: If $(X, \sM, \mu)$ is a measure space, a set $E \in \sM$ such that $\mu(E) = 0$ is called a ... null set.

DEF: If a statement about points $x \in X$ in a measure space is true expect for $x$ in some null set, we say that it is true ... almost everywhere (or $\mu$-almost everywhere).

DEF: A measure whose domain contains all subsets of null sets is called ... complete.

\renewcommand{\sN}{\mathscr{N}}

THM: Suppose $(X, \sM, \mu)$ is a measure space. Let $\sN = \{ N \in \sM : \mu(N) = 0\}$ and $\overline{\sM} = \{ E \cup F : E \in \sM \text{ and } F \subset N \text{ for some } N \in \sN\}$. Then $\overline{\sM}$ is ... a $\sigma$-algebra, and there is a unique extension $\overline{\mu}$ of $\mu$ to a complete measure on $\overline{\sM}$.

*Proof sketch*. 

- $\overline{\sM}$ is a $\sigma$-algebra.

    - $\emptyset \in \overline{\sM}$ since $\emptyset \cup \emptyset \in \overline{\sM}$.

    - $\sM$ and $\sN$ are closed under countable unions, therefore $\overline{\sM}$ is too.

        - Just write $\cup_1^\infty(E_n \cap F_n) = (\cup E_n) \cup (\cup F_n)$.

    - $\overline{\sM}$ is closed under complements.

        - Suppose $E \cup F \in \sM$, where $E \in \sM$ and $F \in \sN$.
        - Note $F^c \supset N^c$.
        - Now $(E \cup F)^c = E^c \cap F^c \supset E^c \cap N^c$.
        - Show that $(E^c \cap F^c) \setminus (E^c \cap N^c) = E^c \cap F^c \cap N \subset N$.
        - Note $E^c \cap N^c \in \sM$ and $E^c \cap F^c \cap N \in \sN$.
        - Therefore $E^c \cap F^c = (E^c \cap N^c) \cap (E^c \cap F^c \cap N)$ is in $\overline{\sM}$

- When $E \cup F \in \overline{\sM}$ define $\overline{\mu}(E \cup F) = \mu(E)$.

    - $\overline{\mu}$ is well defined.

        - Take two representations of a set $C \in \overline{\sM}$.
        - Apply $\overline{\mu}$.
        - Argue by monotonicity.

    - $\overline{\mu}$ extends $\mu$.

        - If $E \in \sM \subset \overline{\sM}$, then $\overline{\mu}(E) = \overline{\mu}(E \cap \emptyset) = \mu(E)$.

- $\overline{\mu}$ is the unique, complete, measure satisfying $\overline{\mu}\vert_\sM = \mu$.

    - It's painfully straightforward to check.

DEF: We say that triple $(X, \overline{\sM}, \overline{\mu})$ is the completion, with respect to ... $\mu$, of the measure space ($X$, $\sM$, $\mu$).

#### Outer measures

The outer measure $\mu^*$ (defined out of $2^X$) measures a set "from the outside". Here's the gist of an outer measure's "relaxed definition":

- $\mu^*$ assigns no mass to null sets
- $\mu^*$ is monotone
- $\mu^*$ is countably subadditive

DEF: (Outer measure) An outer measure on a non-empty set $X$ is a function $\mu^* \colon \sP(X) \to [0,\infty]$ that satisfies ... (OM1) $\mu^*(\emptyset) = 0$; (OM2) $\mu^*(A) \le \mu^*(B)$ if $A \subset B$; (OM3) $\mu^*(\cup_1^\infty A_j) \le \sum_1^\infty \mu^*(A_j)$.

DEF: If $\mu^*$ is an outer measure on a set $X$, then a set $A \subset X$ is called $\mu^*$-measurable if ... $\mu^*(E) = \mu^*(E \cap A) + \mu^*(E \cap A^c)$ for all $E \subset X$ (given subadditivity, it suffices to show that $\mu^*(E) \ge \mu^*(E \cap A) + \mu^*(E \cap A^c)$ whenever $\mu^*(E) < \infty$).

To construct an outer measure, we can take $\mu^*(A)$ as the infimum of the sum of $\rho$ weights from any countable coverings of $A$.

PROP: (Carathéodory's construction) Let $\sE \subset \sP(X)$ be an elementary family, and $\rho\colon \sE \to [0,\infty]$ be a "mass assigning" function, such that $\emptyset \in \sE$, $X \in \sE$, and $\rho(\emptyset) = 0$. We can construct an outer measure $\mu^* \colon \sP(X) \to [0,\infty]$ by mapping $A \subset X$ to ... $$\mu^*(A) = \inf \left\{ \sum_1^\infty \rho(E_j) : E_j \in \sE \text{ and } A \subset \cup_1^\infty E_j\right\}.$$

*Proof sketch*.

- To show countable subadditivity, consider $\{A_j\}_1^\infty \subset \sP(X)$.

- If $\sum_1^\infty \mu^*(A_j) = \infty$ we are done, since the $\mu^*(\cup A_j) \le \infty$.

- Now for each $j$ find $\{E_j^k\}_{k=1}^\infty$ such that 
    - $\bigcup_{k=1}^\infty E_j^k \supset A_j$ (a covering)
    - $\sum_{k=1}^\infty \rho(E_j^k) - 2^{-j}\epsilon \le \mu^*(A_j)$ (noting $\mu^*$ is defined an inifimum of sums of the "masses" of coverings of this sort).

- Now I have a countable cover of the union $A = \cup_1^\infty A_j$, it's $\cup_{k=1}^\infty \cup_{j=1}^\infty E_j^k$.
    - Note again that $\mu^*(A)$ is a *lower bound* of the sums of masses of such countable covers.
    - That is, $\mu^*(\cup_{j=1}^\infty A_j) \le \sum_{j=1}^\infty \sum_{k=1}^\infty \rho(E_j^k)$.
    - But we have an inequality for the sum over $k$ (why?), that is $\sum_{j=1}^\infty \sum_{k=1}^\infty \rho(E_j^k) \leq \sum_j \mu^*(A_j) + \epsilon$
    - (Note the convergence of the geometric series to $\epsilon$.)

- String together the last two inequalities: $$\mu^*(\cup_{j=1}^\infty A_j) \le \sum_{j=1}^\infty \mu^*(A_j) + \epsilon$$
- Let $\epsilon >0$ become arbitrarily small.
- We've shown that $\mu^*$ is countably subadditive.

### Week 4: manipulating outer measures

#### Progress so far

To motivate development of measure theory so far, and justify the pains with which we've attended to the details of $\sigma$-algebras.

- The measure space $(\RR,\sB_\RR)$ is not complete with respect to the Lebesgue measure

    - somehow the cantor set has measure zero
    - yet its subsets get larger and larger

- We want to prove convergence theorems

    - we'll *need* measure theoretic arguments anyways
    - we might as well build up measurable functions in an abstract setting.
    - hence the measure spaces $(X, \sM, \mu)$

- We need measurable functions

    - we'll define measurable functions as "almost continuous"
    - for $f \colon X \to \RR$, it ought to be that $f$ is measurable if $f^{-1}((\alpha, \infty)) \in \sM$
    - for any "Borel measurable function" $f \colon \RR \to [0, \infty)$ we want $\int f = \sup \int_{0 \le \phi \le L} \phi$
    - $\phi$ will be a "simple function" or an "almost step" function.


#### Carathéodory's theorem

THM: (Carathéodory's theorem) If $\mu^*$ is an outer measure on $X$, the collection $\sM$ of all $\mu^*$-measurable sets is ... a $\sigma$-algebra, and the restriction of $\mu^*$ to $\sM$ is a complete measure.

*Proof sketch*. 

- $\sM$ is an algebra of sets on $X$.

    - $\emptyset$ is outer measurable (and *all null sets are outer measurable*).
    - If $A$ is outer measurable, then $A^c$ is too.
        - The outer measurable criterion is symmetric in complements.
    - If $A$ and $B$ are outer measurable, then $A \cup B$ is too.
        - For any $E \subset X$, decompose $E \cap (A \cup B)$ into $4$ disjoint unions in terms of $A$, $A^c$, $B$, and $B^c$.
        - Now disjoint $A \cap B$, $A \cap B^c$, and $A^c \cap B$ form $A \cup B$.
        - Argue by subadditivity that $\mu^*(E) \ge \mu^*(E \cap (A \cup B)) + \mu^*(E \cap (A \cup B)^c)$.

- $\sM$ is a $\sigma$-algebra too.

    - Get this lemma by induction: "If $\{F_1,\ldots,F_n\} \subset \sM$ and $F_j \cap F_i = \emptyset$, then for all $E \subset X$, $\mu^*\left(E \cap \bigcup_1^n F_j\right) = \sum_1^n \mu^*(E \cap F_j)$."
    - Decompose any countable collection $\{A_j\}_1^\infty \subset \sM$ into disjoint $\{F_j\}$.
        - $F_1 = A_1$, $F_n = A_n \setminus \cup_1^{n-1} A_j$.
        - The finite (resp. infinite) union of the $F_j$ is equal to the finite (resp. infinite) union of $A_j$.
    - Argue by monotonicity that $\mu^*(E) \ge \sum_1^n \mu^*(E \cap F_j) + \mu^*(E \cap (\cup_1^\infty F_j)^c)$.
    - Let $n \to \infty$ and argue by subadditivity that $$\mu^*(E) \ge \sum_1^\infty \mu^*(E \cap F_j) + \mu^*(E \cap (\cup_1^\infty F_j)^c) \ge \mu^*(E \cap (\cup_1^\infty F_j)) + \mu^*(E \cap (\cup_1^\infty F_j)^c) \ge \mu^*(E).$$
    - So $\cup_1^\infty F_j = \cup_1^\infty A_j$ is outer measurable.

- Obtain that $\mu^*$ is countably additive by choosing $E = \cup_1^\infty F_j$ in the previous inequality.

With Carathéodory's result, we may construct a complete measure space (or "pass to the completion") from an elementary family and some proto-measure.

- take an elementary family $\sE$ and a mass assigning set $\rho$
- form the outer measure of as an infimum of the sums of masses of countable coverings
    - we *do* have $\mu^*$ measurable sets---why?
- pass to $\sM \subset 2^X$ where $\sM$ is the collection of all $\mu^*$ measurable sets
- $\mu^*$ is a complete measure on $\sM$.

DEF: (Premeasure) Let $X$ be a nonempty set and let $\sA$ be an algebra of subsets of $X$. We say the function $\mu_0 \colon \sA \to [0,\infty]$ is a premeasure on $\sA$ if ... (PM1) $\mu_0(\emptyset) = 0$; (PM2) whenever (maybe $\sA$ is not infinite) $\{A_j\}_1^\infty \subset \sA$ are pairwise disjoint and $\sqcup_1^\infty A_j \in \sA$, then $$\mu_0(\sqcup_1^\infty A_j) = \sum_1^\infty \mu_0(A_j).$$

For example, let $X = \RR$, and consider some elementary family $$\sE = \{ \emptyset, \RR, (a,b] \text{ for } -\infty \le a < b \le \infty\} \cup \{(b,\infty) \text{ for all } b \in \RR\}.$$

We generate an algebra $\sA$ consisting of finite, disjoint, unions of elements from $\sE$. We define---*this is what we wanted naively*---a premeasure on $\sA$:

- $\mu_0(\emptyset) = 0$,
- $\mu_0((-\infty,\infty)) = \infty$,
- $\mu_0((a,b]) = b-a$,
- $\mu_0((b,\infty]) = \infty$, and lastly, 
- extend $\mu_0$ to $\sqcup_1^n (a_j, b_j]$ by $$\mu_0 \left(\sqcup_1^n (a_j,b_j]\right) = \sum_1^n (b_j - a_j).$$

PROP: If $\mu_0$ is a premeasure on $\sA$ and $\mu^*$ is the corresponding outer measure defined, for each $E \in X$, by $$\mu^*(E) = \inf \left\{ \sum_1^\infty \mu_0(A_j) : A_j \in \sE \text{ and } E \subset \cup_1^\infty A_j\right\}$$ then $\mu^* | \sA$ is ... $\mu_0$ and every set in $\sA$ is $\mu^*$-measurable.


<!---
PROP: If $\mu_0$ is a premeasure on $\sA$ and $\mu^*$ is the corresponding outer measure defined, for each $E \in X$, by [...] then $\mu^* | \sA = \mu_0$ and every set in $\sA$ is $\mu^*$-measurable. ... $$\mu^*(E) = \inf \left\{ \sum_1^\infty \mu_0(A_j) : A_j \in \sE \text{ and } E \subset \cup_1^\infty A_j\right\}$$ 
--->

*Proof sketch*. 

- To show that $\mu_0(E) \le \mu^*(E)$ for $E \in \sA$.
    - Observe $\mu_0$ is monotone on $\sA$.
    - Suppose $\{ A_j \}_1^\infty \subset \sA$ is a countable covering of $E$.
    - Define $B_1 = E \cap A_1$ and $B_n = E \cap \left(A_n \setminus \cup_1^{n-1} A_j\right)$.
        - All the $B_n$ are in $\sA$.
        - The union of the $B_n$ is just $E \cap \left(\cup_1^\infty A_j\right) = E$.
        - Note each $B_j \in A_j$.
    - Then $\mu_0(E) \le \sum_1^\infty \mu_0(B_j) \le \sum_1^\infty \mu_0(A_j)$.
    - By definition of $\mu^*$ as an infimum of such sums (the RHS above), $\mu_0(E) \le \mu^*(E)$.

- Now for $\mu^*(E) \le \mu^0(E)$.
    - Take the countable covering $\{E\} \subset \sA$ of $E$.
    - By definition of $\mu^*$ as an infimum, $\mu^*(E) \le \sum_1^1 \mu_0(E) = \mu_0(E)$.

- "So on intervals, e.g., the Lebesgue measure will coincide with the length".

- For $\mu^*$-measurability, we need $\mu^*(E) = \mu^*(E \cap A) + \mu^*(E \cap A^c)$ for any $A \subset X$.
    - Use the definition of $\mu^*$ as an infimum; let $\epsilon > 0$. 
    - There must exist some countable covering $\{B_j\}_1^\infty$ of $E$ such that $\mu^*(E) + \epsilon \ge \sum_1^\infty \mu_0(B_j)$.
    - We observe that $\mu_0$ is additive on disjoint sets in $\sA$.
    - Now note both $E \cap A \subset \left( \cup_1^\infty (B_j \cap A)\right)$ and $E \cap A^c \subset \left( \cup_1^\infty (B_j \cap A^c)\right)$.
    - Use additivity of $\mu_0$, and the definition of $\mu^*$.
    - $\sum_1^\infty \mu_0(B_j) = \sum_1^\infty \mu_0(B_j \cap A) + \sum_1^\infty \mu_0(B_j \cap A) \ge \mu^*(E \cap A) + \mu^*(E \cap A^c)$.
    - Since $\epsilon$ is arbitrary, we conclude $\mu^*(E) \ge \mu^*(E \cap A) + \mu^*(E \cap A^c)$.

Importantly, $\sM(\sA)$ is the smallest $\sigma$-algebra containing $\sA$, and because $\sM^*$ is a $\sigma$-algebra that contains $\sA$, we have the following inclusions: $$\sA \subset \sM(\sA) \subset \sM^*.$$

THM! Let $\sA \subset \sP(X)$ be an algebra, $\mu$ a premeasure on $\sA$, and $\sM$ the $\sigma$-algebra generated by $\sA$. There exists a measure $\bar{\mu}$ on $\sM$ whose restriction to $\sA$ is $\mu$. If $\nu$ is another such measure on $\sM$, then $\nu(E) \le \bar{\mu}(E)$ for all $E \in \sM$, with equality when $\bar{\mu}(E) < \infty$. If $\mu$ is $\sigma$-finite, then $\bar{\mu}$ is the unique extension of $\mu$ to a measure on $\sM$.

*Proof sketch*. TODO (notes from 2018-09-21).

We say "restrict to the finite part".

#### Analogy with topological spaces

From [@Ru87], an analogy to unify the material yet covered.

topological spaces | measurable spaces
--- | ---
topology | $\sigma$-algebra
open set | measurable set
continuous function | measurable function

We borrow some slick definitions.

DEF: A collection $\sM$ of subsets of a set $X$ is said to be a $\sigma$-algebra in $X$ if $\sM$ has the following properties ... (SA1) $X \in \sM$; (SA2) If $A \in \sM$ then $A^c \in \sM$ where $A^c$ is the complement of $A$ relative to $X$; (SA3) if $A = \cup_{n=1}^\infty A_n$ and $A_n \in \sM$ for $n =1, 2, 3, \ldots$, then $A \in \sM$.

DEF: If $\sM$ is a $\sigma$-algebra in $X$ then $X$ is called a measurable space, and the members of $\sM$ are called ... the measurable sets in $X$.

DEF: If $X$ is a measurable space, $Y$ a topological space, and $f \colon X \to Y$ a function, then $f$ is said to be measurable provided that ... $f^{-1}(V)$ is a measurable set in $X$ for every open set $V$ in $Y$.

### Week 5: Borel measures on the real line

PROP: Let $F \colon \RR \to \RR$ be increasing and right continuous. If the $(a_j, b_j]$ are (finitely many) disjoint h-intervals, let $\mu\left(\bigcup_1^n (a_j, b_j] \right)$ be given by ... $$\sum_1^n \left[ F(b_j) - F(a_j)\right]$$ with also $\mu(\emptyset) = 0$. Then $\mu$ is a premeasure on the algebra $\sA$ (of finite disjoint unions of $h$-intervals on the real line).

*Proof sketch*. TODO

THM: If $F \colon \RR \to \RR$ is any increasing, right continuous function, there is a unique measure $\mu_F$ on $\sB_\RR$ such that ... $\mu_F((a,b]) = F(b) - F(a)$ for all $a,b \in \RR$. If $G$ is another such function, we have $\mu_F = \mu_G$ iff $F - G$ is constant. 

*Proof sketch*. TODO

THM: Conversely, if $\mu$ is a measure on $\sB_\RR$ which is finite on all bounded Borel sets and we define [...], then $F$ is increasing and right continuous, and $\mu = \mu_F$. ... $F(x) = \mu((0,x])$ when $x > 0$, $F(0) = 0$, and $F(x) = -\mu((x,0])$ when $x < 0$.

*Proof sketch*. TODO

DEF: Suppose $\mu$ is a finite Borel measure on $\RR$. The cumulative distribution function $F$ associated to the measure $\mu$ is defined at $x \in \RR$ by ... $F(x) = \mu(-\infty, x])$.

DEF: Let $F$ be an increasing, right continuous function, and let $\mu_F$ be its associated measure. Then $\mu_F$ is dubbed ... Lebesgue-Stieltjes measure associated to $F$.

THM: When is it true that for all $E \in \sM_\mu$, we have $\mu(E) = \inf\{\mu(U) : U \supset E \text{ and $U$ is open}\}\\ = \sup\{\mu(K) : K \subset E \text{ and $K$ is compact}\}$? ... When we fix a complete Lebesgue-Stieltjes measure $\mu$ on $\RR$ associated to the increasing, right continuous function $F$, and we denote $\sM_\mu$ the domain of $\mu$.

THM: If $E \subset \RR$, the following are equivalent: [...]; $E = V\setminus N_1$ where $V$ is a $G_\delta$ set and $\mu(N_1) = 0$; $E = H \cup N_2$ where $H$ is an $F_\sigma$ set and $\mu(N_2) = 0$. ... $E \in \sM$

<!---
THM: If $E \subset \RR$, the following are equivalent: $E \in \sM$; $E = V\setminus N_1$ where $V$ is a $G_\delta$ set and $\mu(N_1) = 0$; [...] ... $E = H \cup N_2$ where $H$ is an $F_\sigma$ set and $\mu(N_2) = 0$

THM: If $E \subset \RR$, the following are equivalent: $E \in \sM$; [...]; $E = H \cup N_2$ where $H$ is an $F_\sigma$ set and $\mu(N_2) = 0$. ... $E = V\setminus N_1$ where $V$ is a $G_\delta$ set and $\mu(N_1) = 0$
--->

*Proof sketch.* TODO

PROP! If $\mu(E) < \infty$, the for every $\epsilon > 0$, there's a set $A$ which is a finite union of open intervals such that $\mu(E \triangle A) < \epsilon$. TODO

\renewcommand{\sL}{\mathcal{L}}

DEF! Lebesgue measure $m$ on $\RR$. Lebesgue measurable sets $\sL$. TODO

THM! (Translation invariance) if $E \subset \RR$ and $s,r \in \RR$, let $E+s= \{x+s : x \in E\}$ and $rE = \{rx: x \in E\}$. If $E \in \sL$, then $E + s \in \sL$ and $rE \in \sL$ for all $s$ and $r$, moreover $m(E+s) = m(E)$ and $m(rE) = \abs{r}m(E)$. TODO

### Week 6: summary of measures, review for midterm

I took the midterm today and realized I don't quite understand sets of outer Lebesgue measure zero. 

To summarize concepts I struggled with:

- techniques used to navigate the proofs of basic properties of measures 
    - e.g., monotonicity, continuity from below
- associated Lebesgue-Stieltjes measures $\mu_F$ for an increasing, right continuous function $F$
- "white bread" Lebesgue measures
- the Cantor set as a counter example
<!---
- *timeliness* 
    - e.g., being about two weeks behind in Folland 
    - and therefore being about two weeks behind in comprehension of the lectures
Not sure if I'm continuing in the course or what. Have to ask about the GPA requirement. Can't lose funding over the Lebesgue measure.
--->
