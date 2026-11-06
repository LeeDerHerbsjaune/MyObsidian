---
type: technical-term
title: "Convergence and Divergence"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - convergence
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Convergence and Divergence** describe the limiting behavior of sequences and infinite series.
>
> Convergence means approaching a finite limit. Divergence means that no finite limit exists.

## 1. Sequence Convergence

> [!definition] Convergent Sequence
> A sequence $(a_n)$ converges to $L$ if:
>
> $$\lim_{n\to\infty}a_n=L$$
>
> Formally:
>
> $$\forall\varepsilon>0,\ \exists N:
> n\geq N\implies |a_n-L|<\varepsilon$$
>
> A sequence diverges if it does not approach any finite real limit.

## 2. Series Convergence

> [!definition] Convergent Series
> A series converges when its partial-sum sequence converges:
>
> $$\sum_{n=1}^{\infty}a_n=S$$
>
> if and only if:
>
> $$\lim_{N\to\infty}\sum_{n=1}^{N}a_n=S$$

> [!warning] Term Test for Divergence
> If:
>
> $$\lim_{n\to\infty}a_n\neq0$$
>
> or the limit does not exist, then:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> diverges.
>
> If the limit equals zero, no conclusion can be made from this test alone.

## 3. Absolute and Conditional Convergence

> [!definition] Absolute Convergence
> A series converges absolutely if:
>
> $$\sum_{n=1}^{\infty}|a_n|$$
>
> converges.
>
> Absolute convergence implies ordinary convergence.

> [!definition] Conditional Convergence
> A series converges conditionally if:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> converges, but:
>
> $$\sum_{n=1}^{\infty}|a_n|$$
>
> diverges.

> [!important] Absolute Convergence Theorem
> Every absolutely convergent real or complex series is convergent.
>
> Conditional convergence is possible because positive and negative terms can cancel.

## 4. Cauchy Criterion for Series

> [!important] Cauchy Criterion
> A series $\sum a_n$ converges if and only if, for every $\varepsilon>0$, there exists $N$ such that:
>
> $$\left|\sum_{k=m}^{n}a_k\right|<\varepsilon$$
>
> whenever $n\geq m\geq N$.
>
> This criterion expresses convergence through the behavior of series tails.

## 5. Important Properties

> [!note] Convergent Sequences
> - Every convergent sequence is bounded.
> - Every subsequence of a convergent sequence has the same limit.
> - Every bounded monotone real sequence converges.

> [!note] Convergent Series
> - A convergent series has terms approaching zero.
> - A convergent series remains convergent after changing or removing finitely many terms.
> - Absolute convergence is stronger than ordinary convergence.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Sequences:** The basic objects whose limits define convergence.
- **Series:** The partial sums of a series form a sequence.
- **Limits:** Provide the formal mathematical definition.

### Downstream Knowledge
- **Tests for Convergence:** Develops practical criteria for determining convergence.
- **Power Series:** Requires convergence analysis at different values of the variable.
- **Uniform Convergence:** Extends convergence theory to sequences and series of functions.
- **Real Analysis:** Establishes rigorous general convergence theorems.