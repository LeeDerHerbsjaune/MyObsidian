---
type: technical-term
title: "Riemann–Liouville Derivative"
aliases:
  - Riemann–Liouville Fractional Derivative
abbreviation: RL Derivative
field:
  - Mathematics
subfield:
  - Fractional Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - fractional-calculus
sources:
  - "Samko, Kilbas, and Marichev (1993), Fractional Integrals and Derivatives"
related: []
projects: []
---

> [!abstract] Definition
> The **Riemann–Liouville derivative** is a fractional differentiation operator constructed by first applying a fractional integral and then taking an ordinary integer-order derivative.
>
> It is one of the classical definitions of fractional differentiation.

> [!important] Mathematical Formulation
> Let $\alpha>0$ and $n=\lceil\alpha\rceil$. The left-sided Riemann–Liouville derivative is
>
> $$
> D_{a+}^{\alpha}f(x)
> =
> \frac{d^n}{dx^n}
> \left[
> \frac{1}{\Gamma(n-\alpha)}
> \int_a^x
> (x-t)^{n-\alpha-1}f(t)\,dt
> \right]
> $$
>
> Equivalently,
>
> $$
> D_{a+}^{\alpha}f(x)
> =
> \frac{d^n}{dx^n}I_{a+}^{n-\alpha}f(x)
> $$
>
> where $I_{a+}^{n-\alpha}$ is the Riemann–Liouville fractional integral.

> [!note] Integer-Order Case
> When $\alpha=n$ is an integer, the definition reduces to the ordinary $n$-th derivative, with the fractional integral of order zero interpreted as the identity operator.

> [!important] Derivative of a Power Function
> For suitable $\beta$ and $\alpha$,
>
> $$
> D_{0+}^{\alpha}x^\beta
> =
> \frac{\Gamma(\beta+1)}
> {\Gamma(\beta-\alpha+1)}
> x^{\beta-\alpha}
> $$
>
> The formula is understood through the Gamma function and the domain of the operator. If the denominator has a Gamma-function pole, the corresponding reciprocal Gamma factor is interpreted as zero where the analytic continuation applies.

> [!example] Derivative of a Constant
> For $f(x)=1$ and $0<\alpha<1$,
>
> $$
> D_{0+}^{\alpha}1
> =
> \frac{x^{-\alpha}}{\Gamma(1-\alpha)}
> $$
>
> Therefore, the Riemann–Liouville derivative of a constant is generally not zero.

> [!important] Properties
> - The operator is linear when the involved derivatives exist.
> - It is defined through a fractional integral followed by ordinary differentiation.
> - It depends on the lower terminal $a$.
> - Its derivative of a constant is generally nonzero.
> - Its natural initial data often involve fractional integrals or fractional derivatives rather than only ordinary integer-order derivatives.

> [!warning] Limitations
> - Initial conditions can be less intuitive than ordinary initial-value conditions.
> - The derivative may be singular near the lower terminal.
> - The operator's existence depends on the regularity and integrability of the function.
> - It is not interchangeable with the Caputo derivative.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Integrals — the operator is defined using a fractional integral.
> - Fractional Derivatives — provides the general framework.
> - Gamma Function — appears in the normalization and power-function formula.
>
> **Downstream Knowledge**
> - Properties of Fractional Operators — studies its algebraic and analytical properties.
> - Fractional Differential Equations — uses this derivative to define fractional-order equations.
> - Fractional Integral Equations — related through integral representations of differential equations.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Podlubny, I. (1999). *Fractional Differential Equations*.