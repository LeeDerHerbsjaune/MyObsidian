---
type: technical-term
title: "Index Raising and Lowering"
aliases:
  - Raising and Lowering Indices
  - Metric Duality
field:
  - Mathematics
subfield:
  - Tensor Calculus
  - Riemannian Geometry
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - tensor-calculus
sources:
  - "Schutz (1980), Geometrical Methods of Mathematical Physics"
  - "Lee (2018), Introduction to Riemannian Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> **Index raising and lowering** are operations that convert covariant tensor indices into contravariant indices, and vice versa, using a nondegenerate metric tensor.
>
> These operations establish an isomorphism between a vector space and its dual space.

> [!important] Lowering an Index
> Let $g_{ij}$ be a nondegenerate metric tensor and $v^i$ a contravariant vector.
>
> The corresponding covector is
>
> $$v_i=g_{ij}v^j$$

> [!important] Raising an Index
> Let $g^{ij}$ denote the inverse metric, satisfying
>
> $$g^{ik}g_{kj}=\delta^i_j$$
>
> A covector $\omega_j$ can be converted into a vector:
>
> $$\omega^i=g^{ij}\omega_j$$

> [!note] General Tensor Indices
> The metric can raise or lower any tensor index.
>
> For example:
>
> $$T^i{}_j=g^{ik}T_{kj}$$
>
> $$T_{ij}=g_{ik}T^k{}_j$$
>
> The tensor's numerical components change, but the underlying geometric object is related through the metric isomorphism.

> [!example] Euclidean Space
> In Cartesian coordinates with the standard Euclidean metric,
>
> $$g_{ij}=\delta_{ij}$$
>
> Therefore, raising and lowering indices does not change the numerical values of the components.
>
> This special case can make the distinction between vectors and covectors appear less significant than it is in general coordinates or non-Euclidean geometries.

> [!warning] Metric Dependence
> Raising and lowering indices require a nondegenerate metric.
>
> Without such a metric, there is no canonical identification of a vector space with its dual space.
>
> A degenerate bilinear form does not provide an invertible metric map.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Metric Tensor — supplies the metric and its inverse.
> - Dual Vector Spaces — establishes the relationship between vectors and covectors.
> - Tensors — provides the tensor structures being transformed.
>
> **Downstream Knowledge**
> - Ricci Tensor — allows curvature indices to be contracted using the inverse metric.
> - Scalar Curvature — uses metric contraction.
> - Riemannian Geometry — uses metric duality throughout its geometric structure.