---
type: technical-term
title: "Tests for Convergence"
aliases:
  - Convergence Tests
  - Series Convergence Tests
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
> **Tests for Convergence** are mathematical criteria used to determine whether an infinite series converges or diverges.
>
> They establish convergence without necessarily requiring the exact sum of the series.

## 1. Preliminary Test

> [!important] Divergence Test
> For a series:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> if:
>
> $$\lim_{n\to\infty}a_n\neq0$$
>
> or the limit does not exist, the series diverges.
>
> If the limit is zero, the test is inconclusive.

## 2. Comparison Tests

> [!definition] Direct Comparison Test
> Suppose $0\leq a_n\leq b_n$ for sufficiently large $n$.
>
> - If $\sum b_n$ converges, then $\sum a_n$ converges.
> - If $\sum a_n$ diverges, then $\sum b_n$ diverges.

> [!definition] Limit Comparison Test
> Suppose $a_n>0$ and $b_n>0$ for sufficiently large $n$, and:
>
> $$\lim_{n\to\infty}\frac{a_n}{b_n}=L$$
>
> If $0<L<\infty$, then both series:
>
> $$\sum a_n,\qquad \sum b_n$$
>
> either both converge or both diverge.

## 3. Ratio and Root Tests

> [!definition] Ratio Test
> Define:
>
> $$L=\lim_{n\to\infty}
> \left|\frac{a_{n+1}}{a_n}\right|$$
>
> when the limit exists.
>
> - $L<1$: Absolutely convergent.
> - $L>1$ or $L=\infty$: Divergent.
> - $L=1$: Inconclusive.

> [!definition] Root Test
> Define:
>
> $$L=\limsup_{n\to\infty}\sqrt[n]{|a_n|}$$
>
> - $L<1$: Absolutely convergent.
> - $L>1$: Divergent.
> - $L=1$: Inconclusive.

## 4. Integral Test

> [!definition] Integral Test
> Let $f(x)$ be positive, continuous, and decreasing for $x\geq1$, with $a_n=f(n)$.
>
> Then:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> converges if and only if:
>
> $$\int_1^\infty f(x)\,dx$$
>
> converges.

## 5. Alternating Series Test

> [!definition] Leibniz Test
> Consider:
>
> $$\sum_{n=1}^{\infty}(-1)^{n-1}b_n$$
>
> where $b_n\geq0$.
>
> The series converges if:
>
> 1. $b_{n+1}\leq b_n$ for sufficiently large $n$.
> 2. $\lim_{n\to\infty}b_n=0$.
>
> The test guarantees convergence, not necessarily absolute convergence.

## 6. Absolute Convergence Test

> [!important] Absolute Convergence Criterion
> If:
>
> $$\sum_{n=1}^{\infty}|a_n|$$
>
> converges, then:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> also converges.
>
> This criterion is particularly useful for series containing positive and negative terms.

## 7. Cauchy Condensation Test

> [!definition] Cauchy Condensation Test
> If $(a_n)$ is nonnegative and decreasing, then:
>
> $$\sum_{n=1}^{\infty}a_n$$
>
> converges if and only if:
>
> $$\sum_{k=0}^{\infty}2^k a_{2^k}$$
>
> converges.
>
> It is especially useful for logarithmic and slowly decreasing sequences.

## 8. Strategy for Selecting Tests

> [!tip] Practical Selection
> - Terms do not approach zero: use the divergence test.
> - Terms resemble known positive series: use comparison or limit comparison.
> - Terms contain factorials or exponential expressions: consider the ratio test.
> - Terms contain powers with index-dependent exponents: consider the root test.
> - Terms arise from a decreasing positive function: consider the integral test.
> - Terms alternate in sign: consider the alternating series test.
> - Absolute values produce a manageable positive series: test for absolute convergence.

## 9. Knowledge Relationships

### Foundation Knowledge
- **Sequences:** Provide the limiting concepts underlying convergence.
- **Series:** Defines the objects being tested.
- **Convergence and Divergence:** Establishes the properties and definitions that the tests determine.

### Downstream Knowledge
- **Power Series:** Uses ratio and root tests to determine intervals of convergence.
- **Uniform Convergence:** Requires stronger convergence criteria for function series.
- **Real Analysis:** Develops general convergence theorems and proofs.