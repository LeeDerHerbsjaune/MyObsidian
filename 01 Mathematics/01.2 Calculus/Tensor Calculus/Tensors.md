---
type: technical-term
title: "Tensors"
aliases:
  - Tensor
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
> A **tensor** is a multilinear mathematical object that generalizes scalars, vectors, and linear maps. Tensors provide a coordinate-independent way to represent multilinear relationships between vectors and covectors.
>
> A tensor of type $(r,s)$ on a finite-dimensional vector space $V$ is an element of
>
> $$T \in V^{\otimes r}\otimes (V^*)^{\otimes s}$$
>
> where:
> - $V$ is the vector space.
> - $V^*$ is its dual space.
> - $r$ is the number of contravariant slots.
> - $s$ is the number of covariant slots.

> [!important] Core Interpretation
> A tensor can be understood as a multilinear map
>
> $$T:\underbrace{V^*\times\cdots\times V^*}_{r}
> \times
> \underbrace{V\times\cdots\times V}_{s}
> \rightarrow \mathbb{R}$$
>
> The tensor accepts $r$ covectors and $s$ vectors and returns a scalar.
>
> This interpretation is equivalent to the tensor-product representation in finite-dimensional vector spaces.

> [!note] Examples of Tensors
> | Tensor | Type |
> |---|---|
> | Scalar | $(0,0)$ |
> | Vector | $(1,0)$ |
> | Covector | $(0,1)$ |
> | Bilinear form | $(0,2)$ |
> | Linear operator | $(1,1)$ |
> | Metric tensor | $(0,2)$ |

> [!note] Tensor Components
> Given a basis $\{e_i\}$ of $V$ and its dual basis $\{\varepsilon^j\}$, a tensor can be expanded as
>
> $$T=T^{i_1\cdots i_r}_{j_1\cdots j_s}
> e_{i_1}\otimes\cdots\otimes e_{i_r}
> \otimes
> \varepsilon^{j_1}\otimes\cdots\otimes\varepsilon^{j_s}$$
>
> The coefficients $T^{i_1\cdots i_r}_{j_1\cdots j_s}$ are its components in that basis.
>
> Components depend on the chosen basis, while the tensor itself does not.

> [!important] Coordinate Independence
> A tensor is not merely a multidimensional array of numbers.
>
> Its components must transform according to a specific transformation law when the basis or coordinates change. This transformation behavior ensures that the represented object remains geometrically or algebraically consistent.

> [!note] Fundamental Operations
> Tensor algebra includes:
> - Tensor addition.
> - Scalar multiplication.
> - Tensor products.
> - Tensor contraction.
> - Symmetrization and antisymmetrization.
> - Index raising and lowering when a suitable nondegenerate metric is available.

> [!warning] Important Distinction
> Not every array of numbers is a tensor. An array represents tensor components only if it obeys the appropriate transformation law.
>
> Similarly, the ordinary partial derivatives of tensor components do not generally transform as tensor components.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Linear Algebra — provides vector spaces, dual spaces, multilinear maps, and tensor products.
> - Dual Vector Spaces — provides the covariant structure used in tensor definitions.
>
> **Downstream Knowledge**
> - Tensor Fields — assigns tensors to points of a manifold.
> - Tensor Product — constructs higher-order tensors.
> - Tensor Contraction — reduces tensor order by pairing compatible indices.
> - Tensor Calculus — develops differentiation and geometric operations involving tensors.