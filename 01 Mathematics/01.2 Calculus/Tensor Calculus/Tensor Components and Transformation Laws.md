---
type: technical-term
title: "Tensor Components and Transformation Laws"
aliases:
  - Tensor Transformation Law
  - Transformation of Tensor Components
field:
  - Mathematics
subfield:
  - Tensor Calculus
  - Differential Geometry
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
> **Tensor components** are the numerical coefficients representing a tensor relative to a chosen basis or coordinate system.
>
> A **tensor transformation law** specifies how these components change when the basis or coordinates change, while preserving the underlying tensor.

> [!note] Vector Transformation
> Let $x^i$ and $x'^i$ denote two coordinate systems. A contravariant vector transforms as
>
> $$V'^i=\frac{\partial x'^i}{\partial x^j}V^j$$
>
> The Jacobian matrix determines the transformation of its components.

> [!note] Covector Transformation
> A covector transforms according to
>
> $$\omega'_i=\frac{\partial x^j}{\partial x'^i}\omega_j$$
>
> This transformation is inverse to the contravariant transformation.

> [!important] General Tensor Transformation Law
> A tensor of type $(r,s)$ transforms according to
>
> $$T'^{i_1\cdots i_r}_{j_1\cdots j_s}
> =
> \frac{\partial x'^{i_1}}{\partial x^{a_1}}
> \cdots
> \frac{\partial x'^{i_r}}{\partial x^{a_r}}
> \frac{\partial x^{b_1}}{\partial x'^{j_1}}
> \cdots
> \frac{\partial x^{b_s}}{\partial x'^{j_s}}
> T^{a_1\cdots a_r}_{b_1\cdots b_s}$$
>
> Each upper index contributes a Jacobian factor, and each lower index contributes an inverse-Jacobian factor.

> [!note] Coordinate Invariance
> Although the components change between coordinate systems, the tensor itself remains unchanged.
>
> Scalar quantities obtained by valid tensor contractions are also invariant under coordinate transformations.

> [!example] Vector and Covector Pairing
> Let $V^i$ be a vector and $\omega_i$ a covector. Their contraction is
>
> $$\omega_iV^i$$
>
> Under a coordinate transformation, the Jacobian and inverse-Jacobian factors cancel, leaving the scalar unchanged.

> [!warning] Arrays Are Not Automatically Tensors
> An array of components must satisfy the appropriate transformation law to represent a tensor.
>
> In particular, ordinary partial derivatives of tensor components generally do not transform tensorially. This motivates the introduction of covariant derivatives.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensors — provides the coordinate-independent tensor definition.
> - Tensor Types and Ranks — determines the number and variance of indices.
> - Coordinate Systems — provides the coordinate transformations.
>
> **Downstream Knowledge**
> - Tensor Fields — applies tensor transformations pointwise on manifolds.
> - Covariant Derivatives — constructs a tensorial derivative operation.
> - Differential Geometry — develops coordinate-independent geometric structures.