---
type: technical-term
title: "Scalar Curvature"
aliases:
  - Ricci Scalar
  - Scalar Ricci Curvature
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
> **Scalar curvature** is a scalar-valued geometric quantity obtained by taking the metric trace of the Ricci tensor.
>
> It summarizes a particular average of the sectional curvature information at each point of a Riemannian manifold.

> [!important] Mathematical Definition
> Let $\operatorname{Ric}_{ij}$ be the Ricci tensor and $g^{ij}$ the inverse metric.
>
> Scalar curvature is
>
> $$R=g^{ij}\operatorname{Ric}_{ij}$$
>
> It is a tensor contraction that produces a scalar field.

> [!note] Relation to the Riemann Tensor
> Scalar curvature can also be expressed as a double contraction of the fully covariant Riemann curvature tensor:
>
> $$R=g^{ik}g^{jl}R_{ijkl}$$
>
> The exact index arrangement depends on the adopted curvature convention.

> [!note] Geometric Interpretation
> Scalar curvature describes an aggregate measure of curvature at a point.
>
> With the common convention in which a sphere has positive curvature:
> - Positive scalar curvature indicates positive average curvature in the relevant trace.
> - Negative scalar curvature indicates negative average curvature.
> - Zero scalar curvature indicates that the trace vanishes.
>
> Zero scalar curvature does not necessarily imply that the full Riemann curvature tensor vanishes.

> [!example] Constant Sectional Curvature
> In an $n$-dimensional Riemannian manifold with constant sectional curvature $K$,
>
> $$\operatorname{Ric}_{ij}=(n-1)Kg_{ij}$$
>
> Therefore,
>
> $$R=n(n-1)K$$

> [!important] Dimension Dependence
> In two dimensions, scalar curvature determines the Gaussian curvature up to the conventional factor:
>
> $$R=2K$$
>
> In dimensions greater than two, scalar curvature alone does not determine the full curvature tensor.

> [!warning] Scalar Curvature Versus Flatness
> A zero scalar curvature does not imply a flat manifold.
>
> Flatness requires the entire Riemann curvature tensor to vanish:
>
> $$R^i{}_{jkl}=0$$
>
> Scalar curvature only records a contraction of that tensor.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Ricci Tensor — provides the tensor being traced.
> - Metric Tensor — provides the inverse metric for contraction.
> - Tensor Contraction — defines the operation producing the scalar.
>
> **Downstream Knowledge**
> - Einstein Tensor — combines Ricci curvature and scalar curvature.
> - Scalar Curvature Geometry — studies geometric and topological consequences of scalar curvature.
> - Ricci Flow — uses Ricci curvature to evolve geometric metrics.