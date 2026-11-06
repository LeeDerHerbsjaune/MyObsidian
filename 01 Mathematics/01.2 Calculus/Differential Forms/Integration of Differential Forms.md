---
type: technical-term
title: "Integration of Differential Forms"
aliases:
  - Integration on Manifolds
  - Integration of Forms
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Differential Topology
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
sources:
  - "Spivak (1965), Calculus on Manifolds"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> **Integration of differential forms** is the operation of integrating a differential $k$-form over an oriented $k$-dimensional manifold or submanifold.
>
> If $M$ is an oriented $k$-dimensional manifold and $\omega\in\Omega^k(M)$, then
>
> $$\int_M\omega$$
>
> is a scalar.

> [!important] Integration Through Parametrization
> Let
>
> $$\phi:U\subseteq\mathbb{R}^k\rightarrow M$$
>
> be an orientation-compatible parametrization.
>
> The integral is computed by pulling the form back to the parameter domain:
>
> $$\int_M\omega=\int_U\phi^*\omega$$
>
> The pullback produces a top-degree form on $U$, which can be integrated using ordinary multiple integration.

> [!note] Coordinate Expression
> If
>
> $$\phi^*\omega=f(u^1,\ldots,u^k)
> du^1\wedge\cdots\wedge du^k$$
>
> then
>
> $$\int_M\omega
> =
> \int_U f(u^1,\ldots,u^k)
> \,du^1\cdots du^k$$
>
> for an orientation-compatible parametrization.

> [!important] Orientation
> Integration of differential forms depends on orientation.
>
> Reversing the orientation changes the sign:
>
> $$\int_{-M}\omega=-\int_M\omega$$
>
> This is a fundamental distinction from integrating scalar densities without orientation.

> [!note] Dimension Matching
> A $k$-form is naturally integrated over a $k$-dimensional oriented manifold.
>
> A form of a different degree cannot be directly integrated over that manifold using the standard differential-form integral.

> [!note] Coordinate Invariance
> Pullback and the transformation law of differential forms ensure that the integral does not depend on the chosen orientation-compatible parametrization.

> [!warning] Differential Forms Versus Scalar Integration
> A differential form already contains the appropriate alternating structure for integration.
>
> A metric is not required to define the integral of a top-degree form. A metric is needed for metric-dependent volume forms and related constructions, but not for integration itself.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Differential Forms — provides the integrands.
> - Pullback — transfers forms to parameter domains.
> - Orientation — determines the sign convention.
> - Multivariable Integration — provides the local integration procedure.
>
> **Downstream Knowledge**
> - Generalized Stokes' Theorem — relates integration to exterior differentiation.
> - De Rham Cohomology — connects integration with global topology.