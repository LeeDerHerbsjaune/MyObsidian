---
type: technical-term
title: "Fractional Derivatives"
aliases:
  - Derivatives of Fractional Order
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
> **Fractional derivatives** generalize ordinary differentiation to non-integer orders. They define differentiation operators of arbitrary real or, in some formulations, complex order.
>
> Unlike ordinary derivatives, many fractional derivatives are nonlocal: evaluating the derivative at a point can depend on the function over an interval or an entire domain.

> [!important] General Concept
> For an integer $n$, ordinary differentiation is represented by
>
> $$
> \frac{d^n f(x)}{dx^n}
> $$
>
> Fractional calculus extends the order to $\alpha\in\mathbb{R}^+$:
>
> $$
> D^\alpha f(x)
> $$
>
> However, there is no single universally accepted definition of a fractional derivative. Different definitions impose different mathematical properties, boundary conditions, and interpretations.

> [!note] Main Definitions
> Important fractional derivative formulations include:
>
> - **Riemann–Liouville derivative:** constructs differentiation using an ordinary derivative applied after fractional integration.
> - **Caputo derivative:** applies fractional integration to an ordinary derivative.
> - **Grünwald–Letnikov derivative:** defines fractional differentiation through a generalized finite-difference limit.
> - **Riesz fractional derivative:** defines a symmetric, nonlocal operator, commonly through Fourier transforms.
>
> These definitions are related but generally not equivalent.

> [!important] Nonlocality
> An ordinary derivative is local in the sense that it depends on the behavior of a function arbitrarily close to the evaluation point.
>
> Many fractional derivatives instead involve weighted contributions from a region of the function's domain.
>
> This property is often associated with memory effects in time-dependent models and spatial interactions over a range of distances.

> [!note] Fractional Derivative of a Power Function
> For the Riemann–Liouville derivative, under the usual conditions,
>
> $$
> D_{0+}^{\alpha}x^\beta
> =
> \frac{\Gamma(\beta+1)}
> {\Gamma(\beta-\alpha+1)}
> x^{\beta-\alpha}
> $$
>
> This expression is valid when the involved Gamma functions and operator are well-defined. Special parameter values require separate interpretation.

> [!warning] Important Distinctions
> - Different definitions can produce different results for the same function.
> - The derivative of a constant is not necessarily zero under every definition.
> - Initial conditions for fractional differential equations depend on the selected derivative.
> - The ordinary derivative semigroup property does not generally extend to arbitrary fractional derivatives.
> - Boundary terminals and domain assumptions can affect the operator.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Differential Calculus — establishes ordinary differentiation.
> - Fractional Integrals — provides the integral operators used in several derivative definitions.
> - Gamma Function — supports non-integer-order normalization.
> - Real Analysis — establishes the relevant function spaces and convergence conditions.
>
> **Downstream Knowledge**
> - Riemann–Liouville Derivative — a specific fractional derivative definition.
> - Caputo Derivative — a formulation with important initial-value properties.
> - Grünwald–Letnikov Derivative — a difference-based formulation.
> - Riesz Fractional Derivative — a symmetric spatial operator.
> - Fractional Differential Equations — equations involving fractional derivatives.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Podlubny, I. (1999). *Fractional Differential Equations*.