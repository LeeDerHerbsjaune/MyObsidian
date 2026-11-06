---
type: technical-term
title: "Fractional Integrals"
aliases:
  - Integrals of Fractional Order
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
> **Fractional integrals** generalize ordinary integration to non-integer orders. They define operators that integrate a function by an arbitrary positive real order, rather than only by integer orders.
>
> Unlike ordinary repeated integration, fractional integration is generally represented by an integral kernel that depends on the distance between the evaluation point and the integration variable.

> [!important] Riemann–Liouville Fractional Integral
> The left-sided Riemann–Liouville fractional integral of order $\alpha>0$ is
>
> $$
> (I_{a+}^{\alpha}f)(x)
> =
> \frac{1}{\Gamma(\alpha)}
> \int_a^x (x-t)^{\alpha-1}f(t)\,dt
> $$
>
> where:
> - $\alpha$ is the fractional integration order.
> - $a$ is the lower terminal.
> - $\Gamma(\alpha)$ is the Gamma function.
> - $f(t)$ is the integrand.
>
> The kernel $(x-t)^{\alpha-1}$ determines how values of the function over the interval contribute to the result.

> [!example] Special Cases
> For $\alpha=1$:
>
> $$
> I_{a+}^{1}f(x)=\int_a^x f(t)\,dt
> $$
>
> For $\alpha=2$:
>
> $$
> I_{a+}^{2}f(x)
> =
> \int_a^x\int_a^s f(t)\,dt\,ds
> $$
>
> Thus, fractional integration extends the ordinary concept of repeated integration.

> [!note] Right-Sided Fractional Integral
> A right-sided Riemann–Liouville fractional integral is defined by
>
> $$
> (I_{b-}^{\alpha}f)(x)
> =
> \frac{1}{\Gamma(\alpha)}
> \int_x^b (t-x)^{\alpha-1}f(t)\,dt
> $$
>
> The left-sided and right-sided operators differ in their integration direction and terminal.

> [!important] Properties
> - **Linearity**
>
>   $$
>   I^\alpha(af+bg)=aI^\alpha f+bI^\alpha g
>   $$
>
> - **Semigroup property**
>
>   Under suitable integrability assumptions,
>
>   $$
>   I^\alpha I^\beta f=I^{\alpha+\beta}f
>   $$
>
> - **Identity at order zero**
>
>   The operator is conventionally extended by $I^0f=f$.
>
> - **Nonlocality**
>
>   The value at $x$ depends on function values throughout the interval $[a,x]$, not only on the behavior near $x$.

> [!warning] Conditions and Limitations
> - The integral must exist for the selected function and order.
> - The semigroup property requires appropriate function-space and integrability conditions.
> - Fractional integrals are generally not inverse operators to every definition of fractional derivative without additional terms or conditions.
> - The lower terminal $a$ is part of the operator's definition and affects its result.

> [!example] Power Function
> For $\beta>-1$ and $\alpha>0$,
>
> $$
> I_{0+}^{\alpha}x^\beta
> =
> \frac{\Gamma(\beta+1)}
> {\Gamma(\beta+\alpha+1)}
> x^{\beta+\alpha}
> $$
>
> This formula generalizes the ordinary integration rule for power functions.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Integral Calculus — provides the ordinary integration framework.
> - Gamma Function — generalizes factorials and appears in fractional-order normalization.
> - Real Analysis — provides the function-space and integrability foundations.
>
> **Downstream Knowledge**
> - Fractional Derivatives — fractional differentiation operators are commonly constructed using fractional integration.
> - Fractional Integral Equations — use fractional integral operators as part of their defining equations.
> - Fractional Differential Equations — fractional integrals are used in their integral formulations.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Oldham, K. B., and Spanier, J. (1974). *The Fractional Calculus*.