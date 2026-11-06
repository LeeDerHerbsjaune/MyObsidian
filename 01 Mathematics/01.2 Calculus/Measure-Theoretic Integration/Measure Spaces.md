---
type: technical-term
title: "Measure Spaces"
aliases:
  - Measure Space
field:
  - Mathematics
subfield:
  - Measure Theory
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - measure-theory
sources:
  - "Folland (1999), Real Analysis: Modern Techniques and Their Applications"
  - "Royden & Fitzpatrick (2010), Real Analysis"
related: []
projects: []
---

> [!abstract] Definition
> A **measure space** is a mathematical structure consisting of a set, a σ-algebra of measurable subsets, and a measure that assigns nonnegative sizes to those subsets.
>
> It provides the foundational framework for measure theory and measure-theoretic integration.

## 1. Mathematical Structure

> [!definition] Measure Space
> A measure space is a triple:
>
> $$ (X,\mathcal{F},\mu) $$
>
> where:
> - $X$ is the underlying set.
> - $\mathcal{F}$ is a σ-algebra on $X$.
> - $\mu:\mathcal{F}\rightarrow[0,\infty]$ is a measure.

## 2. σ-Algebras

> [!definition] σ-Algebra
> A collection $\mathcal{F}\subseteq\mathcal{P}(X)$ is a σ-algebra if:
>
> 1. $X\in\mathcal{F}$.
> 2. If $A\in\mathcal{F}$, then $A^c\in\mathcal{F}$.
> 3. If $A_1,A_2,\ldots\in\mathcal{F}$, then:
>
> $$\bigcup_{n=1}^{\infty}A_n\in\mathcal{F}$$
>
> Consequently, σ-algebras are also closed under countable intersections and set differences.

## 3. Measures

> [!definition] Measure
> A function $\mu:\mathcal{F}\rightarrow[0,\infty]$ is a measure if:
>
> - $\mu(\varnothing)=0$.
> - For pairwise disjoint measurable sets $A_n$:
>
> $$\mu\left(\bigcup_{n=1}^{\infty}A_n\right)
> =\sum_{n=1}^{\infty}\mu(A_n)$$
>
> The second property is called **countable additivity**.

## 4. Important Properties

> [!important] Consequences of Countable Additivity
> - Monotonicity: if $A\subseteq B$, then $\mu(A)\leq\mu(B)$.
> - Countable subadditivity:
>
> $$\mu\left(\bigcup_{n=1}^{\infty}A_n\right)
> \leq\sum_{n=1}^{\infty}\mu(A_n)$$
>
> - Continuity from below: if $A_n\uparrow A$, then $\mu(A_n)\rightarrow\mu(A)$.
> - Continuity from above: if $A_n\downarrow A$ and $\mu(A_1)<\infty$, then $\mu(A_n)\rightarrow\mu(A)$.

## 5. Special Measure Spaces

> [!definition] Finite Measure Space
> A measure space is finite if $\mu(X)<\infty$.

> [!definition] Probability Space
> A probability space is a measure space satisfying:
>
> $$\mu(X)=1$$

> [!definition] σ-Finite Measure Space
> A measure space is σ-finite if:
>
> $$X=\bigcup_{n=1}^{\infty}A_n$$
>
> where each $A_n$ is measurable and $\mu(A_n)<\infty$.

> [!definition] Complete Measure Space
> A measure space is complete if every subset of every measure-zero measurable set is measurable.

## 6. Standard Examples

> [!example] Lebesgue Measure
> On $\mathbb{R}^n$, Lebesgue measure generalizes length, area, and volume.

> [!example] Counting Measure
> For a set $A$:
>
> $$\mu(A)=|A|$$
>
> where the value may be infinite.

> [!example] Dirac Measure
> For a fixed point $x_0$:
>
> $$\delta_{x_0}(A)=
> \begin{cases}
> 1,&x_0\in A\\
> 0,&x_0\notin A
> \end{cases}$$

## 7. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Set Theory** — supplies set operations and countable unions.
> - **Topology** — provides Borel σ-algebras and topological measurable structures.

> [!note] Downstream Knowledge
> - **Measurable Sets** — studies the subsets belonging to a σ-algebra.
> - **Measurable Functions** — defines functions compatible with measurable structures.
> - **Measure-Theoretic Integration** — constructs integrals using measures.
> - **Product Measures** — constructs measures on product spaces.