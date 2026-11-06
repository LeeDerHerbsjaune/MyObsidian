---
type: technical-term
title: "Taylor Series"
aliases:
  - Taylor Expansion
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
  - taylor-series
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **Taylor series** is an infinite power series constructed from the derivatives of a function evaluated at a specified point.
>
> It provides a method for representing or approximating a function locally using polynomial terms.

## 1. Mathematical Formulation

> [!important] Taylor Series
> For a function $f$ with derivatives of all orders at $x=a$, its Taylor series centered at $a$ is:
>
> $$\sum_{n=0}^{\infty}
> \frac{f^{(n)}(a)}{n!}(x-a)^n$$
>
> Expanded:
>
> $$f(a)+f'(a)(x-a)
> +\frac{f''(a)}{2!}(x-a)^2+\cdots$$
>
> where $f^{(n)}(a)$ denotes the $n$-th derivative evaluated at the center.

## 2. Taylor Polynomials

> [!definition] Taylor Polynomial
> The Taylor polynomial of degree $N$ is the finite truncation of the Taylor series:
>
> $$T_N(x)=\sum_{n=0}^{N}
> \frac{f^{(n)}(a)}{n!}(x-a)^n$$
>
> It approximates the function near the expansion point.

## 3. Taylor's Theorem and Remainder

> [!important] Taylor's Theorem
> If $f$ has sufficiently many derivatives on an interval containing $a$ and $x$, then:
>
> $$f(x)=T_N(x)+R_N(x)$$
>
> where $R_N(x)$ is the remainder or approximation error.
>
> One form of the Lagrange remainder is:
>
> $$R_N(x)=
> \frac{f^{(N+1)}(\xi)}{(N+1)!}
> (x-a)^{N+1}$$
>
> for some $\xi$ between $a$ and $x$, under the theorem's differentiability assumptions.

> [!important] Convergence to the Function
> A function equals its Taylor series at $x$ if:
>
> $$\lim_{N\to\infty}R_N(x)=0$$
>
> Having derivatives of all orders does not by itself guarantee this condition.

## 4. Taylor Series and Approximation

> [!note] Local Approximation
> Taylor polynomials approximate a function using information about its derivatives at the expansion point.
>
> Lower-degree terms describe local behavior:
> - Constant term: function value.
> - Linear term: local slope.
> - Quadratic term: local curvature.
> - Higher-order terms: increasingly detailed local behavior.

> [!example] Exponential Function
> The Taylor series of $e^x$ centered at $a=0$ is:
>
> $$e^x=1+x+\frac{x^2}{2!}
> +\frac{x^3}{3!}+\cdots$$
>
> This expansion converges to $e^x$ for every real $x$.


## 5. Important Properties

> [!note] Differentiation
> Within its interval of convergence, a Taylor power series can be differentiated term by term.

> [!note] Integration
> Within its interval of convergence, a Taylor power series can be integrated term by term.

> [!warning] Smoothness Versus Analyticity
> A function is smooth if it has derivatives of all orders.
>
> A function is analytic at a point if it equals its Taylor series in some neighborhood of that point.
>
> Analyticity is a stronger condition than smoothness.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Differentiation:** Taylor coefficients are constructed from derivatives.
- **Sequences and Series:** Taylor expansions are infinite series.
- **Power Series:** Provides the mathematical structure of Taylor expansions.
- **Convergence and Divergence:** Determines whether the expansion converges.

### Downstream Knowledge
- **Maclaurin Series:** The special case centered at zero.
- **Approximation Theory:** Develops polynomial approximation and error analysis.
- **Numerical Analysis:** Uses Taylor expansions for numerical approximation and error estimation.
- **Differential Equations:** Uses Taylor expansions in series-based solution methods.
- **Complex Analysis:** Connects Taylor expansions to analytic functions.