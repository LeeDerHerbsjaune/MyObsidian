---
type: technical-term
title: "Tensor Fields"
aliases:
  - Tensor Field
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
  - "Lee (2012), Introduction to Smooth Manifolds"
  - "Lee (2018), Introduction to Riemannian Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> A **tensor field** assigns a tensor to every point of a differentiable manifold, with the assignment varying smoothly when the field is smooth.
>
> A tensor field of type $(r,s)$ on a manifold $M$ is a section of the tensor bundle
>
> $$T^r_sM
> =
> \underbrace{TM\otimes\cdots\otimes TM}_{r}
> \otimes
> \underbrace{T^*M\otimes\cdots\otimes T^*M}_{s}$$
>
> More precisely, it is a smooth section of this bundle.

> [!important] Pointwise Tensor Structure
> At each point $p\in M$, a tensor field assigns a tensor
>
> $$T_p\in T^r_s(T_pM)$$
>
> where $T_pM$ is the tangent space and $T_p^*M$ is the cotangent space at $p$.
>
> The tensor field therefore combines pointwise multilinear algebra with the smooth structure of the manifold.

> [!note] Examples
> | Tensor field | Type |
> |---|---|
> | Scalar field | $(0,0)$ |
> | Vector field | $(1,0)$ |
> | Covector field | $(0,1)$ |
> | Metric tensor field | $(0,2)$ |
> | Endomorphism field | $(1,1)$ |

> [!note] Local Components
> In local coordinates, a tensor field can be expressed as
>
> $$T=T^{i_1\cdots i_r}_{j_1\cdots j_s}
> \frac{\partial}{\partial x^{i_1}}\otimes\cdots\otimes
> \frac{\partial}{\partial x^{i_r}}
> \otimes
> dx^{j_1}\otimes\cdots\otimes dx^{j_s}$$
>
> The component functions vary with position.

> [!important] Smoothness
> A smooth tensor field has component functions that are smooth in every coordinate chart.
>
> Smoothness ensures that differential operations, including covariant differentiation, can be meaningfully defined.

> [!warning] Tensor Versus Tensor Field
> A tensor is an algebraic object at a particular vector space or point.
>
> A tensor field is a spatially varying assignment of tensors over a manifold.
>
> The distinction is analogous to the difference between a vector and a vector field.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensors — defines the pointwise algebraic objects.
> - Differential Manifolds — provides tangent and cotangent spaces.
> - Smooth Maps — provides the smooth structure required for tensor fields.
>
> **Downstream Knowledge**
> - Metric Tensor — defines a distinguished covariant tensor field.
> - Covariant Derivatives — differentiates tensor fields.
> - Riemann Curvature Tensor — defines curvature through a connection.