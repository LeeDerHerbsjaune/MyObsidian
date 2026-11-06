---
type: technical-term
title: "Tensor Types and Ranks"
aliases:
  - Tensor Valence
  - Tensor Order
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
  - "Bishop & Goldberg (1968), Tensor Analysis on Manifolds"
  - "Lee (2018), Introduction to Riemannian Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> The **type of a tensor** specifies the number of contravariant and covariant slots it possesses.
>
> A tensor of type $(r,s)$ belongs to
>
> $$V^{\otimes r}\otimes(V^*)^{\otimes s}$$
>
> where:
> - $r$ is the contravariant rank.
> - $s$ is the covariant rank.
>
> The total tensor order is $r+s$.

> [!important] Contravariant and Covariant Slots
> - **Contravariant slots** correspond to factors of the vector space $V$.
> - **Covariant slots** correspond to factors of the dual space $V^*$.
>
> The distinction determines how tensor components transform under a change of coordinates.

> [!note] Common Tensor Types
> | Tensor | Type | Total order |
> |---|---:|---:|
> | Scalar | $(0,0)$ | 0 |
> | Vector | $(1,0)$ | 1 |
> | Covector | $(0,1)$ | 1 |
> | Linear operator | $(1,1)$ | 2 |
> | Bilinear form | $(0,2)$ | 2 |
> | Contravariant rank-2 tensor | $(2,0)$ | 2 |
> | Mixed rank-3 tensor | $(2,1)$ | 3 |

> [!note] Component Notation
> A tensor of type $(r,s)$ is represented by components
>
> $$T^{i_1\cdots i_r}_{j_1\cdots j_s}$$
>
> Upper indices represent contravariant slots, while lower indices represent covariant slots.

> [!important] Tensor Rank Versus Matrix Rank
> Tensor order and matrix rank are different concepts.
>
> - **Tensor order** counts the number of tensor slots.
> - **Matrix rank** is the dimension of the image of a linear transformation represented by a matrix.
>
> A rank-2 tensor does not necessarily have matrix rank 2.

> [!warning] Terminological Variation
> The word *rank* is used inconsistently across mathematical literature.
>
> In tensor calculus, it often refers to the total number of tensor indices, also called tensor order or valence. In linear algebra, matrix rank has a different meaning.
>
> Use the pair $(r,s)$ whenever the distinction between covariant and contravariant slots matters.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensors — establishes the tensor-product definition.
> - Vector Spaces — provides the underlying spaces.
> - Dual Vector Spaces — explains covariant slots.
>
> **Downstream Knowledge**
> - Tensor Components and Transformation Laws — derives component transformations from tensor type.
> - Index Raising and Lowering — changes tensor type using a metric.
> - Tensor Contraction — reduces tensor order.