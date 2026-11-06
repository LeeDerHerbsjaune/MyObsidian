---
type: technical-term
title: "Caputo Derivative"
aliases:
  - Caputo Fractional Derivative
abbreviation: ""
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
  - "Caputo (1967), Linear Models of Dissipation whose Q is Almost Frequency Independent"
  - "Podlubny (1999), Fractional Differential Equations"
related: []
projects: []
---

> [!abstract] Definition
> The **Caputo derivative** is a fractional differentiation operator that applies fractional integration to an ordinary integer-order derivative.
>
> It is particularly useful in fractional differential equations because its initial conditions can often be expressed using ordinary integer-order derivatives.

> [!important] Mathematical Formulation
> Let $\alpha>0$ and $n=\lceil\alpha\rceil$. The left-sided Caputo derivative is
>
> $$
> {}^{C}D_{a+}^{\alpha}f(x)
> =
> \frac{1}{\Gamma(n-\alpha)}
> \int_a^x
> (x-t)^{n-\alpha-1}f^{(n)}(t)\,dt
> $$
>
> Equivalently,
>
> $$
> {}^{C}D_{a+}^{\alpha}f(x)
> =
> I_{a+}^{n-\alpha}f^{(n)}(x)
> $$
>
> where $f^{(n)}$ is the ordinary $n$-th derivative.

> [!note] Integer-Order Case
> When $\alpha=n$ is an integer, the Caputo derivative reduces to the ordinary $n$-th derivative, under the appropriate interpretation of the limiting definition.

> [!important] Derivative of a Constant
> For a constant function $f(x)=C$,
>
> $$
> {}^{C}D_{a+}^{\alpha}C=0
> $$
>
> whenever the Caputo derivative is defined.

> [!example] Power Function
> For $\beta>n-1$,
>
> $$
> {}^{C}D_{0+}^{\alpha}x^\beta
> =
> \frac{\Gamma(\beta+1)}
> {\Gamma(\beta-\alpha+1)}
> x^{\beta-\alpha}
> $$
>
> For lower integer powers, the Caputo derivative can be zero because the corresponding ordinary $n$-th derivative vanishes.

> [!important] Relation to the Riemann–Liouville Derivative
> Under suitable regularity assumptions,
>
> $$
> {}^{C}D_{a+}^{\alpha}f(x)
> =
> D_{a+}^{\alpha}
> \left[
> f(x)-
> \sum_{k=0}^{n-1}
> \frac{f^{(k)}(a)}{k!}(x-a)^k
> \right]
> $$
>
> This shows that the Caputo derivative removes the initial Taylor polynomial before applying the Riemann–Liouville derivative.

> [!note] Initial Conditions
> For $n-1<\alpha\leq n$, a common initial-value formulation uses
>
> $$
> f(a),f'(a),\ldots,f^{(n-1)}(a)
> $$
>
> These are ordinary initial values, which often make the Caputo formulation convenient for modeling.

> [!warning] Limitations
> - The function must possess the required ordinary derivatives and the fractional integral must exist.
> - The Caputo derivative is generally not identical to the Riemann–Liouville derivative.
> - It does not satisfy every familiar integer-order differentiation rule without additional conditions.
> - The choice of derivative definition must match the intended initial or boundary conditions.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Integrals — the Caputo operator is a fractional integral of an ordinary derivative.
> - Fractional Derivatives — provides the general theory.
> - Differential Calculus — supplies the ordinary derivatives used in its definition.
>
> **Downstream Knowledge**
> - Fractional Differential Equations — commonly uses Caputo derivatives in initial-value problems.
> - Properties of Fractional Operators — studies its relationship with other fractional operators.
> - Fractional PDEs — uses Caputo-type time derivatives in evolution equations.

> [!quote] References
> - Caputo, M. (1967). *Linear Models of Dissipation whose Q is Almost Frequency Independent*.
> - Podlubny, I. (1999). *Fractional Differential Equations*.