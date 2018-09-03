---
title: Vector Norms
---

\renewcommand{\abs}[1]{\lvert #1\rvert}
\renewcommand{\norm}[1]{\lVert #1\rVert}
\renewcommand{\RR}{\mathbf{R}}

DEF! A vector norm is a real valued function $\norm{\cdot}\colon \RR^n \to \RR$ with $3$ properties, namely ... it's positive unless zero, or $\norm{x}\geq 0$ and $\norm{x}= 0$ iff $x=0$; it scales, i.e., $\norm{\alpha x} = \abs{\alpha}\cdot \norm{x}$; and it respects the triangle inequality $\norm{x + y} \leq \norm{x}+\norm{y}$.

DEF! The $l_p$ norms (for $p \in \RR^+$) are given by ... $\norm{x}_p = \sqrt[p]{\sum_{i=1}^n \abs{x_i}^p}$.

FACT! The Holder inequality (of which the Cauchy Bunyakovsky Schwarz inequality is a special case) states ... for all $x,y \in \RR^n$ and $p,q$ such that $\frac1p + \frac1q = 1$ we have $\abs{x^Ty} \leq \norm{x}_p\norm{y}_q$.

DEF! The $l_\infty$ norm is ... $\norm{x}_\infty = \max\{\abs{x_i} : i=1,n\}$.

EXAMPLE! The $l_2$ norm is ... $\norm{x}_2 = \sum_{i=1}^n \abs{x_i}^2 = \sqrt{x^T x}$.

DEF! A matrix norm is a real valued function $\norm{\cdot}\colon \RR^{m\times n} \to \RR$ with $3$ properties, namely ... it's positive unless zero, or $\norm{A}\geq 0$ and $\norm{A}= 0$ iff $A=0$; it scales, i.e., $\norm{\alpha A} = \abs{\alpha}\cdot \norm{A}$; and it respects the triangle inequality $\norm{A + B} \leq \norm{A}+\norm{B}$.

DEF! A matrix norm has the submultiplicative property iff ... $$\forall A \in \RR^{m\times n}\, \forall B \in \RR^{n\times p}\, \norm{AB}\leq\norm{A}\norm{B}.$$

Vector norms induce matrix norms; these are called *natural* matrix norms.

FACT! Some matrix norms guaranteed to have the submultiplicative property are ... those induced by $l_p$ vector norms.

EX! The matrix norm given by the max column sum of magnitudes is ... the $l_1$ matrix norm.

EX! The matrix norm given by the max row sum of magnitudes is ... the $l_\infty$ matrix norm.

EX! Turns out that the scalar $\max_i\{\sqrt{\lambda_i}: \lambda_i \text{ is an eigenvalue of } A^T A\}$ is given by ... $\norm{A}_2$, the spectral norm.

DEF! Given a vector norm, the induced matrix norm is ... $$\norm{A} = \sup_{x\neq 0} \frac{\norm{Ax}}{\norm{x}}.$$
