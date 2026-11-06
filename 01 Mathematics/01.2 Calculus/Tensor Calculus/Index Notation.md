---
type: technical-term
title: "Index Notation"
aliases:
  - Tensor Index Notation
  - Einstein Summation Notation
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
  - "Wald (1984), General Relativity"
related: []
projects: []
---

> [!abstract] Definition
> **Index notation** is a mathematical notation used to represent tensor components and operations through indexed symbols.
>
> It is especially useful for expressing multilinear relationships, coordinate transformations, contractions, and differential operations.

> [!important] Einstein Summation Convention
> The Einstein summation convention states that a repeated index appearing once as an upper index and once as a lower index is implicitly summed over its full range.
>
> For example,
>
> $$a_i b^i=\sum_{i=1}^{n}a_i b^i$$
>
> The repeated index is called a dummy index.

> [!note] Free and Dummy Indices
> - **Free indices** appear once in each term and determine the component being represented.
> - **Dummy indices** appear twice in a term and are summed over.
>
> Example:
>
> $$C^i{}_j=A^i{}_kB^k{}_j$$
>
> Here, $i$ and $j$ are free indices, while $k$ is a dummy index.

> [!important] Index Consistency
> Every term in a valid tensor equation must have the same free indices in the same positions.
>
> A dummy index can be renamed without changing the expression, provided the renaming does not introduce ambiguity.

> [!note] Tensor Operations
> **Tensor contraction**
>
> $$T^i{}_i$$
>
> **Matrix composition**
>
> $$C^i{}_j=A^i{}_kB^k{}_j$$
>
> **Metric contraction**
>
> $$g_{ij}v^iv^j$$
>
> **Covariant derivative**
>
> $$\nabla_jV^i$$

> [!warning] Upper and Lower Indices
> Upper and lower indices have different transformation properties.
>
> They must not be treated as interchangeable labels. Moving an index from an upper to a lower position, or vice versa, generally requires a metric tensor or inverse metric.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensors — provides the indexed component representation.
> - Tensor Types and Ranks — explains upper and lower indices.
> - Tensor Components and Transformation Laws — establishes their coordinate behavior.
>
> **Downstream Knowledge**
> - Tensor Contraction — uses repeated indices to express contraction.
> - Covariant Derivatives — uses indexed connection coefficients.
> - Riemann Curvature Tensor — uses index notation to express curvature components.