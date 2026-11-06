---
type: technical-term
title: Measurable Sets
aliases:
  - Measurable Subsets
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
  - Folland (1999), Real Analysis
  - Royden & Fitzpatrick (2010), Real Analysis
related:
projects: []
---

> [!abstract] Definition
> A **measurable set** is a subset of a measure space that belongs to its designated σ-algebra.
>
> Measurability determines which subsets can consistently be assigned a measure.

## 1. Formal Definition

> [!definition] Measurable Set
> Given a measurable space $(X,\mathcal{F})$, a subset $A\subseteq X$ is measurable if:
>
> $$A\in\mathcal{F}$$
>
> Its measure $\mu(A)$ is then defined by the measure associated with the space.

## 2. Closure Properties

> [!important] σ-Algebra Properties
> If $A,B,A_n$ are measurable, then:
>
> - $A^c$ is measurable.
> - $A\cup B$ and $A\cap B$ are measurable.
> - $A\setminus B$ is measurable.
> - $\bigcup_{n=1}^{\infty}A_n$ is measurable.
> - $\bigcap_{n=1}^{\infty}A_n$ is measurable.
>
> These properties allow measurable sets to be manipulated using countable set operations.

## 3. Borel Sets

> [!definition] Borel Set
> The Borel σ-algebra on a topological space $X$ is the smallest σ-algebra containing every open subset of $X$:
>
> $$\mathcal{B}(X)=\sigma(\text{open subsets of }X)$$
>
> On $\mathbb{R}$, it contains open sets, closed sets, intervals, and all sets obtainable from them through countable unions, intersections, and complements.

## 4. Lebesgue Measurable Sets

> [!definition] Lebesgue Measurability
> A subset of $\mathbb{R}^n$ is Lebesgue measurable if it belongs to the Lebesgue σ-algebra, which is the completion of the Borel σ-algebra under Lebesgue measure.
>
> This completion includes every subset of a Lebesgue measure-zero set.

## 5. Null Sets

> [!definition] Null Set
> A measurable set $N$ is a null set if:
>
> $$\mu(N)=0$$
>
> Null sets may contain infinitely many points and need not be empty.

> [!important] Almost-Everywhere Statements
> A property holds almost everywhere if the set where it fails is contained in a measurable null set.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Set Theory** — provides the language of subsets and set operations.
> - **Measure Spaces** — supplies the σ-algebra defining measurability.

> [!note] Downstream Knowledge
> - **Measurable Functions** — uses measurable preimages of sets.
> - **Lebesgue Integral** — integrates functions defined on measurable spaces.
> - **Almost-Everywhere Convergence** — describes convergence outside null sets.