---
type: technical-term
title: "Fractional PDEs"
aliases:
  - Fractional Partial Differential Equations
  - Fractional-Order Partial Differential Equations
field:
  - Mathematics
subfield:
  - Fractional Calculus
  - Partial Differential Equations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - fractional-calculus
  - partial-differential-equations
sources:
  - "Luchko and Gorenflo (1998), An Operational Method for Solving Fractional Differential Equations"
  - "Kwaśnicki (2017), Ten Equivalent Definitions of the Fractional Laplace Operator"
related: []
projects: []
---

> [!abstract] Definition
> **Fractional partial differential equations (fractional PDEs)** are partial differential equations involving fractional-order derivatives or nonlocal operators.
>
> Fractional operators may act on time, spatial coordinates, or both.
>
> They extend classical PDE formulations by allowing non-integer differentiation orders and nonlocal interactions.

> [!important] General Form
> A fractional PDE can be represented abstractly as
>
> $$
> F\left(
> \mathbf{x},t,u,
> D_t^\alpha u,
> D_{x_1}^{\beta_1}u,\ldots,
> D_{x_n}^{\beta_n}u
> \right)=0
> $$
>
> where:
> - $u(\mathbf{x},t)$ is the unknown field.
> - $D_t^\alpha$ is a fractional time derivative.
> - $D_{x_i}^{\beta_i}$ are fractional spatial derivatives.
> - $\alpha$ and $\beta_i$ are fractional orders.
>
> This is an abstract representation; particular equations require specific operator definitions and domains.

> [!note] Time-Fractional PDEs
> A time-fractional diffusion equation may be written as
>
> $$
> {}^C D_t^\alpha u(\mathbf{x},t)
> =
> \kappa\Delta u(\mathbf{x},t),
> \qquad 0<\alpha<1
> $$
>
> where $\kappa>0$ is a diffusion coefficient.
>
> The Caputo derivative introduces a nonlocal dependence on the temporal history of the solution.

> [!note] Space-Fractional PDEs
> A space-fractional diffusion equation may be expressed as
>
> $$
> \frac{\partial u}{\partial t}
> =
> -\kappa(-\Delta)^s u,
> \qquad 0<s<1
> $$
>
> where $(-\Delta)^s$ is the fractional Laplacian.
>
> This operator introduces nonlocal spatial interactions.

> [!important] Space-Time Fractional PDEs
> A model may include both fractional time and spatial operators:
>
> $$
> {}^C D_t^\alpha u
> =
> -\kappa(-\Delta)^s u+f
> $$
>
> where $f$ is a source term.
>
> The temporal and spatial fractional orders represent different mathematical features and must be specified independently.

> [!note] Mathematical Characteristics
> - **Nonlocality in time:** the evolution can depend on the solution's past history.
> - **Nonlocality in space:** the operator can couple distant spatial points.
> - **Boundary dependence:** the definition of spatial operators on bounded domains depends on boundary conditions and operator construction.
> - **Function-space requirements:** weak formulations often require fractional Sobolev spaces or related spaces.
> - **Regularity:** solutions may have weaker smoothness than solutions of corresponding classical PDEs.

> [!important] Analytical Methods
> Common approaches include:
> - Fourier and Laplace transforms.
> - Eigenfunction expansions.
> - Weak and variational formulations.
> - Semigroup and operator methods.
> - Energy estimates.
> - Fixed-point and compactness methods.
>
> These methods depend on the structure of the fractional operator and the geometry of the domain.

> [!note] Numerical Methods
> Common computational approaches include:
> - Finite-difference schemes.
> - Finite-element methods.
> - Spectral methods.
> - Convolution quadrature.
> - Numerical methods for fractional Laplacians.
>
> Nonlocal operators can create dense discrete systems and substantial computational costs.

> [!warning] Scope and Limitations
> - A time-fractional derivative and a space-fractional derivative are not interchangeable.
> - Different definitions of fractional Laplacians can produce different boundary-value problems.
> - Boundary conditions must be consistent with the selected operator.
> - Fractional PDEs do not all share the same existence, uniqueness, or regularity theory.

> [!link] Knowledge Relationships
> **Foundation Knowledge**
> - Fractional Integrals and Derivatives of Several Variables — provides multidimensional fractional operators.
> - Fractional Derivatives — provides the time-fractional and coordinate-wise derivative framework.
> - Partial Differential Equations — provides the classical PDE framework.
> - Functional Analysis — supports operator and weak-solution theory.
> - Fourier Analysis — supports the analysis of translation-invariant spatial operators.
>
> **Downstream Knowledge**
> - Fractional Diffusion Equations — develops diffusion models with fractional operators.
> - Fractional Wave Equations — studies wave-type equations with fractional operators.
> - Fractional Sobolev Spaces — provides function spaces for weak formulations.
> - Numerical Methods for Fractional PDEs — develops computational solution techniques.
> - Nonlocal Analysis — studies the broader class of nonlocal operators.

> [!quote] References
> - Luchko, Y., and Gorenflo, R. (1998). *An Operational Method for Solving Fractional Differential Equations*.
> - Kwaśnicki, M. (2017). *Ten Equivalent Definitions of the Fractional Laplace Operator*. Fractional Calculus and Applied Analysis, 20, 7–51.