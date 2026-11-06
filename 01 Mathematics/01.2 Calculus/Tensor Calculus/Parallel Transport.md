---
type: technical-term
title: "Parallel Transport"
aliases:
  - Parallel Translation
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
> **Parallel transport** is the process of transporting a vector or tensor along a curve on a manifold while requiring its covariant derivative along that curve to vanish.
>
> It provides a connection-dependent way to compare vectors belonging to different tangent spaces.

> [!important] Parallel Transport Equation
> Let $\gamma(t)$ be a smooth curve and $V(t)$ a vector field along it.
>
> The vector field is parallel along $\gamma$ if
>
> $$\frac{DV}{dt}=0$$
>
> In local coordinates,
>
> $$\frac{dV^i}{dt}
> +\Gamma^i_{jk}
> \frac{dx^j}{dt}V^k=0$$
>
> This is a system of linear ordinary differential equations for the components of $V$ along the curve.

> [!note] Geometric Meaning
> Parallel transport preserves the notion of direction determined by the connection.
>
> It does not generally mean that vector components remain constant, because the coordinate basis may vary along the curve.

> [!note] Metric Preservation
> Under a metric-compatible connection, parallel transport preserves inner products.
>
> If $V$ and $W$ are parallel along the same curve, then
>
> $$\frac{d}{dt}g(V,W)=0$$
>
> Consequently, their lengths and mutual angle remain constant.

> [!important] Path Dependence
> In curved spaces, parallel transport between two points can depend on the path taken.
>
> Transporting a vector around a closed loop may return it with a different direction. This phenomenon is closely related to curvature and holonomy.

> [!warning] Dependence on the Connection
> Parallel transport is defined by a connection, not by a metric alone.
>
> A metric determines a unique Levi-Civita connection, but other connections can define different parallel transport rules.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Covariant Derivatives — provides the defining differential operation.
> - Connections — defines differentiation across tangent spaces.
> - Tensor Fields — provides vector and tensor fields along curves.
>
> **Downstream Knowledge**
> - Riemann Curvature Tensor — measures infinitesimal path dependence of parallel transport.
> - Holonomy — studies transformations produced by transport around loops.
> - Geodesics — curves whose tangent vectors are parallel along themselves under an affine parametrization.