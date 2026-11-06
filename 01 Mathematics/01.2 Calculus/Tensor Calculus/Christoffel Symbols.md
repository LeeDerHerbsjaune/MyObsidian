---
type: technical-term
title: "Christoffel Symbols"
aliases:
  - Connection Coefficients
  - Christoffel Symbols of the Second Kind
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
> **Christoffel symbols** are coordinate coefficients that describe a connection on a manifold relative to a chosen coordinate basis.
>
> They appear in the coordinate expression of covariant derivatives and encode how the coordinate basis vectors vary from point to point.

> [!important] Definition Through a Connection
> For a connection $\nabla$ and coordinate basis vectors $\partial_i=\partial/\partial x^i$, define
>
> $$\nabla_{\partial_i}\partial_j
> =
> \Gamma^k_{ij}\partial_k$$
>
> The coefficients $\Gamma^k_{ij}$ are the Christoffel symbols in that coordinate chart.

> [!note] Levi-Civita Christoffel Symbols
> For the Levi-Civita connection associated with a metric $g_{ij}$, the coefficients are
>
> $$\Gamma^k_{ij}
> =
> \frac{1}{2}g^{k\ell}
> \left(
> \frac{\partial g_{j\ell}}{\partial x^i}
> +
> \frac{\partial g_{i\ell}}{\partial x^j}
> -
> \frac{\partial g_{ij}}{\partial x^\ell}
> \right)$$
>
> This formula follows from metric compatibility and zero torsion.

> [!note] Symmetry
> For a torsion-free connection in a coordinate basis,
>
> $$\Gamma^k_{ij}=\Gamma^k_{ji}$$
>
> In particular, the Levi-Civita connection is torsion-free.

> [!note] Covariant Derivative of a Vector
> For a vector field $V=V^i\partial_i$,
>
> $$\nabla_jV^i
> =
> \partial_jV^i+\Gamma^i_{jk}V^k$$
>
> The Christoffel term accounts for the variation of the coordinate basis.

> [!warning] Christoffel Symbols Are Not Tensor Components
> Christoffel symbols do not generally transform according to the tensor transformation law.
>
> Their transformation includes an additional second-derivative term from the coordinate transformation.
>
> Consequently, Christoffel symbols are coordinate-dependent connection coefficients, not tensor components.

> [!important] Geometric Interpretation
> Christoffel symbols describe how the coordinate basis changes under differentiation.
>
> They can be nonzero even in flat Euclidean space when curvilinear coordinates are used. Their nonzero values alone do not imply intrinsic curvature.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Metric Tensor — determines the Levi-Civita connection.
> - Tensor Fields — provides the fields being differentiated.
> - Coordinate Systems — defines the local coordinate basis.
>
> **Downstream Knowledge**
> - Covariant Derivatives — use Christoffel symbols to differentiate tensor components.
> - Parallel Transport — is described by differential equations involving connection coefficients.
> - Riemann Curvature Tensor — is constructed from connection coefficients and their derivatives.