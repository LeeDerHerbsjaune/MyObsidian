---
type: technical-term
title: "Power Series"
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
  - power-series
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **power series** is an infinite series in which each term contains a nonnegative integer power of a variable, multiplied by a coefficient.
>
> Its general form is:
>
> $$\sum_{n=0}^{\infty}c_n(x-a)^n$$
>
> where:
> - $c_n$ is the coefficient of the $n$-th term.
> - $x$ is the independent variable.
> - $a$ is the center of the power series.

## 1. Radius and Interval of Convergence

> [!important] Radius of Convergence
> Every power series has a radius of convergence $R$, where:
>
> $$0\leq R\leq\infty$$
>
> The series:
>
> - Converges absolutely when $|x-a|<R$.
> - Diverges when $|x-a|>R$.
> - Requires separate investigation at $|x-a|=R$.

> [!definition] Interval of Convergence
> The interval of convergence is the set of real values of $x$ for which the power series converges.
>
> Its endpoints must be tested individually because convergence at either endpoint cannot be inferred from the radius alone.

## 2. Determining the Radius

> [!note] Ratio Test
> If the relevant limit exists, the radius can be determined by:
>
> $$R=\lim_{n\to\infty}
> \left|\frac{c_n}{c_{n+1}}\right|$$
>
> provided the expression has a finite or infinite limit and the resulting ratio-test criterion applies.

> [!note] Root Test
> More generally:
>
> $$R=\frac{1}{\limsup_{n\to\infty}\sqrt[n]{|c_n|}}$$
>
> with the conventions:
> - $1/0=\infty$.
> - $1/\infty=0$.

## 3. Properties

> [!important] Differentiation and Integration
> Inside its interval of convergence, a power series can be differentiated and integrated term by term.
>
> If:
>
> $$f(x)=\sum_{n=0}^{\infty}c_n(x-a)^n$$
>
> then:
>
> $$f'(x)=\sum_{n=1}^{\infty}nc_n(x-a)^{n-1}$$
>
> and:
>
> $$\int f(x)\,dx
> =C+\sum_{n=0}^{\infty}
> \frac{c_n}{n+1}(x-a)^{n+1}$$
>
> Both resulting power series have the same radius of convergence as the original series.

> [!important] Uniqueness of Coefficients
> If a function is represented by a power series in a neighborhood of its center, its coefficients are uniquely determined by its derivatives at that center:
>
> $$c_n=\frac{f^{(n)}(a)}{n!}$$
>
> This applies when the function is genuinely represented by that power series near $a$.

## 4. Examples

> [!example] Geometric Power Series
> For $|x|<1$:
>
> $$\frac{1}{1-x}
> =\sum_{n=0}^{\infty}x^n$$
>
> Its radius of convergence is $R=1$.
>
> The series diverges at both endpoints $x=-1$ and $x=1$.

## 5. Limitations

> [!warning] Convergence Does Not Guarantee Representation
> A power series defines a function within its interval of convergence. However, an arbitrary function need not equal its Taylor series, even if derivatives of all orders exist.
>
> The equality between a function and its Taylor series requires additional conditions.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Sequences:** Power-series coefficients form a sequence.
- **Series:** A power series is a particular type of infinite series.
- **Convergence and Divergence:** Determines where the series defines a finite value.
- **Tests for Convergence:** Provides methods for finding the radius and endpoint behavior.

### Downstream Knowledge
- **Taylor Series:** A power series whose coefficients are determined by derivatives of a function.
- **Maclaurin Series:** A Taylor series centered at zero.
- **Differential Equations:** Power-series solutions are used to solve certain differential equations.
- **Complex Analysis:** Develops power series as representations of analytic functions.