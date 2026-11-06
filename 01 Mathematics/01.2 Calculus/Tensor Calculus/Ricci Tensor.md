---
type: technical-term
title: "Ricci Tensor"
aliases:
  - Ricci Curvature Tensor
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
> The **Ricci tensor** is a symmetric covariant rank-2 tensor obtained by contracting the Riemann curvature tensor.
>
> It captures a particular trace of the full curvature information of a Riemannian manifold.

> [!important] Definition
> Under the convention
>
> $$R^i{}_{jkl}$$
>
> for the Riemann curvature components, define
>
> $$\operatorname{Ric}_{jl}=R^i{}_{jil}$$
>
> This is a contraction of the first and third indices.
>
> Other sign and index conventions exist, so the defining curvature convention must be stated.

> [!note] Symmetry
> For the Levi-Civita connection,
>
> $$\operatorname{Ric}_{ij}=\operatorname{Ric}_{ji}$$
>
> The Ricci tensor is therefore a symmetric covariant tensor of type $(0,2)$.

> [!note] Geometric Interpretation
> The Ricci tensor describes curvature information obtained by tracing the Riemann curvature tensor.
>
> It is closely related to the behavior of volume under geodesic spreading and to averaged curvature in tangent directions.

> [!note] Ricci Curvature in a Direction
> Given a tangent vector $v$, the Ricci curvature in that direction is
>
> $$\operatorname{Ric}(v,v)$$
>
> For a unit vector $v$, it can be interpreted as the trace of sectional curvature over planes containing $v$.

> [!important] Relation to Scalar Curvature
> Contracting the Ricci tensor with the inverse metric produces scalar curvature:
>
> $$R=g^{ij}\operatorname{Ric}_{ij}$$
>
> The Ricci tensor retains directional information, whereas scalar curvature summarizes its metric trace.

> [!warning] Information Loss
> The Ricci tensor does not contain all the information in the Riemann curvature tensor in general dimensions.
>
> In dimensions greater than three, the Weyl curvature tensor captures additional curvature information not determined by the Ricci tensor alone.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Riemann Curvature Tensor — supplies the curvature tensor being contracted.
> - Tensor Contraction — performs the required index contraction.
> - Metric Tensor — provides the geometric setting and index operations.
>
> **Downstream Knowledge**
> - Scalar Curvature — contracts the Ricci tensor.
> - Einstein Tensor — combines the Ricci tensor and scalar curvature.
> - Ricci Flow — evolves a Riemannian metric according to its Ricci curvature.