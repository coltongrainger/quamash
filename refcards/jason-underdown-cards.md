---
title: Flash cards from Jason Underdown
author: 
    - Jason Underdown
    - Colton Grainger
date: 2018-08-27
url: https://www.math.utah.edu/~jasonu/flash-cards/
license: CC-2.5
---

Note: These flashcards and the accompanying source code are licensed under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License. I have forked them from https://www.math.utah.edu/~jasonu/flash-cards/. The original author is Jason Underdown. The file is modified for compatibility with mnemosyne.

## Algebra

### Linear algebra

Confound confusing inner ear pneumonics!
	
DEF! A matrix is in row--echelon form when: ... all nonzero rows are above any rows of all zeroes; and the pivot element of a nonzero row is strictly to the right of the pivot of the row above it.

DEF! The rank of a matrix $A$ is (give two characterizations) ... $\mathrm{dim}C(A)$, the dimension of the vector space spanned by its columns; or the number of nonzero rows of $\mathrm{rref}(A)$.

DEF! If a system of equations has at least one solution, then it is said to be ... consistent.

DEF! If a system of equations has no solutions, then it is said to be ... inconsistent (or overdetermined).

THM! A consistent system has how many solutions? ... Either infinitely many (underdeterminied) or exactly one (exactly determined).

DEF! A subset $W$ of $\mathbf{R}^n$ is called a subspace of $\mathbf{R}^n$ if (state three properties): ... $W$ contains the zero vector for $\mathbf{R}^n$. $W$ is closed under addition. $W$ is closed under scalar multiplication.

NOTATION! Suppose we have a linear transformation from $\mathbf{R}^n$ to $\mathbf{R}^m$. Then, up to change of basis, we can represent the transformation with left multiplication of each $x \in \mathbf{R}^n$ by the matrix $A$, where $A$ lives in ... $\mathbf{R}^{n\times m}$.

DEF! What is the kernel of a linear transformation $T: \mathbf{R}^n \to \mathbf{R}^n$ defined by $T(\vec{x}) = A\vec{x}$? ... It's the nullspace $N(A) = \{\vec{x} \in \mathbf{R}^n : A\vec{x} = 0 \}$.

DEF! What is the image of a linear transformation $T: \mathbf{R}^n \to \mathbf{R}^m$ defined by $T(\vec{x}) = A\vec{x}$? ... It's the column space $C(A) = \{A\vec{x} : \vec{x} \in \mathbf{R}^n\}$.

RECALL! Suppose $A \in \mathcal{M}_{3 \times 5}$. Quick! What's the minimum and maximum dimension of the nullspace, $N(A)$?  ... We have $\mathrm{dim}N(A)$ is at most $5$ and at least $2$.

RECALL! Suppose $A \in \mathcal{M}_{5 \times 3}$. Quick! What's the minimum and maximum dimension of the nullspace, $N(A)$?  ... We have $\mathrm{dim}N(A)$ at most $3$ (all $3$-vectors map to $0$) and at least $0$ (only the $(0,0,0)^T$ maps to $0$).

RECALL! Suppose $A \in \mathbf{F}^{j \times k}$, where $j, k \in \mathbf{Z}$. Quick! What're the domain and the co-domain of the linear transformation defined by $T(x) = Ax$? ... $T: \mathbf{F}^k \to \mathbf{F}^j$.

RECALL! Suppose a matrix $A \in \mathcal{M}_{m\times n}$ has more columns than rows, i.e., $n > m$. What are the minimum and maximum dimensions of the nullspace, $N(A)$?  ... At most $n$ (all $n$-vectors $x$ map to $\vec{0}$) and at least $n - m$ (if $A$ has full row rank). 

FACT! Let $T(\vec{x}) = A\vec{x}$ be a linear transformation from $\mathbf{R}^n$ to $\mathbf{R}^m$. Is the image $\mathrm{im}(A)$ a subspace of the domain or co-domain? ... $\mathbf{im}(T)= C(A)$ is a subspace of the co-domain $\mathbf{R}^m$.

FACT! Let $T(\vec{x}) = A\vec{x}$ be a linear transformation from $\mathbf{R}^n$ to $\mathbf{R}^m$. Is the kernel $\mathrm{ker}(A)$ a subspace of the domain or co-domain? ... $\mathbf{ker}(T)= N(A)$ is a subspace of the domain $\mathbf{R}^n$.

DEF! Consider vectors $\vec{v}_1, \ldots, \vec{v}_m$ from a subspace $V$ of $\mathbf{F}^n$.  These vectors are said to form a basis of $V$, if they meet the following two requirements: ... they span $V$, they are linearly independent.

DEF! For any subspace $V$ of $\mathbf{R}^n$, the number of vectors in a basis of $V$ is called the ... dimension of $V$ and is denoted by $\mathrm{dim}(V)$.

DUH! The number of vectors in any basis for a subspace $V$ is  ... $\mathrm{dim} V$.

NOTE! What's an algorithmic construction of a basis of the image $\mathrm{im}(A)$? ... To construct a basis of the image of $A$, pick those column vectors of $A$ that correspond to the columns of $rref(A)$ that contain leading $1$s.

THM! State the rank-nullity theorem. ... For any $m \times n$ matrix $A$ we have $$\mathrm{dim}(\mathrm{im}(A)) + \mathrm{dim}(\mathrm{ker}(A)) = m.$$ Alternatively, defining $\mathrm{dim}(\mathrm{ker}(A))$ as the nullity of $A$, $$\mathrm{rank}(A) + \mathrm{nullity}(A) = m.$$ 

THM! A function $T$ that maps vectors from $\mathbf{F}^n$ to $\mathbf{F}^m$ is called a linear transformation if there is an matrix $A$, living in  ... $A \in \mathbf{F}^{m \times n}$ such that $T(\vec{x}) = A\vec{x}$ for all $\vec{x}$ in $\mathbf{F}^n$.

RECALL! $\mathrm{det}(A^{T})$ in terms of $A$ is ... $\mathrm{det}(A)$.

THM! $\mathrm{ker}(A)$ in terms of a guaranteed square matrix is ... $\mathrm{ker}(A^{T}A)$.

THM! $(\mathrm{im}A)^{\bot}$ in terms of the kernel is ... $\mathrm{ker}(A^{T})$.

RECALL! What's the dressing-undressing principle for transposes of products? ... $(AB)^{T} = B^{T}A^{T}$

DEF! A square matrix $A$ is symmetric when ... $A^{T} = A$

DEF! A square matrix $A$ is skew-symmetric when ... $A^{T} = -A$

<!---

[Definition]{orthogonal complement}

Consider a subspace $V$ of $\mathbf{R}^n$.  The \textit{orthogonal complement}
$V^{\bot}$ of $V$ is the set of those vectors $\vec{x}$ in $\mathbf{R}^n$ that
are orthogonal to all vectors in $V$:
\begin{displaymath}
V^{\bot} = \lbrace \vec{x}: \vec{v}\cdot\vec{x} = 0, \forall \vec{v} \in V \rbrace
\end{displaymath}
Note that $V^{\bot}$ is the kernel of the orthogonal projection onto $V$.



[Theorem]{properties of orthogonal matrices}

\begin{small}
Consider an $n \times n$ matrix $A$.  The following statements are equivalent:

 $A$ is an orthogonal matrix
 The columns of $A$ form an orthonormal basis of $\mathbf{R}^n$
 $A^{T}A = I_{n}$
 $A^{-1} = A^{T}$
 $\forall \vec{x} \in \mathbf{R}^{n} \quad \Vert A\vec{x} \Vert = \Vert \vec{x} \Vert \quad$ (preserves length)

\end{small}



[Theorem]{determinants of similar matrices}

\begin{displaymath}
A \sim B \Rightarrow det(A) = det(B)
\end{displaymath}



[Theorem]{determinant of an inverse}

\begin{displaymath}
det(A^{-1}) = (det A)^{-1} = \frac{1}{det(A)}
\end{displaymath}



[Theorem]{the determinant in terms of the columns}

If A is an $n \times n$ matrix with columns, $\vec{v}_1, \ldots \vec{v}_n$, then,
\begin{displaymath}
\vert det(A) \vert =
\Vert \vec{v}_1 \Vert
\Vert {\vec{v}_2}^{\bot} \Vert
\cdots
\Vert {\vec{v}_n}^{\bot} \Vert
\end{displaymath}
where ${\vec{v}_1}^{\bot}, \ldots {\vec{v}_n}^{\bot}$ are defined as in the Gram-Schmidt process.



[Theorem]{elementary row operations and determinants}

For any $n \times n$ matrix $A$, and any scalar $k$:
\smallskip
\begin{small}
\begin{center}
\begin{tabular}{|p{3cm}|l|}
\hline
Elementary row op & Effect on determinant \\
\hline
scalar multiplication & $det(A) \rightarrow k \cdot det(A)$ \\
\hline
row swap & $det(A) \rightarrow -det(A)$ \\
\hline
multiple of one row added to another & $det(A) \rightarrow det(A)$ \\
\hline
\end{tabular}
\end{center}
\end{small}
\smallskip
Analogous results hold for column operations.



[Definition]{eigenvectors and eigenvalues}

Consider an $\nbyn$ matrix $A$.  A \textbf{nonzero} vector $\vec{v}$ in $\mathbf{R}^n$ is called an \textit{eigenvector} of $A$ if $A\vec{v}$ is a scalar multiple of $\vec{v}$.  That is, if
\begin{displaymath}
A\vec{v} = \lambda\vec{v}
\end{displaymath}
for some scalar $\lambda$.  Note that this scalar may be zero.  This scalar $\lambda$ is caled the \textit{eigenvalue} associated with the eigenvector $\vec{v}$.



[Theorem]{eigenvalues and characteristic equation}

The eigenvalues of an $\nbyn$ matrix $A$ correspond to the solutions of the \textit{characteristic equation} given by:
\begin{displaymath}
\vert A - \lambda I \vert = 0
\end{displaymath}



[Definition]{trace}

The sum of the diagonal entries of a square matrix $A$ is called the \textit{trace} of $A$, and is denoted by $tr(A)$.



[Theorem]{characteristic equation of a $2\!\times\!2$ matrix}

Given a $2\!\times\!2$ matrix $A$:
\begin{displaymath}
det(A - \lambda I) = \lambda^2 - tr(A)\lambda + det(A) = 0
\end{displaymath}



## Abstract Algebra I

[Definition]{set operations}

\begin{eqnarray*}
A \cup B &=& \lbrace x\mid x\in A \;\textrm{or}\; x\in B\rbrace \\
A \cap B &=& \lbrace x\mid x\in A \;\textrm{and}\; x\in B\rbrace \\
A - B &=& \lbrace x\mid x\in A \;\textrm{and}\; x\not\in B\rbrace \\
A + B &=& (A-B) \cup (B-A)\\ 
\end{eqnarray*}



[Theorem]{De Morgan's rules}

For $A$, $B \subseteq S$
\begin{eqnarray*}
(A\cap B)' &=& A' \cup B'\\
(A\cup B)' &=& A' \cap B'
\end{eqnarray*}



[Definition]{surjective or onto mapping}

The mapping $f:S \mapsto T$ is \textit{onto} or \textit{surjective} if every 
$t \in T$ is the image under $f$ of some $s \in S$; that is, iff, $\forall \; t \in T, \quad \exists \; s \in S$ such that $t = f(s)$.



[Definition]{injective or one--to--one mapping}

The mapping $f:S \mapsto T$ is \textit{injective} or \textit{one--to--one} 
\mbox{(1-1)} if for $s_1 \neq s_2$ in $S$, $f(s_1) \neq f(s_2)$ in $T$.

\medskip
Equivalently:
\begin{equation*}
f\; \mathrm{ injective } \Longleftrightarrow f(s_1) = f(s_2) \Rightarrow s_1 = s_2
\end{equation*}



[Definition]{bijection}

The mapping $f:S \mapsto T$ is said to be a \textit{bijection} if $f$ is both 
\mbox{1-1} and onto.



[Definition]{composition of functions}

Suppose $g: S \mapsto T$ and $f: T \mapsto U$, then the \textit{composition}
or \textit{product}, denoted by $f\circ g$ is the mapping $f\circ g: S \mapsto U$
defined by:
\begin{equation*}
(f\circ g)(s) = f(g(s))
\end{equation*}




[Lemma]{composition of functions is associative}

If $h: S \mapsto T, g:T \mapsto U$, and $f: U \mapsto V$, then,
\begin{equation*}
f\circ(g\circ h) = (f\circ g)\circ h
\end{equation*}



[Lemma]{cancellation and composition}

\begin{equation*}
f \circ g = f \,\circ \stackrel{\sim}{g} \; \textrm{and} \; f\;\textrm{is 1--1}
\Rightarrow g = \,\stackrel{\sim}{g}
\end{equation*}
\begin{equation*}
f \circ g = \,\stackrel{\sim}{f} \circ\, g\; \textrm{and $g$ is onto} \;
\Rightarrow f = \,\stackrel{\sim}{f}
\end{equation*}



[Definition]{image and inverse image of a function}

Suppose $f: S\mapsto T$, and $U\subseteq S$, then the \textit{image}
of $U$ under $f$ is
\begin{equation*}
f(U)=\lbrace f(u)\mid u\in U\rbrace
\end{equation*}

\bigskip
If $V\subseteq T$ then the \textit{inverse image} of $V$ under $f$ is
\begin{equation*}
f^{-1}(V) = \lbrace s\in S \mid f(s) \in V\rbrace
\end{equation*}



[Definition]{inverse function}

Suppose $f: S\mapsto T$.  An \textit{inverse} to $f$ is a function
$f^{-1}:T\mapsto S$ such that
\begin{eqnarray*}
f\circ f^{-1} &=& i_T\\
f^{-1}\circ f &=& i_S
\end{eqnarray*}
Where $i_T:T\mapsto T$ is defined by $i_T(t) = t$, and is called the
\textit{identity function} on $T$.  And similarly for $S$. 



[Definition]{$A(S)$}

If $S$ is a nonempty set, then $A(S)$ is the set of all 1--1 mappings of $S$
onto itself.

\medskip
When $S$ has a finite number of elements, say $n$, then $A(S)$ is called the
\textit{symmetric group of degree n} and is often denoted by $S_n$.



[Lemma]{properties of $A(S)$}

$A(S)$ satisfies the following:

 $f,g \in A(S)\Rightarrow f\circ g \in A(S)$
 $f,g,h \in A(S)\Rightarrow (f\circ g)\circ h = f\circ (g\circ h)$
 There exists an $i$ such that $f\circ i = i\circ f = f$\
$\forall f \in A(S)$
 Given $f \in A(S)$, there exists a $g \in A(S)$ such~that 
$f\circ g = g\circ f = i$ 




[Definition]{group}

A nonempty set $G$ together with some operator $*$ is said to be a \textit{group} if:

 If $a, b \in G$ then $a*b \in G$
 If $a, b, c \in G$ then $a*(b*c) = (a*b)*c$
 $G$ has an identity element $e$ such that 
\mbox{$a*e=e*a=a \;\; \forall \> a \in G$}
 $\forall \> a \in G, \;\; \exists \> b \in G $ such that
\mbox{$a*b=b*a=e$}




[Definition]{order of a group}

The number of elements in $G$ is called the \textit{order} of $G$ and 
is denoted by $\vert G \vert$.



[Definition]{abelian}

A group $G$ is said to be \textit{abelian} if $\quad \forall \; a,b\in G$
\begin{equation*}
a*b=b*a
\end{equation*}



[Lemma]{properties of groups}

If $G$ is a group then

 Its identity element, $e$ is unique.
 Every $a \in G$ has a unique inverse $a^{-1} \in G$.
 If $a \in G$, then $(a^{-1})^{-1}=a$.
 For $a,b \in G$, \mbox{$(ab)^{-1} = b^{-1}a^{-1}$}, where
$ab=a*b$.




[Definition]{subgroup}

A nonempty subset, $H$ of a group $G$ is called a \mbox{\textit{subgroup}}
of $G$ if, relative to the operator in $G$, $H$ itself forms a group.



[Lemma]{when is a subset a subgroup}

A nonempty subset $A\subset G$ is a subgroup $\Leftrightarrow$ \
$A$ is closed with respect to the operator of $G$ and given $a \in A$ then $a^{-1} \in A$.



[Definition]{cyclic subgroup}

A \textit{cyclic subgroup} of $G$ is generated by a single element $a \in G$ and is denoted by $(a)$.
\begin{equation*}
(a) = \left\lbrace a^i \mid i \; \textrm{any integer} \right\rbrace
\end{equation*}



[Lemma]{finite subsets and subgroups}

Suppose that $G$ is a group and $H$ a nonempty \textit{finite} subset of $G$
closed under the operation in $G$.  Then $H$ is a subgroup of $G$.

\textbf{Corollary}  If $G$ is a \textit{finite} group and $H$ a nonempty subset of $G$
closed under the operation of $G$, then $H$ is a subgroup of $G$.



[Lemma]{subgroups under $\cap$ and $\cup$}

Suppose $H$ and $H'$ are subgroups of $G$, then

 $H \cap H'$ is a subgroup of $G$
 $H \cup H'$ is \textbf{not} a subgroup of $G$, as long as neither
$H$ nor $H'$ is contained in the other.




[Definition]{equivalence relation}

A relation $\sim$ on elements of a set $S$ is an \textit{equivalence relation}
if for all $a, b, c \in S$ it satisfies the following criteria:

 $a \sim a$ reflexivity
 $a \sim b \Rightarrow b \sim a$ symmetry
 $a \sim b$ and $b \sim c \Rightarrow a \sim c$ transitivity




[Definition]{equivalence class}

If $\sim$ is an equivalence relation on a set $S$, then the
\textit{equivalence class} of $a$ denoted $[a]$ is defined to be:
\begin{equation*}
[a] = \left\lbrace b \in S \mid b \sim a\right\rbrace 
\end{equation*}



[Theorem]{equivalence relations partition sets}

If $\sim$ is an equivalence relation on a set $S$, then $\sim$ partitions $S$
into equivalence classes.  That is, for any $a, b \in S$ either:
\begin{equation*}
[a] = [b] \quad \textrm{or} \quad [a] \cap [b] = \oslash
\end{equation*}



[Theorem]{Lagrange's theorem}

If $G$ is a finite group and $H$ is a subgroup of $G$, then the order of $H$ divides the order of $G$.  That is,
\begin{equation*}
\left| G \right| = k \left| H \right|
\end{equation*}
for some integer $k$.  The converse of Lagrange's theorem is not generally true.



[Definition]{index of a subgroup}

If $G$ is a finite group, and $H$ a subgroup of $G$, then the
\textit{index} of $H$ in $G$ is the number of distinct right cosets
of $H$ in $G$, and is denoted:
\begin{equation*}
[G : H] = \dfrac{|G|}{|H|} = i_{G}(H)
\end{equation*}



[Definition]{order of an element in a group}

If $a$ is an element of $G$ then the \textit{order} of $a$ denoted by $o(a)$ is the least positive integer $m$ such that $a^m = e$.



[Theorem]{finite groups wrap around}

If $G$ is a finite group of order $n$ then $a^n = e$ for all $a \in G$.



[Definition]{homomorphism}

If $G$ and $G'$ are two groups, then the mapping
\begin{equation*}
f: G\rightarrow G'
\end{equation*}
is a \textit{homomorphism} if 
\begin{equation*}
f(ab) = f(a)f(b) \qquad \forall \; a,b \in G
\end{equation*}



[Definition]{monomorphism, isomorphism, automorphism}

\begin{small}
Suppose the mapping $f: G\rightarrow G'$ is a homomorphism, then:

 If $f$ is 1--1 it is called a \textit{monomorphism}.
 If $f$ is 1--1 and onto, then it is called an \mbox{\textit{isomorphism}}.
 If $f$ is an isomorphism that maps $G$ onto itself then it is called
an \textit{automorphism}.
 If an isomorphism exists between two groups then they are said to be
\textit{isomorphic} and denoted $G\simeq G'$.

\end{small}



[Theorem]{composition of homomorphisms}

Suppose $f : G \mapsto G'$ and $h : G' \mapsto G''$ are homomorphisms,
then the composition of $h$ with $f$, $h\circ f$ is also a homomorphism.



[Definition]{kernel}

If $f$ is a homomorphism from $G$ to $G'$ then the \textit{kernel}
of $f$ is denoted by $\textrm{Ker}f$ and defined to be
\begin{equation*}
\textrm{Ker}f = \lbrace a \in G \mid f(a)=e' \rbrace
\end{equation*}



[Theorem]{kernel related subgroups}

If $f$ is a homomorphism of $G$ into $G'$, then

 $\textrm{Ker} f$ is a subgroup of $G$.
 If $a \in G$ then $a^{-1}(\textrm{Ker} f) a \subset \textrm{Ker} f$.




[Definition]{normal subgroup}

A subgroup $N$ of $G$ is said to be a \textit{normal subgroup}
of $G$ if $a^{-1}Na \subset N$ for each $a \in G$.
\medskip
\\
$N$ normal to $G$ is denoted $N \lhd G$.



[Theorem]{normal subgroups and their cosets}

$N \lhd G$ iff every left coset of $N$ in $G$ is also a right
coset of $N$ in $G$.



[Definition/Theorem]{factor group}

If $N \lhd G$, then we define the \textit{factor group}
of $G$ by $N$ denoted $G/N$ to be:
\begin{equation*}
G/N = \lbrace Na \mid a \in G \rbrace = 
\lbrace [a] \mid a \in G \rbrace
\end{equation*}
\medskip
$G/N$ is a group relative to the operation
\begin{equation*}
(Na)(Nb) = Nab
\end{equation*}



[Theorem]{normal subgroups are the kernel of a homomorphism}

If $N \lhd G$, then there is a homomorphism $\psi : G \mapsto G/N$
such that $\textrm{Ker} \psi = N$.



[Theorem]{order of a factor group}

If $G$ is a finite group and $N \lhd G$, then
\begin{equation*}
\left| G/N \right| = \frac{\left| G \right|}{\left| N \right|}
\end{equation*}



[Theorem]{Cauchy's theorem}

If $p$ is a prime that divides $\left| G \right|$,
then $G$ has an element of order $p$.



[Theorem]{first homomorphism theorem}

If $\varphi : G \mapsto G'$ is an onto homomorphism with kernel $K$ then,
\begin{equation*}
G/K \simeq G'
\end{equation*}
with isomorphism $\psi : G/K \mapsto G'$ defined by
\begin{equation*}
\psi (Ka) = \varphi(a)
\end{equation*}



[Theorem]{correspondence theorem}

Let $\varphi : G \mapsto G'$ be a homomorphism which maps $G$
onto $G'$ with kernel $K$.  If $H'$ is a subgroup of $G'$, and if
$H' = \lbrace a \in G \mid \varphi (a) \in H' \rbrace$ then

 $H$ is a subgroup of $G$
 $K \subset H$
 $H/K \simeq H'$

Also, if $H' \lhd G'$ then $H \lhd G$.



[Theorem]{second isomorphism theorem}

Let $H$ be a subgroup of $G$ and $N \lhd G$, then

 $HN = \lbrace hn \mid h\in H, n\in N \rbrace$ is a subgroup of $G$
 $H\cap N \lhd H$
 $H/(H\cap N) \simeq (HN)/N$




[Theorem]{third isomorphism theorem}

If $\varphi : G \mapsto G'$ is an onto homomorphism with kernel $K$ and
if $N' \lhd G'$ with 
$N = \lbrace a \in G \mid \varphi (a) \in N' \rbrace$ then
\begin{equation*}
G/N \simeq G'/N'
\end{equation*}
\begin{center}
or equivalently
\end{center}
\begin{equation*}
G/N \simeq \frac{G/K}{N/K}
\end{equation*}



[Theorem]{groups of order $pq$}

If $G$ is a group of order $pq$ ($p$ and $q$ primes) where
$p > q$ and $q \not{\mid} \; p-1$ then $G$ must be cyclic.



[Definition]{external direct product}

Suppose $G_{1},\ldots,G_{n}$ is a collection of groups.  The
\textit{external direct product} of these $n$ groups is the set
of all $n$--tuples for which the $i$th component is an element of
$G_{i}$.
\begin{equation*}
G_{1}\times G_{2}\times \ldots\times G_{n} =
\left\lbrace \left( g_{1},g_{2},\ldots,g_{n}\right)
\mid g_{i} \in G_{i}\right\rbrace 
\end{equation*}
The product is defined component--wise.
\begin{equation*}
\left(a_{1},a_{2},\ldots,a_{n} \right)
\left(b_{1},b_{2},\ldots,b_{n}  \right) =
\left( a_{1}b_{1},a_{2}b_{2},\ldots,a_{n}b_{n} \right) 
\end{equation*}



[Definition]{internal direct product}

A group $G$ is said to be the \textit{internal direct product}
of its normal subgroups $N_{1},N_{2},\ldots,N_{n}$ if every element of
$G$ has a unique representation, that is, if $a \in G$ then:
\begin{equation*}
a = a_{1},a_{2},\ldots,a_{n}  \text{ where each } a_{i} \in N_{i}
\end{equation*}



[Lemma]{intersection of normal subgroups when the group
is an internal direct product}

If $G$ is the internal direct product of its normal subgroups
$N_{1},N_{2},\ldots,N_{n}$, then for $i \neq j, N_{i} \cap N_{j} = 
\left\lbrace e \right\rbrace $.



[Theorem]{isomorphism between an external direct product
and an internal direct product}

Let $G$ be a group with normal subgroups $N_{1},N_{2},\ldots,N_{n}$, then the
mapping:
\begin{equation*}
\psi : N_{1} \times N_{2} \times \cdots \times N_{n} \mapsto G
\end{equation*}
defined by
\begin{equation*}
\psi((a_{1},a_{2},\ldots,a_{n})) = a_{1}a_{2}\cdots a_{n}
\end{equation*}
is an isomorphism iff $G$ is the internal direct product of 
$N_{1},N_{2},\ldots,N_{n}$.



[Theorem]{fundamental theorem on finite abelian groups}

A finite abelian group is the direct product of cyclic groups. 



[Definition]{centralizer of an element}

If $G$ is a group and $a \in G$, then the \textit{centralizer} of $a$ in $G$ is the
set of all elements in $G$ that commute with $a$.
\begin{equation*}
C(a) = \left\lbrace g \in G \mid ga = ag \right\rbrace 
\end{equation*}



[Lemma]{the centralizer forms a subgroup}

If $a \in G$, then $C(a)$ is a subgroup of $G$.



[Theorem]{number of distinct conjugates of an element}

Let $G$ be a finite group and $a \in G$, then the number of distinct
conjugates of $a$ in $G$ is $[G : C(a)]$ (the index of $C(a)$ in $G$).



[Theorem]{the class equation}

\begin{equation*}
|G| = |Z(G)| + \sum_{a \not{\in} Z(G)}[G : C(a)]
\end{equation*}



[Theorem]{groups of order $p^{n}$}

If $G$ is a group of order $p^{n}$, ($p$ prime) then $Z(G)$ is
non--trivial, i.e. there exists at least one element other than
the identity that commutes with all other elements of $G$.



[Theorem]{groups of order $p^{2}$}

If $G$ is a group of order $p^{2}$ ($p$ prime), then $G$ is abelian.



[Theorem]{groups of order $p^{n}$ contain a normal 
subgroup}

If $G$ is a group of order $p^{n}$ ($p$ prime), then $G$ contains
a normal subgroup of order $p^{n-1}$.



[Definition]{$p$--Sylow group}

If $G$ is a group of order $p^{n}m$ where $p$ is prime and 
$p \not{\mid} \: m$, then $G$ is a $p$--Sylow group.



[Theorem]{Sylow's theorem (part 1)}

If $G$ is a $p$--Sylow group ($|G| = p^{n}m$),
then $G$ has a subgroup of order $p^{n}$.



[Theorem]{Sylow's theorem (part 2)}

If $G$ is a $p$--Sylow group ($|G| = p^{n}m$), then any 
two subgroups of the same order are conjugate.  For example,
if $P$ and $Q$ are subgroups of $G$ where $|P|=|Q|=p^{n}$ then
\begin{equation*}
P = x^{-1}Qx \quad \text{ for some } x \in G
\end{equation*}



[Theorem]{Sylow's theorem (part 3)}

If $G$ is a $p$--Sylow group ($|G| = p^{n}m$),
then the number of subgroups of order $p^{n}$ in $G$ is
of the form $1 + kp$ and divides $|G|$.



\end{document}




\section{Real Analysis I}

\usepackage{amssymb}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{mathrsfs}
\usepackage{datetime}

\newcommand{\N}{\mathbb{N}}
\newcommand{\Z}{\mathbb{Z}}
\newcommand{\Q}{\mathbb{Q}}
\newcommand{\R}{\mathbb{R}}
\newcommand{\st}{\textrm{ such that }}



[Copyright \& License]{Copyright \copyright \,
2007 Jason Underdown \\Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 3.0 License.
For more information, see creativecommons.org.
You can contact the author at:
\begin{center}
\begin{small}\tt jasonu at physics utah edu\end{small}

\medskip
File last updated on \today, \\
at \currenttime
\end{center}



% Section 1 Logical Connectives

[Definition]{statement}

A sentence that can unambiguously be classified as true or false.



[Definition]{sentential connectives}

\begin{center}
not, and, or, if \ldots then, if and only if
\end{center}



[Definition]{negation}

Let $p$ stand for a statement, then $\sim p$ (read \textit{not} $p$)
represents the logical opposite or \textbf{negation} of $p$.



[Definition]{conjunction}

If $p$ and $q$ are statements, then the statement
$p$ \textit{and} $q$ (called the \textbf{conjunction}
of $p$ and $q$ and denoted $\mathbf{p \wedge q}$)
is true only when both $p$ and $q$ are true, and false otherwise.
\begin{equation*}
\begin{array}{c|c|c}
p & q & p \wedge q \\
\hline
T & T & T\\ 
T & F & F\\ 
F & T & F\\ 
F & F & F\\
\hline
\end{array}
\end{equation*}



[Definition]{disjunction}

If $p$ and $q$ are statements, then the statement $p$ \textit{or} $q$
(called the \textbf{disjunction} of $p$ and $q$ and denoted
$\mathbf{p \vee q}$) is true unless both $p$ and $q$ are false.
\begin{equation*}
\begin{array}{c|c|c}
p & q & p \vee q \\
\hline
T & T & T\\ 
T & F & T\\ 
F & T & T\\ 
F & F & F\\
\hline
\end{array}
\end{equation*}



[Definition]{implication or conditional}

A statement of the form
\begin{center}
 \textit{if p then q}
\end{center}
is called an \textbf{implication} or \textbf{conditional}.
\begin{equation*}
\begin{array}{c|c|c}
p & q & p \Rightarrow q \\
\hline
T & T & T\\ 
T & F & F\\ 
F & T & T\\ 
F & F & T\\
\hline
\end{array}
\end{equation*}



[Definition]{antecedant \& consequent \\
hypothesis \& conclusion}

\begin{center}
If $p$, then $q$.
\end{center}
In the above, the statement $p$ is called the \mbox{\textbf{antecedant}}
or \mbox{\textbf{hypothesis}}, and the statement $q$ is called the
\mbox{\textbf{consequent}} or \mbox{\textbf{conclusion}}.



[Definition]{equivalence}

A statement of the form ``$p$ if and only if $q$'' is the conjunction
of two implications and is called an \textbf{equivalence}.



[Definition]{negation of a conjunction}

\begin{equation*}
\sim (p \wedge q) \Leftrightarrow (\sim p) \vee (\sim q)
\end{equation*}



[Definition]{negation of a disjunction}

\begin{equation*}
\sim (p \vee q) \Leftrightarrow (\sim p) \wedge (\sim q)
\end{equation*}



[Definition]{negation of an implication}

\begin{equation*}
\sim (p \Rightarrow q) \Leftrightarrow p \wedge (\sim q)
\end{equation*}



[Definition]{tautology}

A sentence whose truth table contains only T is called a \textbf{tautology}.
The following sentences are examples of tautologies
($c \equiv$ contradiction):
\begin{eqnarray*}
(p \Leftrightarrow q) & \Leftrightarrow &
(p\Rightarrow q) \wedge (q\Rightarrow p)\\
(p \Rightarrow q) & \Leftrightarrow &
(\sim q \Rightarrow \sim p)\\
(p \Rightarrow q) & \Leftrightarrow &
\left[(p \wedge \sim q) \Rightarrow c \right]
\end{eqnarray*}



% Section 2 Quantifiers

[Definition]{universal quantifier}

\begin{equation*}
\forall \; x, \ p(x)
\end{equation*}
In the above statement, the \textbf{universal quantifier} denoted by
$\forall$ is read ``for all'', ``for each'', or ``for every''.



[Definition]{existential quantifier}

\begin{equation*}
\exists \ x \ni p(x)
\end{equation*}
In the above statement, the \textbf{existential quantifier} denoted by
$\exists$ is read ``there exists \ldots'', ``there is at least one
\ldots''.  The symbol $\ni$ is just shorthand for ``such that''.



% Section 3 Techniques of Proof I

[Definition]{contrapositive}

The implication $p \Rightarrow q$ is logically equivalent with its
\mbox{\textbf{contrapositive}}:
\begin{equation*}
\sim q \Rightarrow \sim p
\end{equation*}



[Definition]{converse}

Given the implication $p \Rightarrow q$ then its
\mbox{\textbf{converse}} is
\begin{equation*}
q \Rightarrow p
\end{equation*}
But they are \textit{not} logically equivalent.



[Definition]{inverse}

Given the implication $p \Rightarrow q$ then its
\mbox{\textbf{inverse}} is
\begin{equation*}
\sim p \Rightarrow \sim q
\end{equation*}
An implication is \textit{not} logically equivalent to its inverse.
The inverse is the contrapositive of the converse.




[Definition]{contradiction}

A \textbf{contradiction} is a statement that is always false.
Contradictions are symbolized by the letter $c$ or by two arrows
pointing directly at each other.
\begin{equation*}
\Rightarrow \Leftarrow
\end{equation*}



% Section 4 Techniques of Proof II

% Section 5 Basic Set Operations

[Definition]{subset}

Let $A$ and $B$ be sets.  We say that $A$ is a \mbox{\textbf{subset}}
of $B$ if every element of $A$ is an element of $B$.  In symbols, this
is denoted
\begin{equation*}
A \subseteq B \textrm{ or } B \supseteq A
\end{equation*}



[Definition]{proper subset}

Let $A$ and $B$ be sets. $A$ is a \mbox{\textbf{proper subset}} of $B$
if $A$ is a subset of $B$ and there exists an element in $B$
that is not in $A$.



[Definition]{set equality}

Let $A$ and $B$ be sets.  We say that $A$ is a \mbox{\textbf{equal}} to $B$
if $A$ is a subset of $B$ and $B$ is a subset of $A$.
\begin{equation*}
A = B \Leftrightarrow A \subseteq B \textrm{ and } B \subseteq A
\end{equation*}



[Definition]{union, intersection, complement, disjoint}

Let $A$ and $B$ be sets.
\begin{eqnarray*}
A \cup B &=& \{ x: x \in A \textrm{ or } x \in B \} \\
A \cap B &=& \{ x: x \in A \textrm{ and } x \in B \} \\
A \setminus B &=& \{ x: x \in A \textrm{ and } x \not \in B \}
\end{eqnarray*}
If $A \cap B = \varnothing$ then $A$ and $B$ are said to be
\mbox{\textbf{disjoint}}.



[Definition]{indexed family of sets}

If for each element $j$ in a nomempty set $J$
there corresponds a set $A_{j}$, then
\begin{equation*}
\mathscr{A} = \{ A_{j} : j \in J \}
\end{equation*}
is called an \textbf{indexed family of sets} with $J$ as the index set.



[Definition]{pairwise disjoint}

If $\mathscr{A}$ is a collection of sets, then $\mathscr{A}$ is called
\mbox{\textbf{pairwise disjoint}} if 
\begin{equation*}
\forall \ A,B \in \mathscr{A}, \textrm{ where } A \neq B
\textrm{ then } A \cap B  = \varnothing
\end{equation*}



% Section 6 Relations

[Definition]{ordered pair}

The \mbox{\textbf{ordered pair}}  $(a,b)$ is the set whose members are
$\{ a \}$ and $\{ a, b \}$.
\begin{equation*}
(a,b) = \{ \{a \} , \{ a,b \} \}
\end{equation*}



[Definition]{Cartesian product}

If $A$ and $B$ are sets,then the \mbox{\textbf{Cartesian product}} or
\mbox{\textbf{cross product}} of $A$ and $B$ is the set of all ordered
pairs $(a,b)$ such that $a \in A$ and $b \in B$.
\begin{equation*}
A \times B = \{ (a,b) : a \in A \textrm{ and } b \in B \}
\end{equation*}



[Definition]{relation}

Let $A$ and $B$ be sets.  A \mbox{\textbf{relaton}} between
$A$ and $B$ is any subset \textsf{R} of $A \times B$.
\begin{equation*}
a \textsf{R} b \Leftrightarrow (a,b) \in \textsf{R}
\end{equation*}



[Definition]{equivalence relation}

A relation \textsf{R} on a set $S$ is an \mbox{\textbf{equivalence relation}}
if for all $x, y, z \in S$ it satisfies the following criteria:

 $x \textsf{R} x$ reflexivity
 $x \textsf{R} y \Rightarrow y \textsf{R} x$ symmetry
 $x \textsf{R} y$ and $y \textsf{R} z \Rightarrow
x \textsf{R} z$ transitivity




[Definition]{equivalence class}

The \textbf{equivalence class} of $x \in S$ with respect to an equivalence 
relation \textsf{R} is the set
\begin{equation*}
E_{x} = \left\lbrace y \in S : y \textsf{R} x\right\rbrace 
\end{equation*}



[Theorem]{partition}

A \textbf{partition} of a set $S$ is a collection $\mathscr{P}$
of nonempty subsets of $S$ such that

 Each $x \in S$ belongs to some subset $A \in \mathscr{P}$.
 For all $A, B \in \mathscr{P}$, if $A \neq B$,
then $A \cap B = \varnothing$

A member of a set $\mathscr{P}$ is called a \textbf{piece} of the partition.



% Section 7 Functions

[Definition]{function between $A$ and $B$}

Let $A$ and $B$ be sets.  A \mbox{\textbf{function between $A$ and $B$}}
is a nonempty relation $f \subseteq A \times B$ such that
\begin{equation*}
\left[ (a,b) \in f \textrm{ and } (a,b') \in f \right] \Longrightarrow b=b'
\end{equation*}



[Definition]{domain}

Let $A$ and $B$ be sets, and let $f \subseteq A \times B$ be a function
between $A$ and $B$.  The \textbf{domain} of $f$ is the set of all first
elements of members of $f$.
\begin{equation*}
\textrm{dom } f = \{ a \in A : \exists \; b \in B \ni (a,b) \in f \}
\end{equation*}



[Definition]{range \& codomain}

Let $A$ and $B$ be sets, and let $f \subseteq A \times B$ be a function
between $A$ and $B$.  The \textbf{range} of $f$ is the set of all second
elements of members of $f$.
\begin{equation*}
\textrm{rng } f = \{ b \in B : \exists \; a \in A \ni (a,b) \in f \}
\end{equation*}
The set $B$ is referred to as the \mbox{\textbf{codomain}} of $f$.



[Definition]{surjective or onto}

The function $f:A \rightarrow B$ is \textbf{surjective} or \textbf{onto}
if $B = \textrm{rng } f$.  Equivalently,
\begin{equation*}
\forall \; b \in B, \quad \exists \; a \in A \ni b = f(a)
\end{equation*}



[Definition]{injective or 1--1}

The function $f:A \rightarrow B$ is \textbf{injective} or \mbox{(1--1)}
if:
\begin{equation*}
\forall \ a, a' \in A, \quad f(a) = f(a') \Longrightarrow a = a'
\end{equation*}



[Definition]{bijective}

A function $f:A \rightarrow B$ is said to be \textbf{bijective}
if $f$ is both surjective and injective.



[Definition]{characteristic or indicator function}

Let $A$ be a nonempty set and let $S \subseteq A$, then the
\mbox{\textbf{characteristic function}} $\chi_{S} : A \rightarrow \{ 0,1 \}$
is defined by
\begin{equation*}
\chi_{S}(a) = \left\{ \begin{array}{ll}
  0 & a \notin S \\
  1 & a \in S
\end{array} \right.
\end{equation*} 



[Definition]{image and pre-image}

Suppose $f: A\rightarrow B$, and $C\subseteq A$, then the \textbf{image}
of $C$ under $f$ is
\begin{equation*}
f(C)=\{ f(x): x\in C\}
\end{equation*}

\bigskip
If $D\subseteq B$ then the \textbf{pre-image} of $D$ in $f$ is
\begin{equation*}
f^{-1}(D) = \{ x\in A : f(x) \in D\}
\end{equation*}



[Definition]{composition of functions}

Suppose $f: A \rightarrow B$ and $g: B \rightarrow C$, then the
\mbox{\textbf{composition}} of $g$ with $f$ denoted by
$g\circ f: A \rightarrow C$ is given by
\begin{equation*}
(g\circ f)(x) = g(f(x))
\end{equation*}
In terms of ordered pairs this means
\begin{equation*}
g\circ f =
\{(a,c) \in A \times C :
\exists \ b \in B \ni (a,b) \in f \wedge (b,c) \in g \}
\end{equation*}



[Definition]{inverse function}

Let $f: A\rightarrow B$ be bijective.  The
\mbox{\textbf{inverse function}} of $f$ is the function $f^{-1}:B
\rightarrow A$ given by
\begin{equation*}
f^{-1} = \{(y,x) \in B \times A : (x,y) \in f \}
\end{equation*}



[Definition]{identity function}

A function that maps a set $A$ onto itself is called the
\mbox{\textbf{identity function}} on $A$, and is denoted $i_{A}$.

\medskip
If $f: A \rightarrow B$ is a bijection, then
\begin{eqnarray*}
f^{-1} \circ f &=& i_{A} \\
f \circ f^{-1} &=& i_{B}
\end{eqnarray*}



% Section 8 Cardinality

[Definition]{equinumerous}

Two sets $S$ and $T$ are \mbox{\textbf{equinumerous}}, denoted
$S \sim T$, if there exists a bijection from $S$ onto $T$.



[Definition]{finite \& infinite sets}

A set $S$ is said to be \textbf{finite} if $S = \varnothing$ or if
there exists an $n \in \N$ and a bijection
\begin{equation*}
f: \{1,2,\ldots,n\} \rightarrow S.
\end{equation*}
If a set is not finite, it is said to be \textbf{infinite}.



[Definition]{cardinal number \& transfinite}

Let $I_{n} = \{1,2,\ldots ,n \}$.  The \mbox{\textbf{cardinal number}}
of $I_{n}$ is $n$.  Let $S$ be a set.  If $S \sim I_{n}$ then
$S$ has $n$ elements.

\bigskip
The cardinal number of $\varnothing$ is defined to be $0$.

\bigskip
Finally, if a cardinal number is not finite, it is said to be
\mbox{\textbf{transfinite}}.



[Definition]{denumerable}

A set $S$ is said to be \textbf{denumerable} if there exists a
bijection
\begin{equation*}
f: \N \rightarrow S
\end{equation*}



[Definition]{countable \& uncountable}

If a set is finite or denumerable, then it is \mbox{\textbf{countable}}.

\bigskip
If a set is not countable, then it is \mbox{\textbf{uncountable}}.



[Definition]{power set}

Given any set $S$, the \textbf{power set} of $S$ denoted by
$\mathscr{P}(S)$ is the collection of all possible subsets of $S$.



[Definition]{continuum hypothesis}

Given that $|\N| = \aleph_{0}$ and $|\R| = c$, we know
that $c > \aleph_{0}$, but is there any set with cardinality say $\lambda$
such that $\aleph_{0} < \lambda < c \ $?

\bigskip
The conjecture that there is no such set was first made by Cantor and is
known as the \mbox{\textbf{continuum hypothesis}}.



[Definition]{algebraic \& transcendental}

A real number is said to be \textbf{algebraic} if it is a root of a 
polynomial with integer coefficients.

\bigskip
If a number is not algebraic, it is called \textbf{transcendental}.



% Section 10 Natural Numbers and Induction

[Axiom]{well--ordering property of $\N$}

If $S$ is a nonempty subset of $\N$, then there exists an element
$m \in S$ such that $ \forall \ k \in S \ m \leq k$.



[Definition]{basis for induction, induction step,
induction hypothesis}

In the \textit{Principle of Mathematical Induction}, part (1) which refers
to $P(1)$ being true is known as the \mbox{\textbf{basis for induction}}.

\bigskip
Part (2) where one must show that $\forall \ k \in \N, P(k)
\Rightarrow P(k+1)$ is known as the \mbox{\textbf{induction step}}.

\bigskip
Finally, the assumption in part (2) that $P(k)$ is true is known as the
\mbox{\textbf{induction hypothesis}}.



[Definition]{recursion relation or recurrence relation}

A \textbf{recurrence relation} is an equation that defines a sequence
recursively: each term of the sequence is defined as a function of the
preceding terms.

\medskip
The Fibonacci numbers are defined using the linear recurrence relation:
\begin{eqnarray*}
F_n &=& F_{n-2} + F_{n-1}\\
F_{1} &=& 1\\
F_{2} &=& 1
\end{eqnarray*}



% Section 11 Ordered Fields

[Axiom]{field axioms}

\begin{small}
\begin{center}
\begin{tabular}{l}
A1 Closure under addition \\
A2 Addition is commutative \\ 
A3 Addition is associative \\
A4 Additive identity is $0$ \\ 
A5 Unique additive inverse of $x$ is $-x$ \\
M1 Closure under multiplication \\
M2 Multiplication is commutative \\
M3 Multiplication is associative \\
M4 Multiplicative identity is $1$ \\
M5 If $x \neq 0$, then the unique multiplicative inverse is $1/x$ \\
DL $\forall \ x,y,z \in \R, x(y+z) = xy + xz$
\end{tabular}
\end{center}
\end{small}



[Axiom]{order axioms}


[O1] $\forall \ x,y \in \R$ exactly one of the relations \\
$x=y, x<y, x>y$ holds. (trichotomy)
[O2] $\forall \ x,y,z \in \R$, $x<y \textrm{ and } y<z 
\Rightarrow x<z$. \\(transitivity)
[O3] $\forall \ x,y,z \in \R$, $x<y \Rightarrow x+z<y+z$
[O4] $\forall \ x,y,z \in \R$, $x<y \textrm{ and } z>0 
\Rightarrow xz<yz$.




[Definition]{absolute value}

If $x \in \R$, then the \mbox{\textbf{absolute value}} of $x$,
is denoted $|x|$ and defined to be
\begin{equation*}
|x| = \left\{ \begin{array}{rl}
   x & x \geq 0 \\
  -x & x < 0
\end{array} \right.
\end{equation*} 



[Theorem]{triangle inequality}

Let $x,y \in \R$ then
\begin{equation*}
|x+y| \leq |x| + |y|
\end{equation*}
alternatively,
\begin{equation*}
|a-b| \leq |a-c| + |c-b|
\end{equation*}



[Definition]{ordered field}

If $S$ is a field and satisfies (O1--O4) of the order axioms,
then $S$ is an \mbox{\textbf{ordered field}}.



% Section 12 The Completeness Axiom

[Definition]{irrational number}

Suppose $x \in \R$.  If $x \neq \frac{m}{n}$ for some $m,n \in 
\Z$, then $x$ is \mbox{\textbf{irrational}}.



[Definition]{upper \& lower bound}

Let $S$ be a subset of $\R$.  If there exists an $m \in \R$ such that
$m \geq s \quad \forall \ s \in S$, then $m$ is called an
\mbox{\textbf{upper bound}} of $S$.

\bigskip
Similarly, if $m \leq s \quad \forall \ s \in S$, then $m$ is called a
\mbox{\textbf{lower bound}} of $S$.



[Definition]{bounded}

A set $S$ is said to be \textbf{bounded} if it is bounded above
and bounded below.



[Definition]{maximum \& minimum}

If $m$ is an upper bound of $S$ and also in $S$, then
$m$ is called the \mbox{\textbf{maximum}} of $S$.

\bigskip
Similarly, if $m$ is a lower bound of $S$ and also in $S$, 
then $m$ is called the \mbox{\textbf{minimum}} of $S$.



[Definition]{supremum}

Let $S$ be a nonempty subset of $\R$.  If $S$ is bounded above, then
the \mbox{\textbf{least upper bound}} is called the
\mbox{\textbf{supremum}}, and is denoted sup $S$.

\medskip
$m = \textrm{sup } S \Leftrightarrow$

 [(a)] $m \geq s, \ \forall \ s \in S$ and
 [(b)] if $m'<m$, then $\exists \; s' \in S \ni s'>m'$




[Definition]{infimum}

Let $S$ be a nonempty subset of $\R$.  If $S$ is bounded below, then
the \mbox{\textbf{greatest lower bound}} is called the
\mbox{\textbf{infimum}}, and is denoted inf $S$.

\medskip
$m = \textrm{inf } S \Leftrightarrow$

 [(a)] $m \leq s, \ \forall \ s \in S$ and
 [(b)] if $m'>m$, then $\exists \; s' \in S \ni s'<m'$




[Axiom]{Completeness Axiom}

Every nonempty subset $S$ of $\R$ that is bounded above has a 
least upper bound.  That is, sup $S$ exists and is a real number.



[Definition]{Archimedean ordered field}

An ordered field $F$ has the \textbf{Archimedean property} 
if 
\begin{equation*}
\forall \ x \in F \quad \exists \; n \in \N \ni x<n
\end{equation*}



[Definition]{dense}

A set $S$ is \textbf{dense} in a set $T$ if
\begin{equation*}
\forall \; t_1, t_2 \in T \quad \exists \; s \in S \ni t_1<s<t_2
\end{equation*}



[Definition]{extended real numbers}

For convenience, we extend the set of real numbers with two symbols
$\infty$ and $-\infty$, that is $\R \cup \{ \infty , -\infty \}$. 

\bigskip
Then for example if a set $S$ is not bounded above, then we can write
\begin{equation*}
\textrm{sup } S = \infty
\end{equation*}



% Section 13 Topology of the Reals

[Definition]{neighborhood \& radius}

Let $x \in \R$ and $\varepsilon > 0$, then a \mbox{\textbf{neighborhood}}
of $x$ is
\begin{equation*}
N(x;\varepsilon) = \{ y \in \R : |y-x|<\varepsilon \}
\end{equation*}
The number $\varepsilon$ is referred to as the \mbox{\textbf{radius}}
of $N(x;\varepsilon)$.



[Definition]{deleted neighborhood}

Let $x \in \R$ and $\varepsilon > 0$, then a
\mbox{\textbf{deleted neighborhood}} of $x$ is
\begin{equation*}
N^{*}(x;\varepsilon) = \{ y \in \R : 0<|y-x|<\varepsilon \}
\end{equation*}



[Definition]{interior point}

Let $S \subseteq \R$.  A point $x \in \R$ is an
\mbox{\textbf{interior point}} of $S$ if there exists a neigborhood
$N(x;\varepsilon)$ such that $N \subseteq S$.

\bigskip
The set of all interior points of $S$ is denoted int $S$.



[Definition]{boundary point}

A point $x \in \R$ is a \mbox{\textbf{boundary point}} of $S$ if
\begin{equation*}
\forall \ \varepsilon > 0, \quad N(x;\varepsilon) \cap S \neq \varnothing
\textrm{ and } N(x;\varepsilon) \cap (\R \setminus S) \neq \varnothing
\end{equation*}
In other words, every neighborhood of a boundary point must intersect the
set $S$ and the complement of $S$ in $\R$.

\medskip
The set of all boundary points of $S$ is denoted bd $S$.



[Definition]{closed and open sets}

Let $S \subseteq \R$.  If bd $S \subseteq S$, then $S$ is said to be
\mbox{\textbf{closed}}.

\bigskip
If bd $S \subseteq \R \setminus S$, then $S$ is said to be
\mbox{\textbf{open}}.



[Definition]{accumulation point}

Suppose $S \subseteq \R$, then a point $x \in \R$ is called an
\mbox{\textbf{accumulation point}} of $S$ if
\begin{equation*}
\forall \ \varepsilon >0, \quad N^{*}(x;\varepsilon) \cap S \neq \varnothing
\end{equation*}
In other words, every deleted neighborhood of $x$ contains a point in $S$.

\medskip
The set of all accumulation points of $S$ is denoted $S'$.



[Definition]{isolated point}

Let $S \subseteq \R$.  If $x \in S$ and $x \not\in S'$,
then $x$ is called an \mbox{\textbf{isolated point}} of $S$.



[Definition]{closure of a set}

Let $S \subseteq \R$.  The \mbox{\textbf{closure}} of $S$ is defined by
\begin{equation*}
\textrm{cl } S = S \cup S'
\end{equation*}
In other words, the closure of a set is the set itself unioned with its
set of accumulation points.



% Section 14 Compact Sets

[Definition]{open cover}

An \mbox{\textbf{open cover}} of a set $S$ is a family or collection of sets
whose union contains $S$.
\begin{equation*}
 S \subseteq \mathscr{F} = \{ F_{n} : n \in \N \}
\end{equation*}



[Definition]{subcover}

Suppose $\mathscr{G} \subseteq \mathscr{F}$ are both families of indexed sets
that cover a set $S$, then since $\mathscr{G}$ is a subset of $\mathscr{F}$
it is called a \mbox{\textbf{subcover}} of $S$.



[Definition]{compact set}

A set $S$ is \mbox{\textbf{compact}} iff \emph{every} open cover
of $S$ contains a finite subcover of $S$.

\bigskip
Note:  This is a difficult definition to use because to show that a
set is compact you must show that \emph{every} open cover contains
a finite subcover.



% Section 16 Convergence

[Definition]{sequence}

A \mbox{\textbf{sequence}} $s$ is a function whose domain is $\N$.
However, instead of denoting the value of $s$ at $n$ by $s(n)$,
we denote it $s_{n}$.  The ordered set of all values of $s$ is denoted
$(s_{n})$. 



[Definition]{converge \& diverge}

A sequence $(s_{n})$ is said to \mbox{\textbf{converge}} to $s \in \R$,
denoted $(s_{n}) \rightarrow s$ if
\begin{equation*}
\forall \ \varepsilon > 0, \ \exists \ N \textrm{ such that } \forall \ 
n \in \N,
\end{equation*}
\begin{equation*}
n>N \Rightarrow |s_{n} - s| < \varepsilon
\end{equation*}
If a sequence does not converge, it is said to \mbox{\textbf{diverge}}.



[Definition]{bounded sequence}

A sequence is said to be \mbox{\textbf{bounded}} if its range
\mbox{$\{ s_{n} : n \in \N \}$} is bounded.  Equivalently if,
\begin{equation*}
\exists \; M \geq 0 \textrm{ such that }
\forall \; n \in \N, \  |s_{n}| \leq M
\end{equation*}



% Section 17 Limit Theorems

[Definition]{diverge to $+\infty$}

A sequence $(s_{n})$ is said to diverge to $+\infty$ if
\begin{equation*}
\forall \; M \in \R, \ \exists \; N \textrm{ such that }
\end{equation*}
\begin{equation*}
n > N \Rightarrow s_{n} > M
\end{equation*}



[Definition]{diverge to $-\infty$}

A sequence $(s_{n})$ is said to diverge to $-\infty$ if
\begin{equation*}
\forall \; M \in \R, \ \exists \; N \textrm{ such that }
\end{equation*}
\begin{equation*}
n > N \Rightarrow s_{n} < M
\end{equation*}



[Definition]{nondecreasing, nonincreasing \& monotone}

A sequence $(s_{n})$ is \mbox{\textbf{nondecreasing}} if
\begin{equation*}
s_{n} \leq s_{n+1} \quad \forall n \in \N
\end{equation*}
A sequence $(s_{n})$ is \mbox{\textbf{nonincreasing}} if
\begin{equation*}
s_{n} \geq s_{n+1} \quad \forall n \in \N
\end{equation*}
A sequence is \mbox{\textbf{monotone}} if it is either nondecreasing
or nonincreasing.



[Definition]{increasing \& decreasing}

A sequence $(s_{n})$ is \mbox{\textbf{increasing}} if
\begin{equation*}
s_{n} < s_{n+1} \quad \forall n \in \N
\end{equation*}
A sequence $(s_{n})$ is \mbox{\textbf{decreasing}} if
\begin{equation*}
s_{n} > s_{n+1} \quad \forall n \in \N
\end{equation*}



[Definition]{Cauchy sequence}

A sequence $(s_{n})$ is said to be a \mbox{\textbf{Cauchy sequence}} if
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; N \st
\end{equation*}
\begin{equation*}
m,n > N \; \Rightarrow |s_{n} - s_{m}| < \varepsilon
\end{equation*}



% Section 19 Subsequences

[Definition]{subsequence}

If $(s_{n})$ is any sequence and $(n_{k})$ is any strictly increasing
sequence, then the sequence $(s_{n_{k}})$ is called a
\mbox{\textbf{subsequence}} of $(s_{n})$.



[Definition]{subsequential limit}

A \mbox{\textbf{subsequential limit}} of a sequence $(s_{n})$ is the
limit of some subsequence of $(s_{n})$.



[Definition]{lim sup \& lim inf}

Suppose $S$ is the set of all subsequential limits of a sequence
$(s_{n})$.  The \mbox{\textbf{lim sup $(s_{n})$}}, shorthand for the
limit superior of $(s_{n})$ is defined to be
\begin{equation*}
\textrm{lim sup } (s_{n}) = \textrm{sup } S
\end{equation*}
The \mbox{\textbf{lim inf $(s_{n})$}}, shorthand for the
limit inferior of $(s_{n})$ is defined to be
\begin{equation*}
\textrm{lim inf } (s_{n}) = \textrm{inf } S
\end{equation*}



[Definition]{oscillating sequence}

If lim inf $(s_{n}) <$ lim sup $(s_{n})$, then we say that the sequence
$(s_{n})$ \mbox{\textbf{oscillates}}.



% Section 20 Limits of Functions

[Definition]{limit of a function}

Suppose $f:D \rightarrow \R$ where $D \subseteq \R$, and suppose $c$ is 
an accumulation point of $D$.  Then the
\mbox{\textbf{limit of $f$ at $c$ is $L$}} is denoted by
\[ \lim_{x \rightarrow c} f(x) = L \]
and defined by
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; \delta > 0 \; \st
\end{equation*}
\begin{equation*}
|x-c| < \delta \Rightarrow |f(x) - L| < \varepsilon
\end{equation*}



[Definition]{sum, product, multiple, \& quotient\\
of functions}

Let $f:D \rightarrow \R$ and $g:D \rightarrow \R$, then we define:

  \textbf{sum} $(f+g)(x) = f(x) + g(x)$
  \textbf{product} $(fg)(x) = f(x)g(x)$
  \textbf{multiple} $(kf)(x) = kf(x) \quad k \in \R$
  \textbf{quotient} $\left( \dfrac{f}{g} \right) = \dfrac{f(x)}{g(x)}
\textrm{ if } g(x) \neq 0 \quad \forall x \in D$




[Definition]{right--hand limit}

Let $f:(a,b) \rightarrow \R$, then the \mbox{\textbf{right--hand limit}}
of $f$ at $a$ is denoted \[\lim_{x \rightarrow a^{+}} f(x) = L \]
and defined by
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; \delta > 0 \st
\end{equation*}
\begin{equation*}
a < x < a + \delta \Rightarrow |f(x) - L| < \varepsilon
\end{equation*}



[Definition]{left--hand limit}

Let $f:(a,b) \rightarrow \R$, then the \mbox{\textbf{left--hand limit}}
of $f$ at $b$ is denoted \[\lim_{x \rightarrow b^{-}} f(x) = L \]
and defined by
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; \delta > 0 \st
\end{equation*}
\begin{equation*}
b - \delta < x < b \Rightarrow |f(x) - L| < \varepsilon
\end{equation*}



% Section 21 Continuous Functions

[Definition]{continuous function at a point}

Let $f:D \rightarrow \R$ where $D \subseteq \R$, and suppose $c \in D$,
then $f$ is \mbox{\textbf{continuous}} at $c$ if
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; \delta > 0 \st
\end{equation*}
\begin{equation*}
|x-c| < \delta \Rightarrow |f(x) - f(c)| < \varepsilon
\end{equation*}



[Definition]{continuous on $S$\\ continuous}

Let $f:D \rightarrow \R$ where $D \subseteq \R$.  If $f$ is continuous
at each point of a subset $S \subseteq D$, then $f$ is said to be
\mbox{\textbf{continuous on $S$}}.

\medskip
If $f$ is continuous on its entire domain $D$, then $f$ is simply said
to be \mbox{\textbf{continuous}}.



% Section 22 Properties of Continuous Functions

[Definition]{bounded function}

A function is said to be \mbox{\textbf{bounded}} if its range is
bounded.  Equivalently, $f:D \rightarrow \R$ is bounded if
\begin{equation*}
\exists \; M \in \R \st \forall \; x \in D, \ |f(x)| \leq M
\end{equation*}



% Section 23 Uniform Continuity

[Definition]{uniform continuity}

A function $f:D \rightarrow \R$ is \textbf{uniformly continuous on $D$} if
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; \delta > 0 \st
\end{equation*}
\begin{equation*}
|x-y|<\delta \Rightarrow |f(x)-f(y)|< \varepsilon
\end{equation*}



[Definition]{extension of a function}

Suppose $f:(a,b)\rightarrow \R$, then the \mbox{\textbf{extension of $f$}}
is denoted $\tilde{f}:[a,b]\rightarrow \R$ and defined by
\begin{equation*}
\tilde{f}(x) = \left\{ \begin{array}{ll}
  u & x=a \\
  f(x) & a<x<b \\
  v & x=b
\end{array} \right.
\end{equation*}
\begin{equation*}
\textrm{where } \lim_{x\rightarrow a} f(x)=u \textrm{ and }
\lim_{x\rightarrow b} f(x)=v.
\end{equation*}



% Section 25 The Derivative

[Definition]{differentiable at a point}

Suppose $f:I\rightarrow \R$ where $I$ is an interval containing the point
$c$.  Then $f$ is \mbox{\textbf{differentiable at $c$}} if the limit
\begin{equation*}
\lim_{x\rightarrow c} \dfrac{f(x)-f(c)}{x-c}
\end{equation*}
exists and is finite.  Whenever this limit exists and is finite, we
denote the \mbox{\textbf{derivative of $f$ at $c$}} by
\begin{equation*}
f'(c) = \lim_{x\rightarrow c} \dfrac{f(x)-f(c)}{x-c}
\end{equation*}



% Section 26 The Mean Value Theorem

[Definition]{strictly increasing function \\
strictly decreasing function}

A function $f:D\rightarrow \R$ is said to be
\textbf{strictly increasing} if
\begin{equation*}
\forall \; x_1,x_2 \in D, \quad x_1 < x_2 \Rightarrow f(x_1) < f(x_2)
\end{equation*}
A function $f:D\rightarrow \R$ is said to be
\textbf{strictly decreasing} if
\begin{equation*}
\forall \; x_1,x_2 \in D, \quad x_1 < x_2 \Rightarrow f(x_1) > f(x_2)
\end{equation*}



% Section 27 L'Hospital's Rule

[Definition]{limit at $\infty$}

Suppose $f:(a,\infty)\rightarrow \R$, then the
\mbox{\textbf{limit at infinity}} of $f$ denoted 
\begin{equation*}
\lim_{x\rightarrow \infty} f(x) = L
\end{equation*}
iff 
\begin{equation*}
\forall \; \varepsilon >0, \quad \exists \; N>a \st
\end{equation*}
\begin{equation*}
x>N \Rightarrow |f(x) - L| < \varepsilon
\end{equation*}



[Definition]{tends to $\infty$}

Suppose $f:(a,\infty)\rightarrow \R$, then we say
\mbox{\textbf{$f$ tends to $\infty$}} as $x\rightarrow \infty$ and
denote it by 
\begin{equation*}
\lim_{x\rightarrow \infty} f(x) = \infty
\end{equation*}
iff 
\begin{equation*}
\forall \; M \in \R , \quad \exists \; N>a \st
\end{equation*}
\begin{equation*}
x>N \Rightarrow f(x) > M
\end{equation*}



% Section 28 Taylor's Theorem

[Definition]{Taylor polynomials for $f$ at $x_0$}

\begin{small}
\begin{align*}
p_0(x) &=f(x_0) \\
p_1(x) &=f(x_0) + f'(x_0)(x-x_0)\\
p_2(x) &=f(x_0) + f'(x_0)(x-x_0) + \dfrac{f''(x_0)}{2!}(x-x_0)^2\\
\vdots &\\
p_n(x) &=f(x_0) + f'(x_0)(x-x_0) + \cdots +
\dfrac{f^{(n)}(x_0)}{n!}(x-x_0)^n
\end{align*}
\end{small}



[Definition]{Taylor series}

If $f$ has derivatives of all orders in a neighborhood of $x_0$, then
the limit of the Taylor polynomials is an infinite series called the
\mbox{\textbf{Taylor series}} of $f$ at $x_0$.
\begin{equation*}
\begin{split}
f(x) &= \sum_{n=0}^{\infty} \dfrac{f^{(n)}(x_0)}{n!} (x-x_0)^n \\
     &= f(x_0) + f'(x_0)(x-x_0) + \dfrac{f''(x_0)}{2!}(x-x_0)^2 + \cdots
\end{split}
\end{equation*}



% Section 29 The Riemann Integral

[Definition]{partition of an interval \\
refinement of a partition}

A \textbf{partition} of an interval $[a,b]$ is a finite set of points
$P = \{x_0, x_1, x_2, \ldots , x_n \}$ such that
\begin{equation*}
a = x_0 < x_1 < \ldots < x_n = b
\end{equation*}
If $P$ and $P'$ are two partitions of $[a,b]$ where $P \subset P'$
then $P'$ is called a \mbox{\textbf{refinement}} of $P$.



[Definition]{upper sum}

Suppose $f$ is a bounded function on $[a,b]$ and $P=\{x_0,\ldots,x_n\}$
is a partition of $[a,b]$.  \\
For each $i \in \{1,\ldots,n\}$ let
\begin{equation*}
M_i(f) = \sup \{f(x): x \in [x_{i-1}, x_{i}] \}.
\end{equation*}
We define the \mbox{\textbf{upper sum}} of $f$ with respect to $P$ to be
\begin{equation*}
U(f,P) = \sum_{i=1}^{n} M_i \Delta x_{i}
\end{equation*}
where $\Delta x_{i} = x_{i} - x_{i-1}$.



[Definition]{lower sum}

Suppose $f$ is a bounded function on $[a,b]$ and $P=\{x_0,\ldots,x_n\}$
is a partition of $[a,b]$.  \\
For each $i \in \{1,\ldots,n\}$ let
\begin{equation*}
m_i(f) = \inf \{f(x): x \in [x_{i-1}, x_{i}] \}.
\end{equation*}
We define the \mbox{\textbf{lower sum}} of $f$ with respect to $P$ to be
\begin{equation*}
L(f,P) = \sum_{i=1}^{n} m_i \Delta x_{i}
\end{equation*}
where $\Delta x_{i} = x_{i} - x_{i-1}$.



[Definition]{upper integral\\ lower integral}

Suppose $f$ is a bounded function on $[a,b]$.  We define the
\mbox{\textbf{upper integral}} of $f$ on $[a,b]$ to be
\begin{equation*}
U(f) = \inf \{ U(f,P): P \textrm{ any partition of } [a,b] \}.
\end{equation*}
Similarly, we define the \mbox{\textbf{lower integral}} of $f$ on
$[a,b]$ to be
\begin{equation*}
L(f) = \sup \{ L(f,P): P \textrm{ any partition of } [a,b] \}.
\end{equation*}



[Definition]{Riemann integrable}

Let $f:[a,b] \rightarrow \R$ be a bounded function.  If $L(f)=U(f)$,
then we say $f$ is \mbox{\textbf{Riemann integrable}} or just 
\mbox{\textbf{integrable}}.  Furthermore,
\begin{equation*}
\int_a^b f = \int_a^b f(x) dx = L(f) = U(f)
\end{equation*}
is called the \mbox{\textbf{Riemann integral}} or just the
\mbox{\textbf{integral}} of $f$ on $[a,b]$.



% Section 30 Properties of the Riemann Integral

[Definition]{monotone function}

A function is said to be \mbox{\textbf{monotone}} if it is either
increasing or decreasing.

\medskip
A function is increasing if $x<y \Rightarrow f(x) \leq f(y)$. \\
A function is decreasing if $x<y \Rightarrow f(x) \geq f(y)$.



[Definition]{proper integral}

When a function $f$ is bounded and the interval over which it is
integrated is bounded, then if the integral exists it is called a
\mbox{\textbf{proper integral}}.



[Definition]{improper integral}

An \mbox{\textbf{improper integral}} is the limit of a definite
integral, as an endpoint of the interval of integration approaches
either a specified real number or $\infty$ or $-\infty$ or, in some
cases, as both endpoints approach limits.

\medskip
Let $f:(a,b] \rightarrow \R$ be integrable on
$[c,b] \ \forall \; c \in (a,b]$.
If $\lim_{c \rightarrow a^{+}} \int_c^b f$ exists then
\begin{equation*}
\int_a^b f = \lim_{c \rightarrow a^{+}} \int_c^b f
\end{equation*}



[Definition]{integral convergence \\
integral divergence}

Suppose $f:(a,b] \rightarrow \R$ is integrable on
$[c,b] \ \forall \; c \in (a,b]$, futhermore let
$L=\lim_{c \rightarrow a^{+}} \int_c^b f$.  If $L$ is finite, then
the improper integral $\int_a^b f$ is said to \mbox{\textbf{converge}}
to $L$.

\medskip
If $L=\infty$ or $L=-\infty$, then the improper integral is said to 
\mbox{\textbf{diverge}}.



[Definition]{infinite series\\ partial sum}

Let $(a_k)$ be a sequence of real numbers, then we can create a new
sequence of numbers $(s_n)$ where each $s_n$ in $(s_n)$ corresponds to
the sum of the first $n$ terms of $(a_k)$.  This new sequence of sums is
called an \mbox{\textbf{infinite series}} and is denoted by
$\displaystyle \sum_{n=0}^{\infty} a_n$.

\smallskip
The $n$-th \mbox{\textbf{partial sum}} of the series, denoted by $s_n$
is defined to be
\begin{equation*}
s_n = \sum_{k=0}^{n} a_k
\end{equation*}



[Definition]{convergent series\\ sum}

If $(s_n)$ converges to a real number say $s$, then we say that the
series $\displaystyle \sum_{n=0}^{\infty} a_n = s$ is
\mbox{\textbf{convergent}}.

\medskip
Furthermore, we call $s$ the \mbox{\textbf{sum}} of the series.



[Definition]{divergent series\\ diverge to $+\infty$}

If a series does not converge then it is \mbox{\textbf{divergent}}.

\medskip
If the $\displaystyle \lim_{n\rightarrow \infty} s_n = +\infty$ then
the series is said to \textbf{diverge to $+\infty$}.



[Definition]{harmonic series}

The \mbox{\textbf{harmonic series}} is given by
\begin{equation*}
\sum_{n=1}^{\infty} \dfrac{1}{n} =
1 + \dfrac{1}{2} + \dfrac{1}{3} + \dfrac{1}{4} + \cdots
\end{equation*}
The harmonic series diverges to $+\infty$.



[Definition]{geometric series}

The \mbox{\textbf{geometric series}} is given by
\begin{equation*}
\sum_{n=0}^{\infty} x^{n} = 1 + x + x^2 + x^3 + \cdots
\end{equation*}
The geometric series converges to $\dfrac{1}{1-x}$ for $|x|<1$, and
diverges otherwise.



[Definition]{converge absolutely\\
converge conditionally}

If $\sum |a_n|$ converges then the series $\sum a_n$ is said to
\mbox{\textbf{converge absolutely}}.

\bigskip
If $\sum a_n$ converges, but $\sum |a_n|$ diverges, then the series
$\sum a_n$ is said to \mbox{\textbf{converge conditionally}}.



[Definition]{power series}

Given a sequence $(a_n)$ of real numbers, then the series
\begin{equation*}
\sum_{n=0}^{\infty} a_n x^n = a_0 + a_1x + a_2x^2 + a_3x^3 + \cdots
\end{equation*}
is called a \mbox{\textbf{power series}}.  The number $a_n$ is called
the \mbox{\textbf{$n$th coefficient}} of the series.



[Definition]{radius of convergence}

The \mbox{\textbf{radius of convergence}} of a power series
$\sum a_n x^n$ is an extended real number $R$ such that (for a power
series centered at $x_0$)
\begin{equation*}
|x-x_0|<R \Rightarrow \sum a_n x^n \textrm{ converges.}
\end{equation*}

\medskip
Note that $R$ may be $0$, $+\infty$ or any number between.



[Definition]{interval of convergence}

The \mbox{\textbf{interval of convergence}} of a power series is the set
of all $x \in \R$ such that $\displaystyle \sum_{n=0}^{\infty} a_n x^n$
converges.

\medskip
By theorem we see that (for a power series centered at 0) this set will 
either be $\{0\}$, $\R$ or a bounded interval centered at 0.



[Definition]{converges pointwise}

Let $(f_n)$ be a sequence of functions defined on a subset $S$ of $\R$.
Then $(f_n)$ \mbox{\textbf{converges pointwise}} on $S$ if for each
$x \in S$ the sequence of numbers $(f_n(x))$ converges.  If $(f_n)$
converges pointwise on $S$, then we define $f:S \rightarrow \R$ by
\begin{equation*}
f(x) = \lim_{n\rightarrow \infty} f_n(x)
\end{equation*}
for each $x \in S$, and we say that $(f_n)$ converges to $f$ pointwise
on $S$.



[Definition]{converges uniformly}

Let $(f_n)$ be a sequence of functions defined on a subset $S$ of $\R$.
 Then $(f_n)$ \mbox{\textbf{converges uniformly}} on $S$ to a function
$f$ defined on $S$ if
\begin{equation*}
\forall \; \varepsilon > 0, \quad \exists \; N \st \forall \; x \in S
\end{equation*}
\begin{equation*}
n > N \Rightarrow |f_n(x) - f(x)| < \varepsilon
\end{equation*}



[Definition]{}





[Definition]{}





[Definition]{}





[Definition]{}





\end{document}




\section{Real Analysis I}

\usepackage{oldgerm}
\usepackage{amssymb}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{mathrsfs}
\usepackage[all]{xy}
\usepackage{datetime}

\newtheorem{lemma}{Lemma}
\newtheorem{corollary}{Corollary}
\newtheorem{theorem}{Theorem}
\newtheorem{axiom}{Axiom}

\newcommand{\bb}[1]{\mathbb{#1}}
\newcommand{\lra}{\longrightarrow}
\newcommand{\Lra}{\Longrightarrow}
\newcommand{\ra}{\rightarrow}
\newcommand{\surj}{\twoheadrightarrow}
\newcommand{\Z}{\bb{Z}}
\newcommand{\Q}{\bb{Q}}
\newcommand{\R}{\bb{R}}
\newcommand{\C}{\bb{C}}
\newcommand{\N}{\bb{N}}
\newcommand{\m}{\bb{m}}
\newcommand{\cl}{\mbox{cl }}
\newcommand{\interior}{\mbox{int }}



[Copyright \& License]{Copyright \copyright \,
2007 Erin Chamberlain \\Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 3.0
License.  For more information, see creativecommons.org.

\medskip
\begin{center}
File last updated on \today, \\
at \currenttime
\end{center}



[Theorem]{Theorem \ref{thm01}}

\begin{theorem}
\label{thm01}
Let $f$ be a continuous function.  If $\int _0 ^1 f(x) \, dx \not= 0$,
then there exists a point $x$ in the interval $[0,1]$ such that
$f(x) \not= 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm02}}

\begin{theorem}
\label{thm02}
Let $x$ be a real number.  If $x > 0$, then $\frac 1x > 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm03}}

\begin{theorem}
\label{thm03}
Let $x$ be a real number.  If $x > 0$, then $\frac 1x > 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm04}}

\begin{theorem}
\label{thm04}
Let $A$ be a set.  Then $\emptyset \subseteq A$.
\end{theorem}



[Theorem]{Theorem \ref{thm05}}

\begin{theorem}
\label{thm05}
Let $A$ and $B$ be subsets of a universal set $U$.  Then
$A \cap (U \smallsetminus B) = A \smallsetminus B$.
\end{theorem}



[Theorem]{Theorem \ref{thm06}}

\begin{theorem}
\label{thm06}
\begin{small}
Let $A, B$, and $C$ be subsets of a universal set $U$.  Then the
following statements are true.

  $A \cup (U \smallsetminus A) = U$.
  $A \cap (U \smallsetminus A) = \emptyset $.
  $U \smallsetminus (U \smallsetminus A) = A$.
  $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$.
  $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$.
  $A \smallsetminus (B \cup C) = (A \smallsetminus B) \cap
(A \smallsetminus C)$.
  $A \smallsetminus (B \cap C) = (A \smallsetminus B) \cup
(A \smallsetminus C)$.

\end{small}
\end{theorem}



[Theorem]{Theorem \ref{thm07}}

\begin{theorem}
\label{thm07}
If $A$ and $B$ are subsets of a set $U$ and $A^c$ and $B^c$ are their
complements in $U$, then

 $(A \cup B)^c = A^c \cap B^c$.
 $(A \cap B)^c = A^c \cup B^c$.

\end{theorem}



[Theorem]{Theorem \ref{thm08}}

\begin{theorem}
\label{thm08}
$(a,b) = (c,d)$ iff $a=c$ and $b=d$.
\end{theorem}



[Theorem]{Theorem \ref{thm09}}

\begin{theorem}
\label{thm09}
Let $R$ be an equivalence relation on a set $S$.  Then $\{ E_x : x \in S\}$ is a partition of $S$.  The relation ``belongs to the same piece as'' is the same as $R$.  Conversely, if $\cal{T}$ is a partition of $S$, let $R$ be defined by $xRy$ iff $x$ and $y$ are in the same piece of the partition.  Then $R$ is an equivalence relation and the corresponding partition into equivalence classes is the same as $\cal{T}$.
\end{theorem}



[Theorem]{Theorem \ref{thm10} (part 1)}

\begin{theorem}
\label{thm10}
\begin{small}
Suppose that $f: A \to B$.  Let $C, C_1$ and $C_2$ be subsets of $A$ and
let $D, D_1$ and $D_2$ be subsets of $B$.  Then the following hold:

 $C \subseteq f^{-1}[f(C)]$.
 $f[f^{-1}(D)] \subseteq D$.
 $f(C_1 \cap C_2 ) \subseteq f(C_1) \cap f(C_2)$.
 $f(C_1 \cup C_2) = f(C_1) \cup f(C_2)$.
 $f(C_1) \smallsetminus f(C_2) \subseteq f(C_1 \smallsetminus C_2)$
if $C_2 \subseteq C_1$.

\end{small}
\end{theorem}



[Theorem]{Theorem \ref{thm10} (part 2)}

\textbf{Theorem \ref{thm10}.}
\begin{small}
\textit{Suppose that $f: A \to B$.  Let $C, C_1$ and $C_2$ be subsets of $A$ and let $D, D_1$ and $D_2$ be subsets of $B$.  Then the following hold:

[6.] $f^{-1}(D_1 \cap D_2) = f^{-1}(D_1) \cap f^{-1}(D_2)$.
[7.] $f^{-1}(D_1 \cup D_2) = f^{-1}(D_1) \cup f^{-1}(D_2)$.
[8.] $f^{-1}(B \smallsetminus D) = A \smallsetminus f^{-1}(D)$.
[9.] $f^{-1}(D_1 \smallsetminus D_2) = f^{-1}(D_1) \smallsetminus f^{-1}(D_2)$ if $D_2 \subseteq D_1$.
}
\end{small}




[Theorem]{Theorem \ref{thm11}}

\begin{theorem}
\label{thm11}
Suppose that $f: A \to B$.  Let $C, C_1$ and $C_2$ be subsets of $A$ and
let $D$ be a subset of $B$.  Then the following hold:

 If $f$ is injective, then $f^{-1}[f(C)]=C$.
 If $f$ is surjective, then $f[f^{-1}(D)]=D$.
 If $f$ is injective, then $f(C_1 \cap C_2) = f(C_1) \cap f(C_2)$.

\end{theorem}



[Theorem]{Theorem \ref{thm12}}

\begin{theorem}
\label{thm12}
Let $f: A \to B$ and $g: B \to C$.  Then

 If $f$ and $g$ are surjective, then $g \circ f$ is surjective.
 If $f$ and $g$ are injective, then $g \circ f$ is injective.
 If $f$ and $g$ are bijective, then $g \circ f$ is bijective.

\end{theorem}



[Theorem]{Theorem \ref{thm13}}

\begin{theorem}
\label{thm13}
Let $f: A \to B$ be bijective.  Then

 $f^{-1}: B \to A$ is bijective.
 $f^{-1} \circ f = i_A$ and $f \circ f^{-1} = i_B$.

\end{theorem}



[Theorem]{Theorem \ref{thm14}}

\begin{theorem}
\label{thm14}
Let $f: A \to B$ and $g: B \to C$ be bijective.  The the composition
$g \circ f : A \to C$ is bijective and
$(g \circ f)^{-1} = f^{-1} \circ g^{-1}$.
\end{theorem}



[Theorem]{Theorem \ref{thm15}}

\begin{theorem}
\label{thm15}
Let $S$ be a countable set and let $T \subseteq S$.  Then $T$ is countable.
\end{theorem}




[Theorem]{Theorem \ref{thm16}}

\begin{theorem}
\label{thm16}
Let $S$ be a nonempty set.  The following three conditions are
equivalent:

 $S$ is countable.
 There exists an injection $f: S \to \N$.
 There exists a surjection $f: \N \to S$.

\end{theorem}



[Theorem]{Theorem \ref{thm17}}

\begin{theorem}
\label{thm17}
The set $\R$ of real numbers is uncountable.
\end{theorem}



[Theorem]{Theorem \ref{thm18}}

\begin{theorem}
\label{thm18}
Let $S, T$ and $U$ be sets.

 If $S \subseteq T$, then $|S| \leq |T|$.
 $|S| \leq |S|$.
 If $|S|\leq |T|$ and $|T| \leq |U|$, then $|S| \leq |U|$.
 If $m, n \in \N$ and $m \leq n$, then $|\{ 1, 2, \ldots , m \} |
\leq |\{ 1, 2, \ldots , n\} |$.
 If $S$ is finite, then $S < \aleph _0$. 

\end{theorem}



[Theorem]{Theorem \ref{thm19}}

\begin{theorem}
\label{thm19}
For any set $S$, we have $|S| < |\cal{P}(S)|$.
\end{theorem}




[Theorem]{Theorem \ref{thm20} \\ Principle of
Mathematical Induction}

\begin{theorem}
\label{thm20}
(Principle of Mathematical Induction)  Let $P(n)$ be a statement that is
either true or false for each $n \in \N$.  Then $P(n)$ is true for all
$n \in \N$ provided that

 $P(1)$ is true, and
 for each $k \in \N$, if $P(k)$ is true, then $P(k+1)$ is true.

\end{theorem}



[Theorem]{Theorem \ref{thm21}}

\begin{theorem}
\label{thm21}
$1 + 2 + 3 + \cdots + n = \frac 12 n(n+1)$ for every natural number $n$.
\end{theorem}



[Theorem]{Theorem \ref{thm22}}

\begin{theorem}
\label{thm22}
$7^n - 4^n$ is a multiple of 3 for all $n \in \N$.
\end{theorem}



[Theorem]{Theorem \ref{thm23} \\ The Binomial Formula}

\begin{theorem}
\label{thm23}
(The Binomial Formula)  If $x$ and $y$ are real numbers and $n \in \N$,
then $$(x+y)^n = \sum _{k=0}^n \binom{n}{k} x^{n-k}y^k.$$
\end{theorem}



[Theorem]{Theorem \ref{thm24}}

\begin{theorem}
\label{thm24}
Let $m \in \N$ and let $P(n)$ be a statement that is either true or
false for each $n \geq m$.  Then $P(n)$ is true for all $n \geq m$
provided that

 $P(m)$ is true, and
 for each $k \geq m$, if $P(k)$ is true, then $P(k+1)$ is true.

\end{theorem}



[Theorem]{Theorem \ref{thm25}}

\begin{theorem}
\label{thm25}
Let $x,y,$ and $z$ be real numbers.

 If $x+z = y + z$, then $x=y$.
 $x\cdot 0 = 0$.
 $(-1)\cdot x = -x$.
 $xy = 0$ iff $x=0$ or $y=0$.
 $x<y$ iff $-y < -x$.
 If $x<y$ and $z<0$, then $xz > yz$.

\end{theorem}



[Theorem]{Theorem \ref{thm26}}

\begin{theorem}
\label{thm26}
Let $x,y \in \R$ such that $x \leq y+\epsilon$ for every $\epsilon > 0$.
Then $x \leq y$.
\end{theorem}



[Theorem]{Theorem \ref{thm27}}

\begin{theorem}
\label{thm27}
Let $x, y \in \R$ and let $a \geq 0$.  Then

 $|x| \geq 0$.
 $|x| \leq a$ iff $-a \leq x \leq a$.
 $|xy| = |x|\cdot |y|$.
 $|x+y| \leq |x| + |y|$.  (The triangle inequality)

\end{theorem}



[Theorem]{Theorem \ref{thm28}}

\begin{theorem}
\label{thm28}
Let $m,n,p \in \Z$.  If $p$ is a prime number and $p$ divides the
product $mn$, then $p$ divides $m$ or $p$ divides $n$.
\end{theorem}



[Theorem]{Theorem \ref{thm29}}

\begin{theorem}
\label{thm29}
Let $p$ be a prime number.  Then $\sqrt{p}$ is not a rational number.
\end{theorem}



[Theorem]{Theorem \ref{thm30}}

\begin{theorem}
\label{thm30}
Every non-empty subset of $\R$ that is bounded below has a greatest
lower bound.
\end{theorem}



[Theorem]{Theorem \ref{thm31}}

\begin{theorem}
\label{thm31}
Let $A$ be a non-empty subset of $\R$ and $x$ an element of $\R$.  Then

 $\sup A \leq x$ iff $a \leq x$ for every $a \in A$.
 $x<\sup A$ iff $x<a$ for some $a \in A$.

\end{theorem}



[Theorem]{Theorem \ref{thm32}}

\begin{theorem}
\label{thm32}
Let $A$ and $B$ be non-empty subsets of $\R$.  Then

 $\inf A \leq \sup A$.
 $\sup (-A) = - \inf A$ and $\inf (-A) = - \sup A$.
 $\sup (A + B) = \sup (A) + \sup (B)$ and $\inf (A+B) = \inf (A) + \inf (B)$.
 $\sup (A - B) = \sup (A) - \inf (B)$.
 If $A \subseteq B$, then $\sup A \leq \sup B$ and $\inf B \leq \inf A$.

\end{theorem}



[Theorem]{Theorem \ref{thm33}}

\begin{theorem}
\label{thm33}
Suppose that $D$ is a nonempty set and that $f: D \to \R$ and $g : D \to \R$.  If for every $x,y \in D$, $f(x) \leq g(y)$, then $f(D)$ is bounded above and $g(D)$ is bounded below.  Furthermore, $\sup f(D) \leq \sup g(D)$.
\end{theorem}



[Theorem]{Theorem \ref{thm34}}

\begin{theorem}
\label{thm34}
Let $f$ and $g$ be functions defined on a set containing $A$ as a subset,
and let $c \in \R$ be a positive constant.  Then

 $\sup _A cf = c \sup _A f$ and $\inf _A cf = c \inf _A f$.
 $\sup _A (-f) = - \inf _A f$.
 $\sup _A (f+g) \leq \sup _A f + \sup _A g$ and \\
$\inf _A f + inf _A g \leq \inf _A (f+g)$.
 $\sup \{ f(x) - f(y) : x,y \in A \} \leq \sup _A f - \inf _A f$.

\end{theorem}



[Theorem]{Theorem \ref{thm35}}

\begin{theorem}
\label{thm35}
The real number system $\R$ is a complete ordered field.
\end{theorem}



[Theorem]{Theorem \ref{thm36}\\
Archimedean Property of $\R$}

\begin{theorem}
\label{thm36}
(Archimedean Property of $\R$) The set $\N$ of natural numbers is
unbounded above in $\R$.
\end{theorem}



[Theorem]{Theorem \ref{thm37}}

\begin{theorem}
\label{thm37}
Each of the following is equivalent to the Archimedean property.

 For each $z \in \R$, there exists $n\in \N$ such that $n>z$.
 For each $x>0$ and for each $y \in \R$, there exists $n \in \N$
such that $nx > y$.
 For each $x > 0$, there exists $n \in \N$ such that
$0 < \frac{1}{n} < x$.

\end{theorem}



[Theorem]{Theorem \ref{thm38}}

\begin{theorem}
\label{thm38}
Let $p$ be a prime number.  Then there exists a positive real number $x$
such that $x^2=p$.
\end{theorem}



[Theorem]{Theorem \ref{thm39}}

\begin{theorem}
\label{thm39}
(Density of $\Q$ in $\R$)  If $x$ and $y$ are real numbers with $x<y$,
then there exists a rational number $r$ such that $x<r<y$.
\end{theorem}



[Theorem]{Theorem \ref{thm40}}

\begin{theorem}
\label{thm40}
If $x$ and $y$ are real numbers with $x<y$, then there exists an
irrational number $w$ such that $x<w<y$.
\end{theorem}



[Theorem]{Theorem \ref{thm41}}

\begin{theorem}
\label{thm41} \quad \\

 A set $S$ is open iff $S = \interior S$.  Equivalently, $S$ is
open iff every point in $S$ is an interior point of $S$.
 A set $S$ is closed iff its complement $\R \smallsetminus S$ is
open.

\end{theorem}



[Theorem]{Theorem \ref{thm42}}

\begin{theorem}
\label{thm42} \quad \\

 The union of any collection of open sets is an open set.
 The intersection of any finite collection of open sets is an open
set.

\end{theorem}



[Corollary]{Corollary \ref{cor01}}

\begin{corollary}
\label{cor01} \quad \\

 The intersection of any collection of closed sets is closed.
 The union of any finite collection of closed sets is closed.

\end{corollary}



[Theorem]{Theorem \ref{thm43}}

\begin{theorem}
\label{thm43}
Let $S$ be a subset of $\R$.  Then

 $S$ is closed iff $S$ contains all of its accumulation points.
 $\cl S$ is a closed set.
 $S$ is closed iff $S = \cl S$.

\end{theorem}



[Lemma]{Lemma \ref{lem01}}

\begin{lemma}
\label{lem01}
If $S$ is a nonempty closed bounded subset of $\R$, then $S$ has a
maximum and a minimum.
\end{lemma}



[Theorem]{Theorem \ref{thm44} \\ Heine--Borel Theorem}

\begin{theorem}
\label{thm44}
(Heine--Borel)  A subset $S$ of $\R$ is compact iff $S$ is closed and
bounded.
\end{theorem}



[Theorem]{Theorem \ref{thm45} \\ Bolzano--Weierstrass
Theorem}

\begin{theorem}
\label{thm45}
(Bolzano--Weierstrass)  If a bounded subset $S$ of $\R$ contains
infinitely many points, then there exists at least one point in $\R$
that is an accumulation point of $S$.
\end{theorem}



[Theorem]{Theorem \ref{thm46}}

\begin{theorem}
\label{thm46}
Let $\mathscr{F} = \{ K_{\alpha} : \alpha \in \mathscr{A} \}$ be a family
of compact subsets of $\R$.  Suppose that the intersection of any finite
subfamily of $\mathscr{F}$ is nonempty.  Then
\mbox{$\bigcap \{ K_{\alpha} : \alpha \in \mathscr{A} \} \neq \varnothing$}.
\end{theorem}



[Corollary]{Corollary \ref{cor02}\\
Nested Intervals Theorem}

\begin{corollary}
\label{cor02}
(Nested Intervals Theorem)  Let $\mathscr{F} = \{ A_{n} : n \in \N \} $
be a family of closed bounded intervals in $\R$ such that $A_{n+1}
\subseteq A_n$ for all $n \in \N$.  Then $\bigcap _{n=1}^{\infty} A_n
\neq \varnothing $.
\end{corollary}



[Theorem]{Theorem \ref{thm47}}

\begin{theorem}
\label{thm47}
Let $(s_n)$ and $(a_n)$ be sequences of real numbers and let $s \in \R$.
If for some $k > 0$ and some $m \in \N$, we have
$$|s_n - s| \leq k|a_n|, \mbox{ for all } n > m,$$
and if $\lim a_n = 0$, then it follows that $\lim s_n = s$.
\end{theorem}



[Theorem]{Theorem \ref{thm48}}

\begin{theorem}
\label{thm48}
Every convergent sequence is bounded.
\end{theorem}



[Theorem]{Theorem \ref{thm49}}

\begin{theorem}
\label{thm49}
If a sequence converges, its limit is unique.
\end{theorem}



[Theorem]{Theorem \ref{thm50}}

\begin{theorem}
\label{thm50}
A sequence $(s_n)$ converges to $s$ iff for each $\epsilon > 0$, there
are only finitely many $n$ for which $|s_n - s| \geq \epsilon$.
\end{theorem}



[Theorem]{Theorem \ref{thm51}}

\begin{theorem}
\label{thm51}
Let $(s_n)$ be a sequence of real numbers such that $\lim s_n = 0$, and
let $(t_n)$ be a bounded sequence.  Then $\lim s_nt_n = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm52} \\ The Squeeze Principle}

\begin{theorem}
\label{thm52}
(The Squeeze Principle)  If $(a_n)$, $(b_n)$, and $(c_n)$ are sequences
for which there is a number $K$ such that $b_n \leq a_n \leq c_n
\mbox{ for all } n > K$, and if $b_n \to a$ and $c_n \to a$, then
$a_n \to a$.
\end{theorem}



[Theorem]{Theorem \ref{thm53}}

\begin{theorem}
\label{thm53}
Suppose that $(s_n)$ and $(t_n)$ are convergent sequences with
$\lim s_n = s$ and $\lim t_n = t$.  Then

 $\lim (s_n + t_n) = s+t$.
 $\lim (ks_n) = ks$ and $\lim (k+s_n) = k+s$ for any $k\in \R$.
 $\lim (s_nt_n) = st.$
 $\lim \left( \frac {s_n}{t_n} \right) = \frac st$, provided that
$t_n \not= 0$ for all $n$ and $t\not= 0$.

\end{theorem}



[Theorem]{Theorem \ref{thm54}}

\begin{theorem}
\label{thm54}
Suppose that $(s_n)$ and $(t_n)$ are convergent sequences with
$\lim s_n = s$ and $\lim t_n = t$.  If $s_n \leq t_n$ for all $n \in
\N$, then $s \leq t$.
\end{theorem}



[Corollary]{Corollary \ref{cor03}}

\begin{corollary}
\label{cor03}
If $(t_n)$ converges to $t$ and $t_n \geq 0$ for all $n \in \N$, then
$t \geq 0$.
\end{corollary}



[Theorem]{Theorem \ref{thm55}\\
Ratio Test}

\begin{theorem}
\label{thm55}
(Ratio Test)  Suppose that $(s_n)$ is a sequence of positive terms and
that the limit $L = \lim \left( \frac{s_{n+1}}{s_n} \right)$ exists.
If $L < 1$, then $\lim s_n = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm56}}

\begin{theorem}
\label{thm56}
Suppose that $(s_n)$ and $(t_n)$ are sequences such that $s_n \leq t_n$
for all $n \in \N$.  

 If $\lim s_n = + \infty$, then $\lim t_n = + \infty$.
 If $\lim t_n = - \infty$, then $\lim s_n = - \infty$.

\end{theorem}



[Theorem]{Theorem \ref{thm57}}

\begin{theorem}
\label{thm57}
Let $(s_n)$ be a sequence of positive numbers.  Then $\lim s_n = + \infty$
iff $\lim \left( \frac{1}{s_n} \right) = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm58} \\ Monotone Convergence
Theorem}

\begin{theorem}
\label{thm58}
(Monotone Convergence Theorem)  A monotone sequence is convergent iff it
is bounded.
\end{theorem}



[Theorem]{Theorem \ref{thm59}}

\begin{theorem}
\label{thm59} \quad \\

 If $(s_n)$ is an unbounded increasing sequence, then $\lim s_n = + \infty$.
 If $(s_n)$ is an unbounded decreasing sequence, then $\lim s_n = - \infty$.

\end{theorem}



[Lemma]{Lemma \ref{lem02}}

\begin{lemma}
\label{lem02}
Every convergent sequence is a Cauchy sequence.
\end{lemma}



[Lemma]{Lemma \ref{lem03}}

\begin{lemma}
\label{lem03}
Every Cauchy sequence is bounded.
\end{lemma}



[Theorem]{Theorem \ref{thm60} \\ Cauchy Convergence
Criterion}

\begin{theorem}
\label{thm60}
(Cauchy Convergence Criterion)  A sequence of real numbers is convergent
iff it is a Cauchy sequence.
\end{theorem}



[Theorem]{Theorem \ref{thm61}}

\begin{theorem}
\label{thm61}
If a sequence $(s_n)$ converges to a real number $s$, then every
subsequence of $(s_n)$ also converges to $s$.
\end{theorem}



[Theorem]{Theorem \ref{thm62} \\ Bolzano--Weierstrass
Theorem For Sequences}

\begin{theorem}
\label{thm62}
(Bolzano--Weierstrass Theorem For Sequences)  Every bounded sequence has
a convergent subsequence.
\end{theorem}



[Theorem]{Theorem \ref{thm63}}

\begin{theorem}
\label{thm63}
Every unbounded sequence contains a monotone subsequence that has either
$+ \infty$ or $- \infty$ as a limit.
\end{theorem}



[Theorem]{Theorem \ref{thm64}}

\begin{theorem}
\label{thm64}
Let $(s_n)$ be a sequence and suppose that $m = \lim s_n$ is a real
number.  Then the following properties hold:

 For every $\epsilon > 0$ there exists $N$ such that $n> N$ implies
that $s_n < m+\epsilon$.
 For every $\epsilon >0$ and for every $i \in \N$, there exists an
integer $k > i$ such that $s_k > m - \epsilon$.

\end{theorem}



[Theorem]{Theorem \ref{thm65}}

\begin{theorem}
\label{thm65}
Let $f: D \to \R$ and let $c$ be an accumulation point of $D$.  Then
$\lim _{x \to c} f(x) = L$ iff for each neighborhood $V$ of $L$ there
exists a deleted neighborhood $U$ of $c$ such that $f(U \cap D)
\subseteq V$.
\end{theorem}



[Theorem]{Theorem \ref{thm66}}

\begin{theorem}
\label{thm66}
Let $f: D \to \R$ and let $c$ be an accumulation point of $D$.  Then
$\lim _{x \to c} f(x) = L$ iff for every sequence $(s_n)$ in $D$ that
converges to $c$ with $s_n \not= c$ for all $n$, the sequence $(f(s_n))$
converges to $L$.
\end{theorem}



[Corollary]{Corollary \ref{cor04}}

\begin{corollary}
\label{cor04}
If $f: D \to \R$ and if $c$ is an accumulation point of $D$, then $f$
can have only one limit at $c$.
\end{corollary}



[Theorem]{Theorem \ref{thm67}}

\begin{theorem}
\label{thm67}
Let $f: D \to \R$ and let $c$ be an accumulation point of $D$.  Then the
following are equivalent:

[(a)]  $f$ does not have a limit at $c$.
[(b)]  There exists a sequence $(s_n)$ in $D$ with each
$s_n \not= c$ such that $(s_n)$ converges to $c$, but $(f(s_n))$ is not
convergent in $\R$.

\end{theorem}



[Theorem]{Theorem \ref{thm68}}

\begin{theorem}
\label{thm68}
Let $f: D \to \R$ and $g: D \to \R$, and let $c$ be an accumulation
point of $D$.  If $\lim _{x \to c} f(x) = L$, $\lim _{x \to c} g(x) = M$,
and $k \in \R$, then $\lim _{x \to c} (f+g)(x) = L + M, \lim _{x \to c}
(fg)(x) = LM$, and $\lim _{x \to c} (kf)(x) = kL$.
\end{theorem}



[Theorem]{Theorem \ref{thm69}}

\begin{small}
\begin{theorem}
\label{thm69}
Let $f : D \to \R$ and let $c \in D$.  Then the following three
conditions are equivalent:

[(a)]  $f$ is continuous at $c$.
[(b)]  If $(x_n)$ is any sequence in $D$ such that $(x_n)$
converges to $c$, then $\lim f(x_n) = f(c)$.
[(c)]  For every neighborhood $V$ of $f(c)$ there exists a
neighborhood $U$ of $c$ such that $f(U \cap D) \subseteq V$.

Furthermore, if $c$ is an accumulation point of $D$, then the above are
all equivalent to

 [(d)]  $f$ has a limit at $c$ and $\lim _{x \to c} f(x) = f(c)$.

\end{theorem}
\end{small}



[Theorem]{Theorem \ref{thm70}}

\begin{theorem}
\label{thm70}
Let $f:D \to \R$ and let $c \in D$.  Then $f$ is discontinuous at $c$
iff there exists a sequence $(x_n)$ in $D$ such that $(x_n)$ converges
to $c$ but the sequence $(f(x_n))$ does not converge to $f(c)$.
\end{theorem}



[Theorem]{Theorem \ref{thm71}}

\begin{theorem}
\label{thm71}
Let $f$ and $g$ be functions from $D$ to $\R$, and let $c \in D$.
Suppose that $f$ and $g$ are continuous at $c$.  Then

[(a)]  $f+g$ and $fg$ are continuous at $c$,
[(b)]  $f/g$ is continuous at $c$ if $g(c) \not= 0$.

\end{theorem}



[Theorem]{Theorem \ref{thm72}}

\begin{theorem}
\label{thm72}
Let $f: D \to \R$ and $g: E \to \R$ be functions such that $f(D)
\subseteq E$.  If $f$ is continuous at a point $c \in D$ and $g$ is
continuous at $f(c)$, then the composition $g \circ f : D \to \R$ is
continuous at $c$.
\end{theorem}



[Theorem]{Theorem \ref{thm73}}

\begin{theorem}
\label{thm73}
Let $D$ be a compact subset of $\R$ and suppose that $f: D \to \R$ is
continuous.  Then $f(D)$ is compact.
\end{theorem}



[Corollary]{Corollary \ref{cor05}}

\begin{corollary}
\label{cor05}
Let $D$ be a compact subset of $\R$ and suppose that $f : D \to \R$ is
continuous.  Then $f$ assumes minimum and maximum values on $D$.  That
is, there exist points $x_1$ and $x_2$ in $D$ such that $f(x_1) \leq f(x)
\leq f(x_2)$ for all $x \in D$.
\end{corollary}



[Lemma]{Lemma \ref{lem04}}

\begin{lemma}
\label{lem04}
Let $f: [a,b] \to \R$ be continuous and suppose that $f(a) < 0 < f(b)$.
Then there exists a point $c$ in $(a,b)$ such that $f(x) = 0$.
\end{lemma}



[Theorem]{Theorem \ref{thm74} \\ Intermediate Value
Theorem}

\begin{theorem}
\label{thm74}
(Intermediate Value Theorem)  Suppose that $f:[a,b] \to \R$ is
continuous.  Then $f$ has the intermediate value property on $[a,b]$.
That is, if $k$ is any value between $f(a)$ and $f(b)$
[i.e. $f(a) < k < f(b)$ or $f(b) < k < f(a)$], then there exists
$c \in [a,b]$ such that $f(c) = k$.
\end{theorem}



[Theorem]{Theorem \ref{thm75}}

\begin{theorem}
\label{thm75}
Let $I$ be a compact interval and suppose that $f: I \to \R$ is a
continuous function.  Then the set $f(I)$ is a compact interval.
\end{theorem}



[Theorem]{Theorem \ref{thm76}}

\begin{theorem}
\label{thm76}
Suppose that $f: D \to \R$ is continuous on a compact set $D$.  Then
$f$ is uniformly continuous on $D$.
\end{theorem}



[Theorem]{Theorem \ref{thm77}}

\begin{theorem}
\label{thm77}
Let $f: D \to \R$ be uniformly continuous on $D$ and suppose that
$(x_n)$ is a Cauchy sequence in $D$.  Then $(f(x_n))$ is a Cauchy
sequence.
\end{theorem}



[Theorem]{Theorem \ref{thm78}}

\begin{theorem}
\label{thm78}
A function $f: (a,b) \to \R$ is uniformly continuous on $(a,b)$ iff it
can be extended to a function $\tilde{f}$ that is continuous on $[a,b]$.
\end{theorem}



[Theorem]{Theorem \ref{thm79}}

\begin{theorem}
\label{thm79}
Let $I$ be an interval containing the point $c$ and suppose that $f: I \to \R$.  Then $f$ is differentiable at $c$ iff, for every sequence $(x_n)$ in $I \smallsetminus \{ c\}$ that converges to $c$, the sequence
$$\displaystyle \left( \frac{f(x_n) - f(c)}{x_n-c} \right)$$
converges.  Furthermore, if $f$ is differentiable at $c$, then the sequence of quotients above will converge to $f'(c)$.
\end{theorem}



[Theorem]{Theorem \ref{thm80}}

\begin{theorem}
\label{thm80}
If $f: I \to \R$ is differentiable at a point $c \in I$, then $f$ is
continuous at $c$.
\end{theorem}



[Theorem]{Theorem \ref{thm81} (part 1)}

\begin{theorem}
\label{thm81}
Suppose that $f: I \to \R$ and $g: I \to \R$ are differentiable at $c \in I$.  Then
 
[(a)]  If $k \in \R$, then the function $kf$ is differentiable at $c$ and $(kf)'(c) = k\cdot f'(c)$.
[(b)]  The function $f+g$ is differentiable at $c$ and $(f+g)'(c) = f'(c) + g'(c)$.

\end{theorem}



[Theorem]{Theorem \ref{thm81} (part 2)}

\textbf{Theorem \ref{thm81}.}
\textit{
Suppose that $f: I \to \R$ and $g: I \to \R$ are differentiable at $c \in I$.  Then
 
[(c)]  (Product Rule)  The function $fg$ is differentiable at $c$ and $(fg)'(c) = f(c)g'(c) + f'(c)g(c)$.
[(d)]  (Quotient Rule)  If $g(c) \not=0$, then the function $f/g$ is differentiable at $c$ and 
$$\displaystyle \left( \frac fg \right) '(c) = \frac{ g(c)f'(c) - f(c)g'(c)}{[g(c)]^2}.$$

}



[Theorem]{Theorem \ref{thm82}\\ Chain Rule}

\begin{theorem}
\label{thm82}
(Chain Rule)  Let $I$ and $J$ be intervals in $\R$, let $f:I \to \R$ and
$g: J \to \R$, where $f(I) \subseteq J$, and let $c \in I$.  If $f$ is
differentiable at $c$ and $g$ is differentiable at $f(c)$, then the
composite function $g \circ f$ is differentiable at $c$ and
$(g\circ f)'(c) = g'(f(c))\cdot f'(c)$.
\end{theorem}



[Theorem]{Theorem \ref{thm83}}

\begin{theorem}
\label{thm83}
If $f$ is differentiable on an open interval $(a,b)$ and if $f$ assumes
its maximum or minimum at a point $c \in (a,b)$, then $f'(c) = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm84}\\ Rolle's Theorem}

\begin{theorem}
\label{thm84}
(Rolle's Theorem)  Let $f$ be a continuous function on $[a,b]$ that is
differentiable on $(a,b)$ and such that $f(a) = f(b) = 0$.  Then there
exists at least one point $c \in (a,b)$ such that $f'(c) = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm85}\\ Mean Value Theorem}

\begin{theorem}
\label{thm85}
(Mean Value Theorem)  Let $f$ be a continuous function on $[a,b]$ that
is differentiable on $(a,b)$.  Then there exists at least one point $c
\in (a,b)$ such that $f'(c) = \frac{f(b) - f(a)}{b-a}$.
\end{theorem}



[Theorem]{Theorem \ref{thm86}}

\begin{theorem}
\label{thm86}
Let $f$ be continuous on $[a,b]$ and differentiable on $(a,b)$.  If
$f'(x) = 0$ for all $x \in (a,b)$, then $f$ is constant on $[a,b]$.
\end{theorem}



[Corollary]{Corollary \ref{cor06}}

\begin{corollary}
\label{cor06}
Let $f$ and $g$ be continuous on $[a,b]$ and differentiable on $(a,b)$.
Suppose that $f'(x) = g'(x)$ for all $x \in (a,b)$.  Then there exists a
constant $C$ such that $f=g+C$ on $[a,b]$.
\end{corollary}



[Theorem]{Theorem \ref{thm87}}

\begin{theorem}
\label{thm87}
Let $f$ be differentiable on an interval $I$.  Then	

[(a)]  if $f'(x) > 0$ for all $x \in I$, then $f$ is
strictly increasing on $i$, and 
[(b)]  if $f'(x) < 0$ for all $x \in I$, then $f$ is
strictly decreasing on $I$.

\end{theorem}



[Theorem]{Theorem \ref{thm88}\\
Intermediate Value Theorem for Derivatives}

\begin{theorem}
\label{thm88}
(Intermediate Value Theorem for Derivatives)  Let $f$ be differentiable
on $[a,b]$ and suppose that $k$ is a number between $f'(a)$ and $f'(b)$.
Then there exists a point $c \in (a,b)$ such that $f'(c) = k$.
\end{theorem}



[Theorem]{Theorem \ref{thm89}\\ 
Inverse Function Theorem}

\begin{theorem}
\label{thm89}
(Inverse Function Theorem)  Suppose that $f$ is differentiable on an
interval $I$ and $f'(x) \not= 0$ for all $x \in I$.  Then $f$ is
injective, $f^{-1}$ is differentiable on $f(I)$, and $(f^{-1})'(y) =
\frac{1}{f'(x)}$, where $y = f(x)$.
\end{theorem}



[Theorem]{Theorem \ref{thm90}\\
Cauchy Mean Value Theorem}

\begin{theorem}
\label{thm90}
(Cauchy Mean Value Theorem)  Let $f$ and $g$ be functions that are
continuous on $[a,b]$ and differentiable on $(a,b)$.  Then there exists
at least one point $c \in (a,b)$ such that
\begin{equation*}
[f(b) - f(a)]g'(c) = [g(b) - g(a)]f'(c)
\end{equation*}
\end{theorem}



[Theorem]{Theorem \ref{thm91}\\ L'Hospital's Rule}

\begin{theorem}
\label{thm91}
(L'Hospital's Rule)  Let $f$ and $g$ be continuous on $[a,b]$ and
differentiable on $(a,b)$.  Suppose that $c \in [a,b]$ and
$f(c) = g(c)=0$.  Suppose also that $g'(x) \not= 0$ for $x \in U$, where
$U$ is the intersection of $(a,b)$ and some deleted neighborhood of $c$.
If $\displaystyle \lim _{x \to c} \frac{f'(x)}{g'(x)} = L$, with $L \in
\R$, then $\displaystyle \lim _{x \to c} \frac{f(x)}{g(x)} = L$.
\end{theorem}



[Theorem]{Theorem \ref{thm92}\\ L'Hospital's Rule}

\begin{theorem}
\label{thm92}
(L'Hospital's Rule)  Let $f$ and $g$ be differentiable on $(b, \infty)$.
Suppose that $\lim _{ x \to \infty} f(x) = \lim _{x \to \infty} g(x) =
\infty$, and that $g'(x) \not= 0$ for $x \in (b, \infty)$.  If
$\displaystyle \lim _{x \to \infty} \frac{f'(x)}{g'(x)} = L$, where
$L \in \R$, then $\displaystyle \lim _{x \to \infty} \frac{f(x)}{g(x)} = L$.
\end{theorem}



[Theorem]{Theorem \ref{thm93}\\ Taylor's Theorem}

\begin{theorem}
\label{thm93}
(Taylor's Theorem)  Let $f$ and its first $n$ derivatives be continuous
on $[a,b]$ and differentiable on $(a,b)$, and let $x_0 \in [a,b]$.  Then
for each $x \in [a,b]$ with $x \not= x_0$ there exists a point $c$
between $x$ and $x_0$ such that
$$f(x) = f(x_0) + f'(x_0)(x-x_0) + \frac{f''(x_0)}{2!}(x-x_0)^2 + \cdots $$
$$+ \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n + \frac{f^{(n+1)}(c)}{(n+1)!}(x-x_0)^{n+1}.$$
\end{theorem}



[Theorem]{Theorem \ref{thm94}}

\begin{theorem}
\label{thm94}
Let $f$ be a bounded function on $[a,b]$.  If $P$ and $Q$ are partitions
of $[a,b]$ and $Q$ is a refinement of $P$, then $L(f,P) \leq L(f,Q) 
\leq U(f,Q) \leq U(f,P)$.
\end{theorem}



[Theorem]{Theorem \ref{thm95}}

\begin{theorem}
\label{thm95}
Let $f$ be a bounded function on $[a,b]$.  Then $L(f) \leq U(f)$.
\end{theorem}



[Theorem]{Theorem \ref{thm96}}

\begin{theorem}
\label{thm96}
Let $f$ be a bounded function on $[a,b]$.  Then $f$ is integrable iff
for each $\epsilon > 0$ there exists a partition $P$ of $[a,b]$
such that $U(f,P) - L(f,P) < \epsilon$.
\end{theorem}



[Theorem]{Theorem \ref{thm97}}

\begin{theorem}
\label{thm97}
Let $f$ be a monotonic function on $[a,b]$.  Then $f$ is integrable.
\end{theorem}



[Theorem]{Theorem \ref{thm98}}

\begin{theorem}
\label{thm98}
Let $f$ be a continuous function on $[a,b]$.  Then $f$ is integrable
on $[a,b]$.
\end{theorem}



[Theorem]{Theorem \ref{thm99}}

\begin{theorem}
\label{thm99}
Let $f$ and $g$ be integrable functions on $[a,b]$ and let $k \in \R$. 
 Then

[(a)]  $kf$ is integrable and $\int _a ^b {kf} = k\int{f}$, and 
[(b)]  $f+g$ is integrable and $\int _a ^b {(f+g)} =
\int _a ^b {f} + \int _a ^b {g}$.

\end{theorem}



[Theorem]{Theorem \ref{thm100}}

\begin{theorem}
\label{thm100}
Suppose that $f$ is integrable on both $[a,c]$ and $[c,b]$.  Then $f$ is
integrable on $[a,b]$.  Furthermore, $\int _a ^b {f} =
\int _a ^c {f} + \int _c ^b {f}$.
\end{theorem}



[Theorem]{Theorem \ref{thm101}}

\begin{theorem}
\label{thm101}
Suppose that $f$ is integrable on $[a,b]$ and $g$ is continuous on
$[c,d]$, where $f([a,b]) \subseteq [c,d]$.  Then $g \circ f$ is
integrable on $[a,b]$.
\end{theorem}



[Corollary]{Corollary \ref{cor07}}

\begin{corollary}
\label{cor07}
Let $f$ be integrable on $[a,b]$.  The $|f|$ is integrable on $[a,b]$
and $\displaystyle \Big| \int _a ^b {f} \Big| \leq \int _a ^b {|f|}.$
\end{corollary}



[Theorem]{Theorem \ref{thm102}\\
The Fundamental Theorem of Calculus I}

\begin{theorem}
\label{thm102}
(The Fundamental Theorem of Calculus I)  Let $f$ be integrable on
$[a,b]$.  For each $x \in [a,b]$ let $\displaystyle F(x) =
\int _a ^x {f(t)}\, dt.$  Then $F$ is uniformly continuous on $[a,b]$. 
 Furthermore, if $f$ is continuous at $c \in [a,b]$, then $F$ is
differentiable at $c$ and $F'(c) = f(c)$.
\end{theorem}



[Theorem]{Theorem \ref{thm103}\\
The Fundamental Theorem of Calculus II}

\begin{theorem}
\label{thm103}
(The Fundamental Theorem of Calculus II)  If $f$ is differentiable on
$[a,b]$ and $f'$ is integrable on $[a,b]$, then
$\displaystyle \int _a ^b {f'} = f(b) - f(a)$.
\end{theorem}



[Theorem]{Theorem \ref{thm104}}

\begin{theorem}
\label{thm104}
Suppose that $\displaystyle \sum a_n = s$ and $\displaystyle
\sum b_n = t$.  Then $\displaystyle \sum (a_n + b_n) = s + t$ and
$\displaystyle \sum (ka_n) = ks$, for every $k \in \R$.
\end{theorem}



[Theorem]{Theorem \ref{thm105}}

\begin{theorem}
\label{thm105}
If $\displaystyle \sum a_n$ is a convergent series, then $\lim
a_n = 0$.
\end{theorem}



[Theorem]{Theorem \ref{thm106}\\
Cauchy Criterion for Series}

\begin{theorem}
\label{thm106}
(Cauchy Criterion for Series)  The infinite series
$\displaystyle \sum a_n$ converges iff for each $\epsilon > 0$ there
exists a number $N$ such that if $n \geq m > N$, then $|a_m + a_{m+1} +
\cdots + a_n|< \epsilon$.
\end{theorem}



[Theorem]{Theorem \ref{thm107}\\ Comparison Test}

\begin{theorem}
\label{thm107}
(Comparison Test)  Let $\displaystyle \sum a_n$ and
$\displaystyle \sum b_n$ be infinite series of nonnegative terms.  That
is, $a_n \geq 0$ and $b_n \geq 0$ for all $n$.  Then

 If $\displaystyle \sum a_n$ converges and $0 \leq b_n \leq a_n$
for all $n$, then $\displaystyle \sum b_n$ converges.
  If $\displaystyle \sum a_n = + \infty$ and $0 \leq a_n \leq b_n$
for all $n$, then $\displaystyle \sum b_n = + \infty$.

\end{theorem}



[Theorem]{Theorem \ref{thm108}}

\begin{theorem}
\label{thm108}
If a series converges absolutely, then it converges.
\end{theorem}



[Theorem]{Theorem \ref{thm109}\\ Ratio Test}

\begin{theorem}
\label{thm109}
\begin{small}
(Ratio Test)  Let $\displaystyle \sum a_n$ be a series of
nonzero terms.

  If $\displaystyle \limsup \Big| \frac{a_{n+1}}{a_n} \Big| < 1$,
then the series converges absolutely.
  If $\displaystyle \liminf \Big| \frac{a_{n+1}}{a_n} \Big| > 1$,
the the series diverges.
  Otherwise, $\displaystyle \liminf \Big| \frac{a_{n+1}}{a_n} \Big|
\leq 1 \leq \limsup \Big| \frac{a_{n+1}}{a_n} \Big|$ and the test gives
no information about convergence or divergence.

\end{small}
\end{theorem}



[Theorem]{Theorem \ref{thm110}\\ Root Test}

\begin{theorem}
\label{thm110}
(Root Test)  Given a series $\displaystyle \sum a_n$, let
$\alpha = \limsup |a_n|^{\frac 1n}$.

  If $\alpha < 1$, then the series converges absolutely.
  If $\alpha > 1$, then the series diverges.
  Otherwise, $\alpha = 1$ and the test gives no information about
convergence or divergence.

\end{theorem}



[Theorem]{Theorem \ref{thm111}\\
Integral Test}

\begin{theorem}
\label{thm111}
(Integral Test)  Let $f$ be a continuous function defined on
$[0, \infty)$, and suppose that $f$ is positive and decreasing.  That is,
if $x_1 < x_2$, then $f(x_1) \geq f(x_2) > 0$.  Then the series
$\displaystyle \sum (f(n))$ converges iff $\displaystyle
\lim _{n \to \infty} \left( \int _1 ^n f(x) \, dx \right)$ exists
as a real number.
\end{theorem}



[Theorem]{Theorem \ref{thm112}\\
Alternating Series Test}

\begin{theorem}
\label{thm112}
(Alternating Series Test)  If $(a_n)$ is a decreasing sequence
of positive numbers and $\lim a_n = 0$, then the series $\displaystyle
\sum (-1)^{n+1} a_n$ converges.
\end{theorem}



[Theorem]{Theorem \ref{thm113}}

\begin{theorem}
\label{thm113}
\begin{small}
Let $\displaystyle \sum a_n x^n$ be a power series and let
$\alpha = \limsup |a_n|^{\frac 1n}$.  Define $R$ by
$$R = \left\{ \begin{array}{ll} \frac 1{\alpha} & \mbox{ if } 0 < \alpha < +
\infty \\ + \infty & \mbox{ if } \alpha = 0 \\ 0 & \mbox{ if } \alpha = + \infty
\end{array} \right. .$$
Then the series converges absolutely whenever $|x| < R$ and diverges whenever
$|x| > R$.  (When $R = + \infty$ we take this to mean that the series converges
absolutely for all real $x$.  When $R=0$ then the series converges only at
$x=0$.)
\end{small}
\end{theorem}



[Theorem]{Theorem \ref{thm114}\\
Ratio Criterion}

\begin{theorem}
\label{thm114}
(Ratio Criterion)  The radius of convergence $R$ of a power
series $\displaystyle \sum a_n x^n$ is equal to $\displaystyle \lim \left|
\frac{a_n}{a_{n+1}} \right|$, provided that this limit exists.
\end{theorem}



[Theorem]{Theorem \ref{thm115}}

\begin{theorem}
\label{thm115}
Let $(f_n)$ be a sequence of functiond defined on a subset $S$
of $\R$.  There exists a function $f$ such that $(f_n)$ converges to $f$
uniformly on $S$ iff the following condition (called the Cauchy criterion) is
satisfied:

For every $\epsilon > 0$ there exists a number $N$ such that $|f_n(x) - f_m(x)|
< \epsilon$ for all $x \in S$ and all $m,n > N$.
\end{theorem}



[Theorem]{Theorem \ref{thm116}\\ Weierstrass M-test}

\begin{theorem}
\label{thm116}
(Weierstrass M-test)  Suppose that $(f_n)$ is a sequence of
functions defined on $S$ and $(M_n)$ is a sequence of nonnegative numbers such
that $|f_n(x)| \leq M_n$ for all $x \in S$ and all $n \in \N$.  If
$\displaystyle \sum M_n$ converges, then $\displaystyle \sum f_n$ converges
uniformly on $S$.
\end{theorem}



[Theorem]{Theorem \ref{thm117}}

\begin{theorem}
\label{thm117}
Let $(f_n)$ be a sequence of continuous functions defined on a
set $S$ and suppose that $(f_n)$ converges uniformly on $S$ to a function $f: S
\to \R$.  Then $f$ is continuous on $S$.
\end{theorem}



[Corollary]{Corollary \ref{cor8}}

\begin{corollary}
\label{cor8}
Let $\displaystyle \sum _{n=0}^{\infty} f_n$ be a series of
functions defined on a set $S$.  Suppose that each $f_n$ is continuous on $S$
and that the series converges uniformly to a function $f$ on $S$.  Then
$\displaystyle f = \sum _{n = 0} ^{\infty} f_n$ si continuous on $S$.
\end{corollary}



[Theorem]{Theorem \ref{thm118}}

\begin{theorem}
\label{thm118}
Let $(f_n)$ be a sequence of continuous functions defined on an
interval $[a,b]$ and suppose that $(f_n)$ converges uniformly on $[a,b]$ to a
function $f$.  Then $\displaystyle \lim _{n \to \infty} \int _a ^b f_n(x) \, dx
= \int _a ^b f(x) \, dx$.
\end{theorem}



[Corollary]{Corollary \ref{cor9}}

\begin{corollary}
\label{cor9}
Let $\displaystyle \sum _{n=0} ^{\infty} f_n$ be a series of
functions defined on an interval $[a,b]$.  Suppose that each $f_n$ is continuous
on $[a,b]$ and that the series converges uniformly to a function $f$ on $[a,b]$.
 Then $\displaystyle \int _a ^b f(x) \, dx = \sum _{n=0}^{\infty} \int _a ^b
f_n(x) \, dx$.
\end{corollary}



[Theorem]{Theorem \ref{thm119}}

\begin{theorem}
\label{thm119}
Suppose that $(f_n)$ converges to $f$ on an interval $[a,b]$. 
Suppose also that each $f_n'$ exists and is continuous on $[a,b]$, and that the
sequence $(f_n')$ converges uniformly on $[a,b]$.  Then $\displaystyle \lim _{n
\to \infty} f_n'(x) = f'(x)$ for each $x \in [a,b]$.
\end{theorem}



[Corollary]{Corollary \ref{cor10}}

\begin{corollary}
\label{cor10}
Let $\displaystyle \sum _{n = 0}^{\infty} f_n$ be a series of
functions that converges to a function $f$ on an interval $[a,b]$.  Suppose that
for each $n, f_n'$ exists and is continuous on $[a,b]$ and that the series of
derivatives $\displaystyle \sum _{n=0}^{\infty} f_n'$ is uniformly convergent on
$[a,b]$.  Then $\displaystyle f'(x) = \sum _{n=0}^{\infty} f_n'(x)$ for all $x
\in [a,b]$.
\end{corollary}



[Theorem]{Theorem \ref{thm120}}

\begin{theorem}
\label{thm120}
There exists a continuous function defined on $\R$ that is
nowhere differentiable.
\end{theorem} 



[Theorem]{Theorem \ref{thm121}}

\begin{theorem}
\label{thm121}
Let $\displaystyle \sum a_n x^n$ be a power series with radius
of convergence $R$, where $0< R \leq + \infty$.  If $0<K<R$, then teh power
series converges uniformly on $[-K,K]$.
\end{theorem}



[Theorem]{Theorem \ref{thm122}}

\begin{theorem}
\label{thm122}
Suppose that a pwer series converges to a function $f$ on
$(-R,R)$, where $R>0$.  Then the series can be differentiated term by term, and
the differentiated series converges on $(-R,R)$ to $f'$.  That is, if $f(x) =
\displaystyle \sum _{n=0}^{\infty} a_nx^n$, then $f'(x) = \displaystyle \sum
_{n=1}^{\infty} na_nx^{n-1}$, and both series have the same radius of
convergence.
\end{theorem}



[Corollary]{Corollary \ref{cor11}}

\begin{corollary}
\label{cor11}
\begin{small}
Suppose that $f(x) = \displaystyle \sum _{n=0}^{\infty}
a_nx^n$ for $x \in (-R,R)$, where $R>0$.  Then for each $k \in \N$, the $k$th
derivative $f^{(k)}$ of $f$ exists on $(-R,R)$ and 
\begin{eqnarray*}
f^{(k)}(x) & = & \sum _{n=k}^{\infty} \frac{n!}{(n-k)!}a_nx^{n-k} \\
 & = & k! a_k + (k+1)!a_{k+1} + \frac{(k+2)!}{2!}a_{k+2}x^2 + \cdots .
\end{eqnarray*}
Furthermore, $f^{(k)}(0) = k!a_k$.
\end{small}
\end{corollary}



[Corollary]{Corollary \ref{cor12}}

\begin{corollary}
\label{cor12}
If $\displaystyle \sum _{n =0} ^{\infty} a_nx^n = \sum_{n=0}^{\infty} b_nx^n$
for all $x$ in some interval $(-R,R)$, where $R>0$, then
$a_n = b_n$ for all $n \in \N \cup \{ 0 \}$.
\end{corollary}



[Theorem]{Theorem \ref{thm123}}

\begin{theorem}
\label{thm123}
Let $\displaystyle \sum _{n=0}^{\infty} a_nx^n$ be a power
series with a finite positive radius of convergence $R$.  If the series
converges at $x=R$, then it converges uniformly on teh interval $[0,R]$. 
Similarly, if the series converges at $x=-R$, then it converges uniformly on
$[-R,0]$.
\end{theorem}



[Corollary]{Corollary \ref{cor13}}

\begin{corollary}
\label{cor13}
Let $\displaystyle f(x) = \sum _{n=0}^{\infty} a_nx^n$ have a
finite positive radius of convergence $R$.  If the series converges at $x=R$,
then $f$ is continuous at $x=R$.  If the series converges at $x=-R$, then $f$ is
continuous at $x=-R$.
\end{corollary} 



\end{document}
% Electrodynamics Flashcards
% copyright 2006 Jason Underdown






\usepackage{amsmath}

\def\lim{\mathop{\rm lim}}
\newcommand{\xhat}[0]{\mathbf{\hat x}}
\newcommand{\yhat}[0]{\mathbf{\hat y}}
\newcommand{\zhat}[0]{\mathbf{\hat z}}



\section{Electrodynamics}

[Copyright \& License]{Copyright \copyright \, 2007 Jason Underdown \\
Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License.  
For more information, see creativecommons.org.  You can contact the author at:
\begin{center}
\begin{small}\tt jasonu [remove-this] at physics dot utah dot edu\end{small}
\end{center}



[Definition]{gradient}

The gradient $\nabla T$ points in the direction of maximum increase of the 
function $T$.

\medskip
\begin{displaymath}
\nabla T \equiv \xhat \frac{\partial T}{\partial x} +
\yhat \frac{\partial T}{\partial y} +
\zhat \frac{\partial T}{\partial z}
\end{displaymath}

\medskip
The magnitude $|\nabla T|$ is the slope along this direction.



[Definition]{the vector operator $\nabla$}

\begin{displaymath}
\nabla \equiv \xhat \frac{\partial}{\partial x} +
\yhat \frac{\partial}{\partial y} +
\zhat \frac{\partial}{\partial z}
\end{displaymath}



[Definition]{divergence}

\begin{eqnarray*}
\nabla \cdot \mathbf v &=& (\xhat \frac{\partial}{\partial x} +
\yhat \frac{\partial}{\partial y} +
\zhat \frac{\partial}{\partial z}) \cdot
(v_x \xhat + v_y \yhat + v_z \zhat)\\
&=& \frac{\partial v_x}{\partial x} +
\frac{\partial v_y}{\partial y} +
\frac{\partial v_z}{\partial z}
\end{eqnarray*}
The \textit{divergence} is a measure of how much the vector function
$\mathbf v$ spreads out from the point in question.



[Definition]{curl}

\begin{displaymath}
\nabla \times \mathbf v  =
\begin{vmatrix}
\xhat & \yhat & \zhat\\
\frac{\partial}{\partial x} &
\frac{\partial}{\partial y} &
\frac{\partial}{\partial z}\\
v_x & v_y & v_z
\end{vmatrix}
\end{displaymath}
The \textit{curl} is a measure of how much the vector field ``curls around''
the point in question.



[Definition]{5 species of second derivatives}

\begin{small}
By applying $\nabla$ twice we can construct five species of second derivatives.

 divergence of a gradient $\nabla \cdot (\nabla T) = \nabla^2$ (Laplacian)
 curl of a gradient $\nabla \times (\nabla T) = 0$ (always)
 gradient of a divergence $\nabla(\nabla \cdot \mathbf v)$ (seldom occurs)
 divergence of a curl $\nabla \cdot (\nabla \times \mathbf v) = 0$ (always)
 curl of a curl $\nabla \times (\nabla \times \mathbf v) = 
\nabla(\nabla \cdot \mathbf v) - \nabla^2 \mathbf v$

\end{small}



[Theorem]{curl--less or irrotational fields}

For a given vector field $\mathbf F$ the following statements are equivalent, i.e. each implies the others.

 $\nabla \times \mathbf F = 0$ everywhere
 $\int_{\mathbf a}^{\mathbf b} \mathbf F \cdot d \mathbf l$ is path independent
 $\oint \mathbf F \cdot d \mathbf l = 0$ on any closed loop
 $\mathbf F = -\nabla V$ for some scalar potential $V$




[Theorem]{divergence--less or solenoidal fields}

For a given vector field $\mathbf F$ the following statements are equivalent, i.e. each implies the others.

 $\nabla \cdot \mathbf F = 0$ everywhere
 $\int \mathbf F \cdot d \mathbf a$ is independent of surface
 $\oint \mathbf F \cdot d \mathbf a = 0$ over any closed surface
 $\mathbf F = \nabla \times \mathbf A$ for some vector potential $\mathbf A$




[Theorem]{gradient theorem}

\begin{displaymath}
\int_{\mathbf{a}}^{\mathbf{b}} (\nabla f) \cdot d \mathbf{l} = 
f(\mathbf{b}) - f(\mathbf{a})
\end{displaymath}



[Theorem]{Green's theorem}

\begin{displaymath}
\int (\nabla \cdot \mathbf{A}) dV = \oint \mathbf A \cdot d \mathbf a
\end{displaymath}



[Theorem]{Stokes' theorem}

\begin{displaymath}
\int (\nabla \times \mathbf A) \cdot d\mathbf a = \oint \mathbf A \cdot d \mathbf l
\end{displaymath}






\end{document} 
\documentclass[avery5371,grid,letterpaper]{flashcards}




\usepackage{amsfonts}

\newcommand{\R}{\mathbb{R}}
\newcommand{\mathbf{R}^n}{\mathbb{R}^{n}}
\newcommand{\mathbf{R}^m}{\mathbb{R}^{m}}
\newcommand{\nbyn}{n\!\times\!n}
\newcommand{\nbym}{n\times m}



%% Flashcards based on the book "Physics for Scientists and Engineers with Modern Physics"
%% 6th edition by Serway and Jewett

%% Chapter 1

[Chapter 1]{Density}
\bigskip
\bigskip
\begin{displaymath}
\rho \equiv \frac{m}{V}
\end{displaymath}


[Chapter 1]{Significant Figures:  Multiplication}
\bigskip
\bigskip
\begin{quote}
When multiplying several quantities, the number of significant figures in the final answer is the same as the number of significant figures in the quantity having the lowest number of significant figures.  The same rule applies to division.
\end{quote}
\hfill


[Chapter 1]{Significant Figures:  Addition}
\bigskip
\bigskip
\begin{quote}
When numbers are added or subtracted, the number of decimal places in the result should equal the smallest number of decimal places of any term in the sum.
\end{quote}
\hfill


%% Chapter 2

[Chapter 2]{Displacement}
\bigskip
\begin{displaymath}
\Delta x \equiv x_{f} - x_{i}
\end{displaymath}
\begin{center}
\textbf{or} \\
\medskip
Displacement = area under the $v_{x}$--$t$ graph
\end{center}


[Chapter 2]{Average velocity}
\bigskip
\bigskip
\begin{displaymath}
\bar{v}_{x} \equiv \frac{\Delta x}{\Delta t} 
\end{displaymath}


[Chapter 2]{Average speed}
\bigskip
\bigskip
\begin{displaymath}
\textrm{Average speed} = \frac{\textrm{total distance}}{\textrm{total time}}
\end{displaymath}


[Chapter 2]{Instantaneous velocity}
\bigskip
\bigskip
\begin{displaymath}
v_{x} \equiv \lim_{\Delta t \rightarrow 0} \frac{\Delta x}{\Delta t} = \frac{dx}{dt}
\end{displaymath}


[Chapter 2]{Average acceleration}
\bigskip
\bigskip
\begin{displaymath}
\bar{a}_{x} \equiv \frac{\Delta v_{x}}{\Delta t} = \frac{v_{xf} - v_{xi}}{t_{f} - t_{i}}
\end{displaymath}


[Chapter 2]{Instantaneous acceleration}
\bigskip
\bigskip
\begin{displaymath}
a_{x} \equiv \lim_{\Delta t \rightarrow 0} \frac{\Delta v_{x}}{\Delta t} = \frac{dv_{x}}{dt}
\end{displaymath}


[Chapter 2]{Velocity as a function of time}
\bigskip
\begin{displaymath}
v_{xf} = v_{xi} + a_{x}t
\end{displaymath}
\begin{center}
(constant acceleration)
\end{center}


[Chapter 2]{Position as a function of velocity and time}
\bigskip
\begin{displaymath}
x_{f} = x_{i} + \frac{1}{2}\left( v_{xi} + v_{xf}\right)t
\end{displaymath}
\begin{center}
(constant acceleration)
\end{center}


[Chapter 2]{Position as a function of time}
\bigskip
\begin{displaymath}
x_{f} = x_{i} + v_{xi}t + \frac{1}{2}a_{x}t
\end{displaymath}
\begin{center}
(constant acceleration)
\end{center}


[Chapter 2]{Velocity as a function of position}
\bigskip
\begin{displaymath}
v_{xf}^{2} = v_{xi}^{2} + 2a_{x}\left( x_{f} - x_{i}\right) 
\end{displaymath}
\begin{center}
(constant acceleration)
\end{center}


%% Chapter 3

[Chapter 3]{Polar $\Longrightarrow$ Cartesian}
\bigskip
\bigskip
\begin{eqnarray}
x &=& r\cos \theta \nonumber\\
y &=& r\sin \theta \nonumber
\end{eqnarray}


[Chapter 3]{Cartesian $\Longrightarrow$ Polar}
\bigskip
\bigskip
\begin{eqnarray}
r &=& \sqrt{x^{2} + y^{2}} \nonumber\\
\tan \theta &=& \frac{y}{x} \nonumber
\end{eqnarray}


[Chapter 3]{Scalar quantity}
\bigskip
\bigskip
\begin{quote}
A value with magnitude only and \textbf{no} associated direction
\end{quote}
\hfill


[Chapter 3]{Vector quantity}
\bigskip
\bigskip
\begin{quote}
A value that has both magnitude and direction
\end{quote}
\hfill


%% Chapter 4

[Chapter 4]{Velocity vector as a function of time}
\bigskip
\bigskip
\begin{displaymath}
\mathbf{v}_{f} = \mathbf{v}_{i} + \mathbf{a} t
\end{displaymath}


[Chapter 4]{Position vector as a function of time}
\bigskip
\bigskip
\begin{displaymath}
\mathbf{r}_{f} = \mathbf{r}_{i} + \mathbf{v}_{i}t + \frac{1}{2} \mathbf{a}t^{2}
\end{displaymath}


[Chapter 4]{Centripetal acceleration}
\bigskip
\bigskip
\begin{displaymath}
a_{c} = \frac{v^{2}}{r}
\end{displaymath}


[Chapter 4]{Period of circular motion}
\bigskip
\bigskip
\begin{displaymath}
T \equiv \frac{2 \pi r}{v}
\end{displaymath}


[Chapter 4]{Total acceleration}
\bigskip
\bigskip
\begin{displaymath}
\mathbf{a} = \mathbf{a}_{t} + \mathbf{a}_{r} = \frac{d \mid \mathbf{v} \mid}{dt} \hat{\mathbf{\theta}} - \frac{v^{2}}{r} \hat{\mathbf{r}}
\end{displaymath}


[Chapter 4]{Galilean Transformation}
\bigskip
\bigskip
\begin{eqnarray}
\mathbf{r}^{\prime} &=& \mathbf{r} - \mathbf{v}_{0}t \nonumber\\
\mathbf{v}^{\prime} &=& \mathbf{v} - \mathbf{v}_{0} \nonumber
\end{eqnarray}


%% Chapter 5

[Chapter 5]{Newton's First Law}
\smallskip
\begin{quote}
In the absence of external forces, when viewed from an inertial reference frame, an object at rest remains at rest and an object in motion continues in motion with a constant velocity (that is, with a constant speed in a a straight line).
\\
\smallskip
\textbf{When no force acts on an object, the acceleration of the object is zero}
\end{quote}
\hfill



[Chapter 5]{Newton's Second Law}
\bigskip
\begin{quote}
When viewed from an inertial reference frame, the acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass.
\end{quote}
\begin{displaymath}
\sum \mathbf{F} = m\mathbf{a}
\end{displaymath}
\hfill



[Chapter 5]{Newton's Third Law}
\bigskip
\begin{quote}
If two objects interact, the force $\mathbf{F}_{12}$ exerted by object 1 on object 2 is equal in magnitude and opposite in direction to the force $\mathbf{F}_{21}$ exerted by object 2 on object 1:
\end{quote}
\begin{displaymath}
\mathbf{F}_{12} = -\mathbf{F}_{21}
\end{displaymath}
\hfill


%% Chapter 6

[Chapter 6]{Force causing centripetal acceleration}
\bigskip
\bigskip
\begin{displaymath}
\sum \mathbf{F} = ma_{c} = m\frac{v^{2}}{r}
\end{displaymath}


[Chapter 6]{Nonuniform circular motion}
\bigskip
\bigskip
\begin{displaymath}
\sum \mathbf{F} = \sum \mathbf{F}_{r} + \sum \mathbf{F}_{t}
\end{displaymath}


%% Chapter 7

[Chapter 7]{Scalar, dot or inner product}
\bigskip
\bigskip
\begin{eqnarray}
\mathbf{A}\cdot \mathbf{B} &=& AB \cos \theta \nonumber \\
\mathbf{A}\cdot \mathbf{B} &=& A_{x}B_{x} + A_{y}B_{y} + A_{z}B_{z} \nonumber
\end{eqnarray}



[Chapter 7]{Work done by a constant force}
\bigskip
\bigskip
\begin{displaymath}
W \equiv F\Delta r \cos \theta
\end{displaymath}


[Chapter 7]{Work done by a varying force}
\bigskip
\bigskip
\begin{displaymath}
W = \int_{x_{i}}^{x_{f}} F_{x}dx
\end{displaymath}


[Chapter 7]{Spring force}
\bigskip
\bigskip
\begin{displaymath}
F_{s} = -kx
\end{displaymath}



\end{document}


% Probability Flashcards
% Copyright 2006 Jason Underdown






\usepackage{amsfonts}
\usepackage{amsmath}

\newcommand{\R}{\mathbb{R}}
\newcommand{\mathbf{R}^n}{\mathbb{R}^{n}}
\DeclareMathOperator{\var}{var}
\DeclareMathOperator{\stddev}{stddev}
\def\lim{\mathop{\rm lim}}




\section{Probability}

[Copyright \& License]{Copyright \copyright \, 2006 Jason Underdown \\
Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License.  
For more information, see creativecommons.org.  You can contact the author at:
\begin{center}
\begin{small}\tt jasonu [remove-this] at physics dot utah dot edu\end{small}
\end{center}



[Definition]{choose notation}

\textit{n choose k} is a brief way of saying how many ways can you choose $k$
objects from a set of $n$ objects, when the order of selection is not relevant.
\begin{displaymath}
{n \choose k} = \frac{n!}{(n-k)! \; k!}
\end{displaymath}
Obviously, this implies $0 \leq k \leq n$.



[Theorem]{binomial theorem}

\begin{displaymath}
(x + y)^n = \sum_{k=0}^{n} {n \choose k} x^k y^{n-k}
\end{displaymath}



[Definition]{$n$ distinct items divided into \\
$r$ distinct groups}

Suppose you want to divide $n$ distinct items in to $r$ distinct groups
each with size $n_1, n_2, \ldots, n_r$, how do you count the possible outcomes?

\smallskip
If $n_1 + n_2 + \ldots + n_r = n$, then the number of possible divisions can be
counted by the following formula:
\begin{displaymath}
{n \choose n_1, n_2, \ldots, n_r} = \frac{n!}{n_1! \; n_2! \ldots n_r!}
\end{displaymath}



[Axioms]{axioms of probability}


 $0 \leq P(E) \leq 1$
 $P(S) = 1$
 For any sequence of mutually exclusive events $E_1,E_2,\ldots$ \\
(i.e. events where $E_i E_j = \emptyset$ when $i\neq j$)
\begin{displaymath}
P \left( \bigcup_{i=1}^{\infty} E_i \right) = \sum_{i=1}^{\infty} P(E_i)
\end{displaymath}




[Proposition]{probability of the complement}

If $E^c$ denotes the complement of event $E$, then
\begin{displaymath}
P(E^c) = 1 - P(E)
\end{displaymath}



[Proposition]{probability of the union of two events}

\begin{displaymath}
P(A \cup B) = P(A) + P(B) - P(A B)
\end{displaymath}



[Definition]{conditional probability}

If $P(F) > 0$, then
\begin{displaymath}
P(E\mid F) = \frac{P(EF)}{P(F)}
\end{displaymath}



[Theorem]{the multiplication rule}

\begin{displaymath}
P(E_1 E_2 E_3 \ldots E_n) = 
\end{displaymath}
\begin{displaymath}
P(E_1)P(E_2\mid E_1)P(E_3 \mid E_2 E_1)\ldots P(E_n\mid E_1 \ldots E_{n-1})
\end{displaymath}



[Theorem]{Bayes' formula}

\begin{eqnarray*}
P(E) &=& P(E F) + P(E F^c) \\
     &=& P(E\mid F)P(F) + P(E\mid F^c)P(F^c) \\
     &=& P(E\mid F)P(F) + P(E\mid F^c)[1-P(F)] \\
\end{eqnarray*}



[Definition]{independent events}

Two events $E$ and $F$ are said to be \textit{independent} iff
\begin{displaymath}
P(EF) = P(E)P(F)
\end{displaymath}
Otherwise they are said to be \textit{dependent}.



[Definition]{probability mass function of
a discrete random variable}

For a discrete random variable $X$, we define the
\textit{probability mass function} $p(a)$ of $X$ by
\begin{displaymath}
p(a) = P\lbrace X=a \rbrace
\end{displaymath}
Probability mass functions are often written as a table.



[Definition]{cumulative distribution function $F$}

The \textit{cumulative distribution function ($F$)} is defined to be
\begin{displaymath}
F(a) = \sum_{all \; x \leq a} p(x)
\end{displaymath}
The cumulative distribution function $F(a)$ denotes the probability
that the random variable $X$ has a value less than or equal to $a$.



[Theorem]{properties of the cumulative 
distribution function}

The cumulative distribution function satisfies the following properties:

 $F$ is a nondecreasing function
 $\lim_{a\to\infty} F(a) = 1$
 $\lim_{a\to-\infty} F(a) = 0$




[Definition]{expected value \\(discrete case)}

\begin{displaymath}
E[X] = \sum_{x:p(x)>0} x p(x)
\end{displaymath}



[Proposition]{expected value of a function of $X$ \\ 
(discrete case)}

If $X$ is a discrete random variable that takes on the values denoted
by $x_i$ $(i=1\ldots n)$ with respective probabilities $p(x_i)$, then for
any real--valued function $f$
\begin{displaymath}
E[f(X)] = \sum_{i=1}^{n} f(x_i) p(x)
\end{displaymath}



[Corollary]{linearity of expectation}

If $\alpha$ and $\beta$ are constants, then
\begin{displaymath}
E[\alpha X + \beta] = \alpha E[X] + \beta
\end{displaymath}



[Definition/Theorem]{variance}

If $X$ is a random variable with mean $\mu$, then we define the
\textit{variance} of $X$ to be
\begin{eqnarray*}
\var(X) &=& E[(X-\mu)^2] \\
        &=& E[X^2] - (E[X])^2 \\
        &=& E[X^2] - \mu^2
\end{eqnarray*}
The first line is the actual definition, but the second and third
equations are often more useful and can be shown to be equivalent
by some algebraic manipulation.



[Definition]{probability mass function of a \\
Bernoulli random variable}

If an experiment can be classified as either success or failure, and if
we denote success by $X=1$ and failure by $X=0$ then, $X$ is a
\textit{Bernoulli random variable} with probability mass function:
\medskip
\begin{center}
\begin{tabular}{ccccc}
$p(0)$ & $=$ & $P\lbrace X=0\rbrace$ & $=$ & $1-p$ \\
$p(1)$ & $=$ & $P\lbrace X=1\rbrace$ & $=$ & $p$ \\
\end{tabular}
\end{center}
where $p$ is the probability of success and $0\leq p \leq 1$.



[Definition]{probability mass function of a \\
binomial random variable}

Suppose $n$ independent Bernoulli trials are performed.  If the probability
of success is $p$ and the probability of failure is $1-p$, then $X$ is said
to be a \textit{binomial random variable} with parameters $(n,p)$.

The probability mass function is given by:
\begin{displaymath}
p(i) = {n \choose i} p^i(1-p)^{n-i}
\end{displaymath}
where $i=0,1,\ldots ,n$



[Theorem]{properties of binomial random variables}

If $X$ is a binomial random variable with parameters $n$ and $p$, then
\begin{eqnarray*}
E[X] &=& np \\
\var(X) &=& np(1-p) \\
\end{eqnarray*}



[Definition]{probability mass function of a \\
Poisson random variable}

A random variable $X$ that takes on one of the values 0,1,$\ldots$, is
said to be a \textit{Poisson random variable} with parameter $\lambda$
if for some $\lambda > 0$
\begin{displaymath}
p(i) = P \lbrace X=i \rbrace  = \frac{\lambda^i}{i!}e^{-\lambda}
\end{displaymath}
where $i = 0,1,2,\ldots$



[Theorem]{properties of Poisson random variables}

If $X$ is a Poisson random variable with parameter $\lambda$, then
\begin{eqnarray*}
E[X] &=& \lambda \\
\var(X) &=& \lambda \\
\end{eqnarray*}



[Definition]{probability mass function of a \\
geometric random variable}

Suppose independent Bernoulli trials, are repeated until success
occurs.  If we let $X$ equal the number of trials required to
achieve success, then $X$ is a \textit{geometric random variable}
with probability mass function:
\begin{displaymath}
p(n) = P \lbrace X = n \rbrace = (1-p)^{n-1}p
\end{displaymath}
where $n=1,2,\ldots$



[Theorem]{properties of geometric random variables}

If $X$ is a geometric random variable with parameter $p$, then
\begin{eqnarray*}
E[X] &=& \frac{1}{p} \\
\var(X) &=& \frac{1-p}{p^2} \\
\end{eqnarray*}



[Definition]{probability mass function of a \\
negative binomial random variable}

Suppose that independent Bernoulli trials (with probability of succes $p$)
are performed until $r$ successes occur.
If we let $X$ equal the number of trials required, then $X$ is a
\textit{negative binomial random variable} with probability mass function:
\begin{displaymath}
p(n) = P \lbrace X = n \rbrace =
{n-1 \choose r-1} p^r(1-p)^{n-r}
\end{displaymath}
where $n = r, r+1,\ldots$



[Theorem]{properties of negative binomial random variables}

If $X$ is a negative binomial random variable with parameters $(p,r)$, then
\begin{eqnarray*}
E[X] &=& \frac{r}{p} \\
\var(X) &=& \frac{r(1-p)}{p^2} \\
\end{eqnarray*}



[Definition]{probability density function of a
continuous random variable}

We define $X$ to be a \textit{continuous} random variable if there
exists a function $f$, such that for any set $B$ of real numbers
\begin{displaymath}
P\lbrace X\in B\rbrace = \int_B f(x)dx
\end{displaymath}
The function $f$ is called the \textit{probability density function}
of the random variable $X$.



[Definition]{probability density function of a \\
uniform random variable}

If $X$ is a \textit{uniform} random variable on the interval $(\alpha,\beta)$,
then its probability density function is given by
\begin{displaymath}
f(x) = \left\{
\begin{array}{ll}
\frac{1}{\beta - \alpha} & \textrm{if $\alpha < x < \beta$}\\
0 & \textrm{otherwise}
\end{array} \right.
\end{displaymath}



[Theorem]{properties of uniform random variables}

If $X$ is a uniform random variable with parameters $(\alpha,\beta)$, then
\begin{eqnarray*}
E[X] &=& \frac{\alpha + \beta}{2}\\
\var(X) &=& \frac{(\beta - \alpha)^2}{12}
\end{eqnarray*}



\end{document}
% Quantum Mechanics Flashcards
% Copyright 2007 Jason Underdown



\usepackage[latin1]{inputenc}
\usepackage{amsfonts}
\usepackage{amsmath}





\section{Quantum Mechanics}

[Copyright \& License]{Copyright \copyright \, 2007 Jason Underdown \\
Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License.  
For more information, see creativecommons.org.  You can contact the author at:
\begin{center}
\begin{small}\tt jasonu [remove-this] at physics dot utah dot edu\end{small}
\end{center}



[Equation]{Schr\"odinger equation\\non-operator form}

\begin{displaymath}
i\hbar \frac{\partial \Psi}{\partial t} = -\frac{\hbar^2}{2m}
\frac{\partial^2 \Psi}{\partial x^2} + V \Psi
\end{displaymath}



[Definition]{statistical interpretation of the wave function}

\begin{displaymath}
\int_a^b |\Psi(x,t)|^2 dx =
\framebox[4.5cm]{\parbox[c]{4cm}{probability of finding the particle
between $a$ and $b$, at time $t$}}
\end{displaymath}



[Formula]{Euler's formula}

\begin{displaymath}
e^{i\theta} = \cos \theta + i\sin \theta
\end{displaymath}



[Equation]{time--independent Schr\"odinger equation}

The simplest way to write the time--independent Schr\"odinger equation is
$H\psi = E\psi$, however, with the Hamiltonian operator expanded it becomes:

\medskip
\begin{displaymath}
-\frac{\hbar^2}{2m} \frac{d^2 \psi}{dx^2} + V\psi = E\psi\\
\end{displaymath}



[Definition]{Hamiltonian operator}

\begin{displaymath}
\textrm{\^H} = -\frac{\hbar^2}{2m}\nabla^2 + V
\end{displaymath}



\end{document}




\section{Quantum Statistical Mechanics}

%\usepackage{amsfonts}
\usepackage{amssymb,amsmath}



[Copyright \& License]{Copyright \copyright \, 2007 Jason Underdown \\
Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License.  
For more information, see creativecommons.org.  You can contact the author at:
\begin{center}
\begin{small}\tt jasonu [remove-this] at physics dot utah dot edu\end{small}
\end{center}



[Definition]{spin excess}

Assuming $N$ is even, then we define the \textit{spin excess} by
\begin{equation*}
N_{\uparrow} - N_{\downarrow} = 2s
\end{equation*}



[Formula]{multiplicity function}

\begin{equation*}
g(N,s) = 
\frac{N!}{\left(\frac{1}{2}N+s \right)! \left(\frac{1}{2}N-s \right)!} =
\frac{N!}{N_{\uparrow}! \; N_{\downarrow}!}
\end{equation*}



[Formula]{Stirling's approximation}

\begin{equation*}
N! \approx (2\pi N)^{1/2} N^{N} \exp(-N +(1/12)N + \cdots)
\end{equation*}



[Formula]{approximate multiplicity function}

\begin{equation*}
G(N,s) \approx (2 / \pi N)^{1/2} 2^{N} \exp(-2s^2/N)
\end{equation*}



[Assumption]{fundamental assumption}

The fundamental assumption of statistical mechanics is that in a closed system,
each of its \textit{accessible} states is \textit{equally likely}.



[Definition]{probability of states}

If $s$ is a state of a system, then the probability of that
state is given by:
\begin{equation*}
P(s) = \left\{ \begin{array}{cl}
1/g & \text{if $s$ is an accessible state} \\
0   & \text{otherwise}
\end{array} \right.
\end{equation*}
The sum of the probabilities over all states is unity.
\begin{equation*}
\sum_{s} P(s) = 1
\end{equation*}



[Definition]{expectation\\average value}

Suppose that a system has some physical property $X=X(s)$ when the
system is in state $s$.  The \textit{expected} or \textit{average value} of $X$ is 
defined by:
\begin{equation*}
\left\langle X \right\rangle = \sum_{s} X(s)P(s)
\end{equation*}



[Definition]{entropy}

\begin{equation*}
\sigma(N,U) \equiv \ln g(N,U)
\end{equation*}



[Equation]{condition for thermal equilibrium}

If two systems are in thermal contact, the condition for them
to be in \textit{thermal equilibrium} is the following:
\begin{equation*}
\left(
\dfrac{\partial \sigma_{1}}{\partial U_{1}}
\right)_{\!\!\! N_1} = \left(
\dfrac{\partial \sigma_{2}}{\partial U_{1}}
\right)_{\!\!\! N_2}
\end{equation*}



[Definition]{fundamental temperature\\Kelvin temperature\\Boltzmann constant}

\begin{equation*}
\dfrac{1}{\tau} \equiv
\left( \dfrac{\partial \sigma}{\partial U} \right)_{\!\!\! N}
\end{equation*}
\bigskip
\begin{equation*}
\tau = k_B T
\end{equation*}
\medskip
\begin{equation*}
k_B = 1.381 \times 10^{-23} \text{ J/K}
\end{equation*}



[Definition]{relationship between entropy\\and classical thermodynamic entropy}

\begin{equation*}
\dfrac{1}{T} = \left( \dfrac{\partial S}{\partial U} \right)_{\!\!\! N}
\end{equation*}
\bigskip
\begin{equation*}
S = k_B \sigma
\end{equation*}



[Equation]{multiplicity function for the Hydrogen atom}

The multiplicity function for a Hydrogen atom with
energy $E_n$, is given by
\begin{equation*}
g(n) = \sum_{l=0}^{n-1} (2l+1)  = n^2
\end{equation*}
where $n$ is the principal quantum number, and $l$ is the orbital quantum
number.



[Equation]{multiplicity function for 3D harmonic oscillator}

The multiplicity function for a simple harmonic oscillator with three
degrees of freedom with energy $E_n$ is given by
\begin{equation*}
g(n) = \dfrac{1}{2}(n+1)(n+2)
\end{equation*}
where $n = n_x + n_y + n_z$.



[]{}





[]{}





[]{}





[]{}





[]{}





[]{}





\end{document}


\newcommand{\deriv}[2]{\frac{\mathrm{d}#1}{\mathrm{d}#2}}
\newcommand{\pderiv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\dQ}[0]{d^{\prime}\!Q}
\newcommand{\dW}[0]{d^{\prime}\!W}





\section{Thermodynamics}

[Equation]{Ideal Gas Law}
  
  \begin{center}
    \begin{displaymath}
      Pv = nRT
    \end{displaymath}
  \end{center}
  


[Equation]{Van der Waals Equation}
  
  \begin{center}
    \begin{displaymath}
      \left(P+\frac{a}{v^2}\right)\left(v-b\right) = RT
    \end{displaymath}
  \end{center}
  


[Definition]{Coefficient of Volume Expansion\\$\beta$}
  
  \begin{center}
    \begin{displaymath}
      \beta = \frac{1}{V}{\left(\pderiv{V}{T}\right)}_P
    \end{displaymath}
  \end{center}
  


[Definition]{Isothermal Compressibility\\$\kappa$}
  
  \begin{center}
    \begin{displaymath}
      \kappa= -\frac{1}{V}\left(\pderiv{V}{P}\right)_T
    \end{displaymath}
  \end{center}
  


[Equation]{Volume Differential\\$dV$}
  
  \begin{center}
    \begin{displaymath}
      dV = {\left(\pderiv{V}{T}\right)}_P\!\!dT  + {\left(\pderiv{V}{P}\right)}_T\!\!dP
    \end{displaymath}
  \end{center}
  


[Definition]{Exact Differential}
  
  \begin{tiny}
  The following two properties are equivalent ways of determining exactness:\\
  1. Mixed second order partial derivatives are equal e.g.:
  \begin{displaymath}
    \frac{\partial^2 V}{\partial P \partial T} = 
    \frac{\partial^2 V}{\partial T \partial P}
  \end{displaymath}
  2. Integral is independent of path
  \begin{displaymath}
    \int_{V_1}^{V_2} dV = V_1 - V_2 \qquad \oint dV = 0
  \end{displaymath}
  A quantity whose differential is \emph{not} exact is not a thermodynamic property.
  \end{tiny}
  


[Law]{First Law of Thermodynamics}
  
  \begin{center}
    \begin{displaymath}
      \begin{array}{ll}
	\Delta U = & Q - W\\
	 & \\
	dU = &\dQ - \dW
      \end{array}
    \end{displaymath}
    \medskip
    (Where the primes denote inexact differentials)
  \end{center}
  


[Definition]{Enthalpy}
  
  \begin{center}
    \begin{displaymath}
      H = U + PV
    \end{displaymath}
  \end{center}
  


[Definition]{Heat Capacity}
  
  \begin{center}
    \begin{displaymath}
      C = \lim_{\Delta T\to0} \frac{Q}{\Delta T} = \frac{\dQ}{dT}
    \end{displaymath}
    \begin{displaymath}
      Q = C(T_2 - T_1) = nc(T_2 - T_1)
    \end{displaymath}
  \end{center}
  


[Equation]{Thermodynamic Potentials}
  
  \begin{center}
    \begin{tabular}{rc}
       & \begin{math}-TS\end{math} \\
       & \begin{math}\longrightarrow\end{math} \\
      \begin{math}+PV \downarrow\end{math} &
      {
	\begin{tabular}{|c|c|}
	  \hline
	  U & F \\
	  \hline
	  H & G \\
	  \hline
	\end{tabular}
      } \\
    \end{tabular}
  \end{center}
  


\end{document}




\section{Topology}

\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{mathrsfs}

\newcommand{\N}{\mathbb{N}}
\newcommand{\Z}{\mathbb{Z}}
\newcommand{\Q}{\mathbb{Q}}
\newcommand{\R}{\mathbb{R}}
\newcommand{\st}{\textrm{ such that }}
\newcommand{\setst}{\; | \;}



[Copyright \& License]{Copyright \copyright \,
2007 Jason Underdown \\ Some rights reserved.}

These flashcards and the accompanying \LaTeX \, source code are licensed
under a Creative Commons Attribution--NonCommercial--ShareAlike 2.5 License.  
For more information, see creativecommons.org.  You can contact the author at:
\begin{center}
\begin{small}\tt jasonu at physics utah edu\end{small}
\end{center}



[Definition]{metric space}

A \textbf{metric space} $(X,d)$ is a set $X$ and a function
\mbox{$d: X \times X \rightarrow \R$} satisfying $\forall \; x,y,z \in X$

  $d(x,y) \geq 0$
  $d(x,y) = 0 \Leftrightarrow x=y$
  $d(x,y) = d(y,x)$
  $d(x,z) \leq d(x,y) + d(y,z)$




[Definition]{subspace}

If $(X,d)$ is a metric space, and $A \subset X$ then
$(A,d|_{A \times A})$ is a metric space and is called
a \mbox{\textbf{subspace}} of $(X,d)$.



[Definition]{isometry}

Suppose $(X_1,d_1)$ and $(X_2,d_2)$ are metric spaces.  A function
$f: X_1 \rightarrow X_2$ is called an \mbox{\textbf{isometry}} if 
$f$ is one--to--one, onto and
\begin{equation*}
d_2(f(x),f(y)) = d_1(x,y) \quad \forall \; x,y \in X_1
\end{equation*}



[Definition]{open set}

Supposing $(X,d)$ is a metric space, then a subset $U \subset X$
is \textbf{open} iff
\begin{equation*}
\forall \; x \in U, \exists \; r>0 \st B(x,r) \subset U
\end{equation*}



[Proposition]{open balls are open}

If $(X,d)$ is a metric space, then for each $x \in X$ and for each
$r>0$, $B(x,r)$ is open in X.



[Theorem]{unions and intersections of open sets}

Let $(X,d)$ be a metric space and let $\left\{U_{\alpha}\right\}_{\alpha \in A}$ be any
collection of open sets in $(X,d)$, then

  $X,\varnothing$ are open.
  $\bigcup_{\alpha \in A} U_{\alpha}$ is open.
  Let $\left\{U_1, \ldots , U_n\right\}$ be a finite
 collection of open sets, then $\bigcap^{n}_{i=1}U_i$ is open.




[Definition]{closed set}

Let $(X,d)$ be a metric space, $F \subset X$ is \mbox{\textbf{closed}} iff
$X - F$ is open.



[Definition]{closed ball}

A \mbox{\textbf{closed ball}} centered at $x$ of radius $r$ is denoted
$\overline{B}(x,r)$, and defined to be:
\begin{equation*}
\overline{B}(x,r) = \left\{ y \in X \setst d(x,y) \leq r \right\}
\end{equation*}



[Proposition]{closed balls are closed sets}

A closed ball $\overline{B}(x,r)$, is a closed set.



[Theorem]{unions and intersections of closed sets}

Let $(X,d)$ be a metric space and let $\left\{F_{\alpha}\right\}_{\alpha \in A}$ be any
collection of closed sets in $(X,d)$, then

  $X,\varnothing$ are closed.
  $\bigcap_{\alpha \in A} F_{\alpha}$ is closed.
  Let $\left\{F_1, \ldots , F_n\right\}$ be a finite collection of
 closed sets, then $\bigcup^{n}_{i=1}F_i$ is closed.




[Definition]{interior}

Let $(X,d)$ be a metric space with $A \subset X$.  The \mbox{\textbf{interior}}
of $A$ denoted $A^{\circ}$  is defined to be:
\begin{equation*}
A^{\circ} = \left\{ x \in A \setst \exists \; r>0 \st B(x,r) \subset A \right\}
\end{equation*}



[Definition]{closure}

Let $(X,d)$ be a metric space with $A \subset X$.  The \mbox{\textbf{closure}}
of $A$ denoted $\overline{A}$  is defined to be:
\begin{equation*}
\overline{A} = \left\{ x \in X \setst \forall \; r>0, B(x,r) \cap A
\neq \varnothing\right\}
\end{equation*}



[Definition]{exterior \& frontier}

Let $(X,d)$ be a metric space with $A \subset X$.

\bigskip
The \mbox{\textbf{exterior}} of a set $A$ is defined to be $(X-A)^{\circ}$.

\bigskip
The \mbox{\textbf{frontier}} of a set $A$ is defined to be $\overline{A}-A^{\circ}$.



[Definition]{distance from a point to a set}

Suppose $(X,d)$ is a metric space with $A \subset X$ and $x \in X$.  We
define \textbf{the distance from $x$ to $A$} by
\begin{equation*}
d(x,A) = \textrm{inf} \left\{ d(x,y) \setst y \in A \right\}
\end{equation*} 



[Definition]{limit of a sequence}

Suppose $(X,d)$ is a metric space.  A sequence $\left\{ x_n \right\} \subset X$
has \mbox{\textbf{limit}} $x$, denoted 
$\lim_{n \rightarrow \infty}   \left\{ x_n \right\} = x$ iff
\begin{equation*}
\forall \; \varepsilon >0, \; \exists \; N \in \N \st
\end{equation*}
\begin{equation*}
n \geq N \Rightarrow x_n \in B(x,\varepsilon)
\end{equation*}



[Definition]{Cauchy Sequence}

Suppose $(X,d)$ is a metric space.
A sequence $\left\{ x_n \right\} \subset X$ is called a
\mbox{\textbf{Cauchy sequence}} iff
\begin{equation*}
\forall \; \varepsilon >0, \; \exists \; N \in \N \st
\end{equation*}
\begin{equation*}
m,n \geq N \Rightarrow d(x_m,x_n) < \varepsilon
\end{equation*}



[Definition]{convergent sequence}

A sequence $\left\{ x_n \right\}$ \mbox{\textbf{converges}} iff
$\lim \left\{ x_n \right\}$ exits.



[Theorem]{convergence implies Cauchy}

If a sequence $\left\{ x_n \right\}$ is convergent then it is Cauchy.



[Definition]{complete metric space}

A metric space $(X,d)$ is \mbox{\textbf{complete}} iff every Cauchy sequence
in $X$ is convergent.



[Theorem]{limits are unique}

If the limit of $\left\{ x_n \right\}$ exists, then that limit is unique.



[Theorem]{distinct points have a radius of separation}

Suppose $(X,d)$ is a metric space, and $x,y \in X$ with $x \neq y$, then
$\exists \; r > 0 \st B(x,r) \cap B(y,r) = \varnothing$



[Definition]{continuous function}

Suppose $(X_1,d_1), (X_2, d_2)$ are metric spaces.  A function
$f:X_1 \rightarrow X_2$ is \mbox{\textbf{continuous}} at $x \in X_1$ iff
\begin{equation*}
\forall \; \varepsilon >0, \; \exists \; \delta (x,\varepsilon) >0 \st 
\end{equation*}
\begin{equation*}
d_1(x,y) < \delta \Rightarrow d_2(f(x), f(y)) < \varepsilon
\end{equation*}



[Definition]{continuous function (alternate definition)}

Suppose $(X_1,d_1), (X_2, d_2)$ are metric spaces.  A function
$f:X_1 \rightarrow X_2$ is \mbox{\textbf{continuous}} on $X_1$ iff
\begin{equation*}
\forall \; x \in X_1, \; \forall \; \varepsilon >0, \; \exists \; \delta >0 \st 
\end{equation*}
\begin{equation*}
f(B(x,\delta)) \subset B(f(x), \varepsilon)
\end{equation*}



[Definition]{Lipschitz function}

Suppose $(X_1,d_1), (X_2, d_2)$ are metric spaces.  A function
$f:X_1 \rightarrow X_2$ is called \mbox{\textbf{Lipschitz}} iff
\begin{equation*}
\forall \; x,y \in X_1 \; \exists \; c>0 \st
\end{equation*}
\begin{equation*}
d_2(f(x),f(y)) \leq c d_1(x,y)
\end{equation*}
A Lipschitz function can be thought of as a ``bounded distortion.''



[Theorem]{Lipschitz functions are uniformly continuous}

If $f:X_1 \rightarrow X_2$ is Lipschitz on $X_1$, then $f$ is uniformly
continuous on $X_1$.



[Definition]{bi-Lipschitz}

Suppose $(X_1,d_1), (X_2, d_2)$ are metric spaces.  A function
$f:X_1 \rightarrow X_2$ is called \mbox{\textbf{bi-Lipschitz}} iff
\begin{equation*}
\forall \; x,y \in X_1 \; \exists \; c_1,c_2>0 \st
\end{equation*}
\begin{equation*}
c_1 d_1(x,y) \leq d_2(f(x),f(y)) \leq c_2 d_1(x,y)
\end{equation*}



[Theorem]{$f$ continuous iff \\
the preimage of every open set is open}

A function $f:X_1 \rightarrow X_2$ is continuous iff 
\begin{equation*}
\forall \; U \mbox{ open }\subset X_2 \Rightarrow
f^{-1}(U) \mbox{ open }\subset X_1
\end{equation*}
Or equivalently:
\begin{equation*}
\forall \; U \mbox{ closed }\subset X_2 \Rightarrow
f^{-1}(U) \mbox{ closed }\subset X_1
\end{equation*}



[Theorem]{continuous functions and sequences}

A function $f:(X_1,d_1) \rightarrow (X_2,d_2)$ is continuous iff
\begin{equation*}
\forall \; \mbox{ convergent sequences } \left\{ x_n \right\} \subset X_1,
\end{equation*}
\begin{equation*}
\lim_{n\rightarrow \infty} f(x_n) = f(\lim_{n\rightarrow \infty}
\left\{ x_n \right\})
\end{equation*}



[Definition]{homeomorphism}

A function $f:(X_1,d_1) \rightarrow (X_2,d_2)$ is called a
\mbox{\textbf{homeomorphism}} iff

  $f$ is continuous
  $f$ is 1-1 and onto
  $f^{-1}$ is continous




[Definition]{equivalent metrics}

Two metrics $d_1$, $d_2$ are called \mbox{\textbf{equivalent}} iff
they have the same open sets.



[Remark]{two metrics are equivalent iff \\
the identity map is a homeomorphism}

Two metrics, $d_1$, $d_2$ are equivalent iff $id: (X,d_1) \rightarrow (X,d_2)$
is a homeomorphism.



[Theorem]{composition of continuous functions \\
preserves continuity}

Suppose $f:X_1 \rightarrow X_2$ and $g:X_2 \rightarrow X_3$.  If $f$
and $g$ are continuous then $g\circ f$ is continuous.



[Definition]{homeomorphic spaces}

Two metric spaces are \mbox{\textbf{homeomorphic}} iff there exists a
homeomorphism between them.



[Definition]{topology}

Suppose $X$ is a set.  A collection $\tau$ of subsets of $X$ is called
a \mbox{\textbf{topology}} on $X$ iff

  $X \in \tau$ and $\varnothing \in \tau$
  $U_{\alpha} \in \tau \;
 \mbox{ for } \alpha \in A \Rightarrow
 \displaystyle \bigcup_{\alpha \in A} U_{\alpha} \in \tau$
  $U_1, U_2, \ldots , U_n \in \tau \Rightarrow
 \displaystyle \bigcap_{i=1}^{\infty} U_i \in \tau$




[Definition]{topological space}

A \mbox{\textbf{topological space}} $(X,\tau)$ is a set $X$ and a 
topology $\tau$ on $X$.



[]{}




[]{}



[]{}




[]{}




\end{document}
--->
