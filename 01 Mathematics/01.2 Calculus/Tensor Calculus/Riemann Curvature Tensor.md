---
type: technical-term
title: "Riemann Curvature Tensor"
aliases:
  - Riemann Tensor
  - Riemann Curvature
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Tensor Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - tensor-calculus
sources:
  - "Lee (2018), Introduction to Riemannian Manifolds"
  - "do Carmo (1992), Riemannian Geometry"
related: []
projects: []
---

> [!abstract] Definition
> The **Riemann curvature tensor** measures the curvature associated with a connection on a manifold.
>
> It describes the failure of covariant derivatives to commute and the infinitesimal path dependence of parallel transport.

> [!important] Operator Definition
> For vector fields $X,Y,Z$, define
>
> $$R(X,Y)Z
> =
> \nabla_X\nabla_YZ
> -\nabla_Y\nabla_XZ
> -\nabla_{[X,Y]}Z$$
>
> where $[X,Y]$ is the Lie bracket of $X$ and $Y$.
>
> This definition is independent of the coordinate system.

> [!note] Coordinate Components
> Using the convention
>
> $$R(\partial_k,\partial_l)\partial_j
> =R^i{}_{jkl}\partial_i$$
>
> the components are
>
> $$R^i{}_{jkl}
> =
> \partial_k\Gamma^i_{lj}
> -\partial_l\Gamma^i_{kj}
> +\Gamma^i_{km}\Gamma^m_{lj}
> -\Gamma^i_{lm}\Gamma^m_{kj}$$
>
> Sign conventions differ between references. Always check the definition used before comparing formulas.

> [!note] Covariant Form
> Lowering the first index using the metric gives
>
> $$R_{ijkl}=g_{im}R^m{}_{jkl}$$
>
> This form is commonly used in Riemannian geometry.

> [!important] Symmetries
> For the Levi-Civita connection, the fully covariant Riemann tensor satisfies
>
> **Antisymmetry in the first pair**
>
> $$R_{ijkl}=-R_{jikl}$$
>
> **Antisymmetry in the second pair**
>
> $$R_{ijkl}=-R_{ijlk}$$
>
> **Pair symmetry**
>
> $$R_{ijkl}=R_{klij}$$
>
> **First Bianchi identity**
>
> $$R_{ijkl}+R_{iklj}+R_{iljk}=0$$
>
> These identities reduce the number of independent curvature components.

> [!note] Flatness
> A connection is flat if its Riemann curvature tensor vanishes:
>
> $$R^i{}_{jkl}=0$$
>
> For a Levi-Civita connection, this means the Riemannian manifold has zero intrinsic curvature.

> [!warning] Coordinate Coefficients Versus Curvature
> Christoffel symbols can be nonzero in flat space because they depend on coordinates.
>
> The Riemann curvature tensor is a genuine tensor. Its vanishing or nonvanishing is coordinate-independent.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Covariant Derivatives — defines the differential operation whose commutator produces curvature.
> - Christoffel Symbols — provides the coordinate representation of a connection.
> - Tensor Fields — provides the geometric setting.
>
> **Downstream Knowledge**
> - Ricci Tensor — obtained by contracting the Riemann tensor.
> - Scalar Curvature — obtained by contracting the Ricci tensor.
> - Riemannian Geometry — studies curvature as a central geometric property.
> - Holonomy — relates curvature to parallel transport around loops.