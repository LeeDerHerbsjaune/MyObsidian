---
type: technical-term
title: "Grünwald–Letnikov Derivative"
aliases:
  - Grünwald–Letnikov Fractional Derivative
abbreviation: GL Derivative
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
  - "Podlubny (1999), Fractional Differential Equations"
related: []
projects: []
---

> [!abstract] Definition
> The **Grünwald–Letnikov derivative** defines fractional differentiation through the limiting behavior of generalized finite differences.
>
> It extends the ordinary finite-difference representation of derivatives by replacing integer binomial coefficients with generalized binomial coefficients.

> [!important] Mathematical Formulation
> The left-sided Grünwald–Letnikov derivative is commonly expressed as
>
> $$
> D_{a+}^{\alpha}f(x)
> =
> \lim_{h\to0^+}
> \frac{1}{h^\alpha}
> \sum_{k=0}^{\lfloor(x-a)/h\rfloor}
> (-1)^k
> \binom{\alpha}{k}
> f(x-kh)
> $$
>
> where:
> - $\alpha>0$ is the fractional order.
> - $h$ is the step size.
> - $\lfloor(x-a)/h\rfloor$ determines the finite summation range.
> - The generalized binomial coefficient is
>
>   $$
>   \binom{\alpha}{k}
>   =
>   \frac{\Gamma(\alpha+1)}
>   {\Gamma(k+1)\Gamma(\alpha-k+1)}
>   $$

> [!note] Generalized Finite Differences
> For an integer order $n$, the finite-difference expression becomes the familiar representation of an $n$-th derivative in the limit.
>
> The Grünwald–Letnikov definition extends this construction to non-integer orders.

> [!important] Properties
> - The definition is based on a limiting process.
> - It uses generalized binomial coefficients.
> - It is naturally connected to discrete approximations.
> - Under suitable assumptions, it is equivalent to Riemann–Liouville formulations.
> - Its numerical discretization can be constructed directly from the finite-difference sum.

> [!example] First-Order Case
> For $\alpha=1$,
>
> $$
> D_{a+}^{1}f(x)
> =
> \lim_{h\to0^+}
> \frac{f(x)-f(x-h)}{h}
> $$
>
> This is the ordinary left-sided derivative when the limit exists.

> [!warning] Limitations
> - The existence of the limiting expression requires suitable regularity.
> - Numerical approximations can involve long summations because fractional operators are nonlocal.
> - Discretization errors depend on the step size and the regularity of the function.
> - Equivalence with other definitions requires appropriate assumptions and compatible terminals.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Derivatives — provides the general operator framework.
> - Finite Differences — provides the discrete differentiation structure.
> - Gamma Function — defines generalized binomial coefficients.
>
> **Downstream Knowledge**
> - Numerical Methods for Fractional Calculus — develops discrete approximations.
> - Fractional Differential Equations — uses Grünwald–Letnikov operators in analytical and numerical formulations.
> - Properties of Fractional Operators — establishes conditions for equivalence with other definitions.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Podlubny, I. (1999). *Fractional Differential Equations*.