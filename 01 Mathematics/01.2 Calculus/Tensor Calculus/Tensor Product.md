---
type: technical-term
title: "Tensor Product"
aliases:
  - Tensor Product of Vector Spaces
field:
  - Mathematics
subfield:
  - Linear Algebra
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
  - "Greub (1978), Multilinear Algebra"
  - "Lee (2018), Introduction to Riemannian Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> The **tensor product** is a construction that combines vector spaces or their elements into a new vector space while preserving multilinear relationships.
>
> For vector spaces $V$ and $W$, their tensor product is denoted
>
> $$V\otimes W$$

> [!important] Universal Property
> The tensor product is characterized by a canonical bilinear map
>
> $$\tau:V\times W\rightarrow V\otimes W$$
>
> such that every bilinear map from $V\times W$ into another vector space $U$ factors uniquely through a linear map from $V\otimes W$ to $U.
>
> This property makes tensor products a natural algebraic representation of bilinear operations.

> [!note] Tensor Product of Elements
> For $v\in V$ and $w\in W$, their tensor product is written
>
> $$v\otimes w$$
>
> The operation is bilinear:
>
> $$ (av_1+bv_2)\otimes w
> =a(v_1\otimes w)+b(v_2\otimes w)$$
>
> $$v\otimes(aw_1+bw_2)
> =a(v\otimes w_1)+b(v\otimes w_2)$$

> [!note] Basis and Dimension
> If $\{e_i\}$ and $\{f_j\}$ are bases of finite-dimensional vector spaces $V$ and $W$, then
>
> $$\{e_i\otimes f_j\}$$
>
> forms a basis of $V\otimes W$.
>
> Therefore,
>
> $$\dim(V\otimes W)=\dim(V)\dim(W)$$

> [!note] Tensor Products of Tensors
> If
>
> $$S\in V^{\otimes r}\otimes(V^*)^{\otimes s}$$
>
> and
>
> $$T\in V^{\otimes p}\otimes(V^*)^{\otimes q}$$
>
> then their tensor product has type
>
> $$(r+p,s+q)$$
>
> The tensor product combines their slots without contracting any indices.

> [!example] Vector Outer Product
> For vectors $u,v\in\mathbb{R}^n$, their tensor product has components
>
> $$(u\otimes v)^{ij}=u^iv^j$$
>
> It produces a rank-2 contravariant tensor.

> [!warning] Tensor Product Versus Dot Product
> The tensor product preserves both tensor factors and increases tensor order.
>
> The inner product or contraction pairs compatible arguments and reduces tensor order. These operations are mathematically distinct.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Vector Spaces — supplies the spaces being combined.
> - Linear Transformations — clarifies the universal property.
> - Multilinear Algebra — provides the algebraic foundation.
>
> **Downstream Knowledge**
> - Tensors — tensor spaces are constructed from tensor products.
> - Tensor Contraction — pairs compatible tensor slots.
> - Tensor Algebra — develops operations on tensor products.