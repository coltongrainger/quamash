---
title: Topology 2
author: Colton Grainger
date: 2019-01-13
revised:
---

$\require{AMScd}$

## MATH 6220 Syllabus

Instructor: [Dr. Agnès Beaudry](https://sites.google.com/view/agnesbeaudry)

Website: <https://sites.google.com/view/agnesbeaudry/teaching/spring-2019/math-6220>

Git Repo: <http://github.com/coltongrainger/fy19alg2>. 

> Continuation of [MATH 6210](top1). Topics covered will be homology, cohomology and some applications. 

### Prelim exam topics

- singular homology
- the Eilenberg-Steenrod axioms
- homology group of spheres
- the degree of a map between spheres
- homology calculations via CW complexes
- proof of homotopy invariance
- proof of excision
- universal coefficient 
- Kunneth Theorem

### Textbooks

- Topology and Geometry, Glen E. Bredon [@Bre93]
- Algebraic Topology, A. Hatcher [@Hat02]
- A Concise Course in Algebraic Topology, J. Peter May [@May99]

### Problem sets

From the [syllabus](https://drive.google.com/file/d/1bPOnqftRnfLxF4UrC44a1NZQMoZHE0tF/view):

> Problems sets will be posted to a [restricted dropbox] and discussed in class during a problem session, which will be approximately every two weeks. We will cover as many problems as we can during problem sessions. For a problem: 
> 
> - One student will be chosen to present the solution in class and lead the discussion on that problem.
> - A different student will be chosen to write-up the solution (typeset using LATEX). Solutions (.tex and .pdf files) are due via email by 1 pm the day of the class following the problem session.
>
> Tentative dates for the problem sessions: Jan 30, Feb 13, Feb 27, Mar 13, Apr 3, Apr 17, and possibly May 1.

### Grading

measure | weigh
--- | ---
presentations | 40%
write-ups | 30%
participation | 10%
final exam | 20%

# Spring semester

*Preface*. I have tried to talk myself out of keeping notes:

- I have no comparative advantage to narrate the development of homology/cohomology.
    - For example, Dr. Beaudry is live-TeXing her lecture notes, and [extensive references](https://math.stackexchange.com/a/1560607/469856) for algebraic topology notes are already listed on stackexchange. 
- When considering Philip Guo's [heuristic](http://pgbovine.net/writings.htm) when deciding what to write 
  > Will at least 100 people care about this topic three years from now?
  I suspect the answer is yes, in general---It is unlikely, however, that at least 100 people will care about my hot-take on the topic.
- My preferred markup language is pandoc markdown, rendered here with MathJax, which has [limited support](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference) for [commutative diagrams](http://www.jmilne.org/not/Mamscd.pdf).

\begin{CD}
A     @>a>>  B\\
@VVbV        @VVcV\\
C     @>d>>  D
\end{CD}

<a href="http://presheaf.com/?d=d2c2h1p4y36n27141x6g1b5r5i16n3j"><img src="http://presheaf.com/cache/d2c2h1p4y36n27141x6g1b5r5i16n3j.png" title="click to go to presheaf.com for editing"/></a>

In this

## Week 1

### Pre-requisites 

It's good to have seen

- point-set topology up to the Baire category theorem
- the statement of Seifert van-Kampen
- group actions on covering spaces
- singular homology (informally)

