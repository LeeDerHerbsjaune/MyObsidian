---
type: technical-term
title: "Riesz Fractional Derivative"
aliases:
  - Riesz Derivative
  - Riesz Fractional Operator
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
  - "Kwaśnicki (2017), Ten Equivalent Definitions of the Fractional Laplace Operator"
related: []
projects: []
---

> [!abstract] Definition
> The **Riesz fractional derivative** is a symmetric, nonlocal fractional differentiation operator. It is commonly defined on the real line or Euclidean space through Fourier transforms.
>
> Unlike left-sided and right-sided fractional derivatives, the Riesz operator treats spatial directions symmetrically.

> [!important] Fourier-Space Definition
> For $0<\alpha<2$, one common convention defines the one-dimensional Riesz derivative by
>
> $$
> \mathcal{F}
> \left[
> \frac{d^\alpha f}{d|x|^\alpha}
> \right](\xi)
> =
> -|\xi|^\alpha\widehat{f}(\xi)
> $$
>
> where:
> - $\mathcal{F}$ denotes the Fourier transform.
> - $\widehat{f}(\xi)$ is the Fourier transform of $f$.
> - $\xi$ is the frequency variable.
>
> The negative sign is part of this common convention. Normalization and sign conventions should be checked when comparing references.

> [!note] Relation to the Fractional Laplacian
> In $\mathbb{R}^n$, the fractional Laplacian is defined through
>
> $$
> \mathcal{F}\left[(-\Delta)^s f\right](\boldsymbol{\xi})
> =
> |\boldsymbol{\xi}|^{2s}
> \widehat{f}(\boldsymbol{\xi}),
> \qquad 0<s<1
> $$
>
> Under the common convention above, the Riesz derivative of order $\alpha=2s$ corresponds to
>
> $$
> -(-\Delta)^s f
> $$
>
> in one dimension. The term *Riesz derivative* is used with different conventions in the literature, so its exact definition must be stated.

> [!important] Singular Integral Representation
> For $0<\alpha<2$, the fractional Laplacian can also be represented as
>
> $$
> (-\Delta)^{\alpha/2}f(x)
> =
> C_{n,\alpha}\,
> \operatorname{PV}
> \int_{\mathbb{R}^n}
> \frac{f(x)-f(y)}
> {|x-y|^{n+\alpha}}\,dy
> $$
>
> where:
> - $C_{n,\alpha}$ is a normalization constant.
> - $\operatorname{PV}$ denotes the Cauchy principal value.
> - $|x-y|$ is the Euclidean distance.
>
> This representation makes the nonlocal interaction between spatial points explicit.

> [!important] Properties
> - **Translation invariance:** on the whole Euclidean space, the operator commutes with translations.
> - **Symmetry:** its spatial definition does not privilege a left or right direction.
> - **Nonlocality:** the operator depends on values of the function away from the evaluation point.
> - **Fourier multiplier:** its action becomes multiplication by a power of the frequency magnitude.
> - **Connection to fractional Laplacians:** it provides a fundamental representation of isotropic fractional spatial operators.

> [!warning] Limitations
> - The operator requires suitable function-space or distributional assumptions.
> - The singular integral requires an appropriate principal-value interpretation.
> - Definitions on bounded domains require additional choices, such as boundary conditions or an extension outside the domain.
> - The Riesz derivative should not be confused with the Riesz potential, which is a fractional integration operator.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Derivatives — provides the general theory of non-integer differentiation.
> - Fourier Analysis — provides the frequency-domain definition.
> - Partial Differential Equations — supplies the operator framework in spatial domains.
> - Real Analysis — provides the function-space and singular-integral foundations.
>
> **Downstream Knowledge**
> - Fractional PDEs — uses Riesz-type spatial operators.
> - Fractional Laplacian — develops the multidimensional nonlocal operator.
> - Fractional Sobolev Spaces — provides the natural functional setting for many fractional Laplacian problems.
> - Nonlocal Analysis — studies operators whose values depend on spatially separated points.

> [!quote] References
> - Samko, S. G., Kilbas, A. A., and Marichev, O. I. (1993). *Fractional Integrals and Derivatives: Theory and Applications*.
> - Kwaśnicki, M. (2017). *Ten Equivalent Definitions of the Fractional Laplace Operator*. Fractional Calculus and Applied Analysis, 20, 7–51.