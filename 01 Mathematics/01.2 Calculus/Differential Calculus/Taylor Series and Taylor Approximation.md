---
type: technical-term
title: "Taylor Series and Taylor Approximation"
aliases:
  - Taylor Expansion
  - Taylor Polynomial
  - Taylor Approximation
  - Chuỗi Taylor
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Differential Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - series
  - approximation
sources: []
related: []
projects: []
---

# Taylor Series and Taylor Approximation

> [!abstract] Definition
> Taylor Series and Taylor Approximation describe methods of representing and approximating functions using polynomial expressions constructed from derivatives at a specified expansion point.
>
> Taylor polynomials provide finite-order approximations, while Taylor series represent infinite expansions whose convergence properties determine whether they reproduce the original function.

## 1. Taylor Polynomial

> [!definition] Definition
> A Taylor polynomial of degree $n$ centered at $a$ is a polynomial constructed using the function's derivatives evaluated at $a$.

$$
T_n(x)=
\sum_{k=0}^{n}
\frac{f^{(k)}(a)}{k!}(x-a)^k
$$

Expanded form:

$$
T_n(x)=f(a)+f'(a)(x-a)
+\frac{f''(a)}{2!}(x-a)^2+\cdots
$$

## 2. Taylor Series

> [!definition] Definition
> A Taylor series is the infinite power series associated with the derivatives of a function at an expansion point.

$$
\sum_{k=0}^{\infty}
\frac{f^{(k)}(a)}{k!}(x-a)^k
$$

> [!important] Convergence
> The existence of derivatives of every order does not guarantee that the Taylor series converges to the original function.
>
> Equality requires appropriate convergence and remainder conditions.

## 3. Maclaurin Series

> [!definition] Definition
> A Maclaurin series is a Taylor series centered at zero.

$$
f(x)=
\sum_{k=0}^{\infty}
\frac{f^{(k)}(0)}{k!}x^k
$$

### Common Maclaurin Expansions

> [!example] Exponential Function

$$
e^x=
1+x+\frac{x^2}{2!}
+\frac{x^3}{3!}+\cdots
$$

> [!example] Sine Function

$$
\sin x=
x-\frac{x^3}{3!}
+\frac{x^5}{5!}-\cdots
$$

> [!example] Cosine Function

$$
\cos x=
1-\frac{x^2}{2!}
+\frac{x^4}{4!}-\cdots
$$

## 4. Taylor Remainder

> [!definition] Definition
> The remainder represents the difference between a function and its Taylor polynomial.

$$
R_n(x)=f(x)-T_n(x)
$$

### Lagrange Remainder

> [!important] Lagrange Form
> Under the appropriate differentiability assumptions, the remainder can be expressed as:

$$
R_n(x)=
\frac{f^{(n+1)}(\xi)}{(n+1)!}
(x-a)^{n+1}
$$

where $\xi$ lies between $a$ and $x$.

## 5. Approximation Error

> [!info] Error
> The absolute approximation error is:

$$
E_n(x)=|f(x)-T_n(x)|
$$

The remainder provides a framework for estimating or bounding this error.

## 6. Order of Approximation

> [!note] Local Approximation
> A higher-degree Taylor polynomial generally incorporates more derivative information.
>
> However, higher degree does not automatically guarantee a smaller error everywhere. Approximation quality depends on the function, expansion point, and evaluation interval.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Supplies the derivative values used to construct Taylor polynomials.
- **Higher-Order Derivatives:** Provides successive derivatives for polynomial coefficients.
- **Sequences and Series:** Provides the convergence theory for infinite expansions.
- **Limits:** Establishes the mathematical framework for convergence and remainder analysis.

### Downstream Knowledge
- **Power Series:** Generalizes the study of infinite polynomial expansions.
- **Numerical Analysis:** Uses polynomial approximations for numerical computation.
- **Differential Equations:** Uses series expansions to construct solutions to certain differential equations.
- **Multivariable Calculus:** Generalizes Taylor expansions to functions of multiple variables.

## 8. References

- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.
- Rudin, Walter (1976). *Principles of Mathematical Analysis*. 3rd Edition.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.