---
type: technical-term
title: "Maclaurin Series"
aliases:
  - Maclaurin Expansion
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
  - maclaurin-series
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **Maclaurin series** is a special case of a Taylor series whose expansion center is zero.
>
> It represents a function through the values of its derivatives at $x=0$.

## 1. Mathematical Formulation

> [!important] Maclaurin Series
> For a function $f$ with derivatives of all orders at zero, its Maclaurin series is:
>
> $$\sum_{n=0}^{\infty}
> \frac{f^{(n)}(0)}{n!}x^n$$
>
> Expanded:
>
> $$f(0)+f'(0)x+
> \frac{f''(0)}{2!}x^2+\cdots$$

## 2. Common Maclaurin Expansions

> [!example] Exponential Function
> $$e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$$
>
> This series converges for every real $x$.

> [!example] Sine Function
> $$\sin x=
> \sum_{n=0}^{\infty}
> \frac{(-1)^n x^{2n+1}}{(2n+1)!}$$
>
> This series converges for every real $x$.

> [!example] Cosine Function
> $$\cos x=
> \sum_{n=0}^{\infty}
> \frac{(-1)^n x^{2n}}{(2n)!}$$
>
> This series converges for every real $x$.

> [!example] Geometric Function
> $$\frac{1}{1-x}
> =\sum_{n=0}^{\infty}x^n$$
>
> This equality holds for $|x|<1$.

> [!example] Natural Logarithm
> $$\ln(1+x)=
> \sum_{n=1}^{\infty}
> \frac{(-1)^{n+1}x^n}{n}$$
>
> This equality holds for $-1<x\leq1$.

> [!example] Inverse Tangent
> $$\arctan x=
> \sum_{n=0}^{\infty}
> \frac{(-1)^n x^{2n+1}}{2n+1}$$
>
> This equality holds for $-1\leq x\leq1$.

## 3. Properties

> [!important] Special Relationship
> A Maclaurin series is a Taylor series centered at zero:
>
> $$a=0$$
>
> Therefore, every Maclaurin series is a Taylor series, but not every Taylor series is a Maclaurin series.

> [!note] Approximation
> A finite Maclaurin polynomial is obtained by truncating the infinite expansion:
>
> $$M_N(x)=\sum_{n=0}^{N}
> \frac{f^{(n)}(0)}{n!}x^n$$
>
> Its accuracy generally improves near zero as additional terms are included, provided the expansion converges appropriately.

> [!warning] Convergence
> The existence of all derivatives at zero does not guarantee that a function equals its Maclaurin series.
>
> The convergence of the series and its equality to the original function must be established separately.

## 4. Knowledge Relationships

### Foundation Knowledge
- **Taylor Series:** Maclaurin series is its zero-centered special case.
- **Differentiation:** Determines the expansion coefficients.
- **Power Series:** Provides the infinite-series representation.
- **Tests for Convergence:** Determines convergence intervals and endpoint behavior.

### Downstream Knowledge
- **Approximation Theory:** Uses Maclaurin polynomials for approximation.
- **Numerical Analysis:** Applies truncated expansions in numerical algorithms.
- **Differential Equations:** Uses Maclaurin expansions to construct solutions.