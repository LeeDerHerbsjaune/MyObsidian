---
type: technical-term
title: "Metric Tensor"
aliases:
  - Riemannian Metric
  - Metric Field
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
> A **metric tensor** is a symmetric, nondegenerate covariant tensor of type $(0,2)$ on a manifold.
>
> A Riemannian metric is additionally positive-definite.
>
> At each point $p$ of a manifold $M$, the metric defines a bilinear map
>
> $$g_p:T_pM\times T_pM\rightarrow\mathbb{R}$$

> [!important] Metric Properties
> A Riemannian metric satisfies:
>
> **Symmetry**
>
> $$g(u,v)=g(v,u)$$
>
> **Positive definiteness**
>
> $$g(v,v)>0 \quad \text{for }v\neq0$$
>
> **Bilinearity**
>
> $$g(au+bv,w)=ag(u,w)+bg(v,w)$$
>
> A pseudo-Riemannian metric preserves symmetry and nondegeneracy but does not require positive definiteness.

> [!note] Coordinate Representation
> In local coordinates, the metric is represented by components $g_{ij}$:
>
> $$g=g_{ij}\,dx^i\otimes dx^j$$
>
> For a tangent vector
>
> $$v=v^i\frac{\partial}{\partial x^i}$$
>
> its squared length is
>
> $$\|v\|^2=g_{ij}v^iv^j$$

> [!note] Inverse Metric
> The inverse metric has components $g^{ij}$ satisfying
>
> $$g^{ik}g_{kj}=\delta^i_j$$
>
> It is used to raise indices and perform metric contractions.

> [!note] Geometric Quantities
> The metric determines:
> - Lengths of tangent vectors.
> - Angles between tangent vectors.
> - Inner products.
> - Lengths of curves.
> - Riemannian volume elements.
>
> It also determines a unique torsion-free, metric-compatible connection: the Levi-Civita connection.

> [!warning] Metric Versus Connection
> A metric and a connection are different geometric structures.
>
> A metric defines inner products on tangent spaces. A connection defines differentiation of vector fields in different tangent spaces.
>
> A metric determines a unique Levi-Civita connection, but general connections need not arise from a metric.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensor Fields — provides the setting for a smoothly varying metric.
> - Inner Product Spaces — supplies the pointwise algebraic structure.
> - Differential Geometry — provides the manifold framework.
>
> **Downstream Knowledge**
> - Index Raising and Lowering — uses the metric and inverse metric.
> - Christoffel Symbols — expresses the Levi-Civita connection in coordinates.
> - Riemann Curvature Tensor — measures curvature associated with a connection.
> - Ricci Tensor and Scalar Curvature — are obtained from Riemann curvature using contraction and the metric.