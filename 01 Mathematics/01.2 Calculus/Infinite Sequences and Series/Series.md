---
type: technical-term
title: "Series"
aliases:
  - Infinite Series
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
  - infinite-series
sources: []
related: []
projects: []
---

> [!abstract] Definition
> An **infinite series** is the sum of the terms of an infinite sequence.
>
> Given a sequence $(a_n)$, its series is:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> A series is studied through its sequence of partial sums.

## 1. Partial Sums

> [!definition] Partial Sum
> The $N$-th partial sum of a series is:
>
> $$S_N=\sum_{n=1}^{N}a_n$$
>
> The partial sums form a new sequence:
>
> $$S_1,S_2,S_3,\ldots$$
>
> The behavior of this sequence determines whether the original series converges.

## 2. Convergence of a Series

> [!important] Definition
> An infinite series converges to $S$ if its partial sums approach a finite limit:
>
> $$\lim_{N\to\infty}S_N=S$$
>
> Otherwise, the series diverges.

## 3. Important Types of Series

> [!definition] Geometric Series
> A geometric series has a constant ratio between consecutive terms:
>
> $$\sum_{n=0}^{\infty}ar^n$$
>
> It converges if $|r|<1$, with sum:
>
> $$S=\frac{a}{1-r}$$
>
> It diverges if $|r|\geq1$.

> [!definition] Harmonic Series
> The harmonic series is:
>
> $$\sum_{n=1}^{\infty}\frac{1}{n}$$
>
> It diverges, despite its terms approaching zero.

> [!definition] Alternating Series
> An alternating series has terms that alternate in sign, commonly expressed as:
>
> $$\sum_{n=1}^{\infty}(-1)^{n-1}b_n$$
>
> where $b_n\geq0$.

> [!definition] Telescoping Series
> A telescoping series is one in which consecutive terms cancel when partial sums are expanded.
>
> For example:
>
> $$\sum_{n=1}^{\infty}
> \left(\frac{1}{n}-\frac{1}{n+1}\right)$$
>
> Its partial sums reduce to:
>
> $$S_N=1-\frac{1}{N+1}$$
>
> Therefore, its sum is $1$.

## 4. Important Properties

> [!important] Linearity
> If $\sum a_n=A$ and $\sum b_n=B$ both converge, then:
>
> $$\sum_{n=1}^{\infty}(ca_n+db_n)=cA+dB$$
>
> for constants $c,d$.

> [!warning] Necessary Condition
> If a series converges, then:
>
> $$\lim_{n\to\infty}a_n=0$$
>
> However, the converse is false. A term approaching zero does not guarantee convergence.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Sequences:** Series are constructed from sequences.
- **Limits:** Series convergence is defined using limits of partial sums.

### Downstream Knowledge
- **Convergence and Divergence:** Establishes the conditions under which a series has a finite sum.
- **Tests for Convergence:** Provides methods for determining series convergence.
- **Power Series:** Generalizes numerical series to variable-dependent series.
- **Taylor Series:** Uses infinite series to represent functions.