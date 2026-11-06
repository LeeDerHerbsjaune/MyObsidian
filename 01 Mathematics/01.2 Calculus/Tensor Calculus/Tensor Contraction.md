---
type: technical-term
title: "Tensor Contraction"
aliases:
  - Contraction of Tensors
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
  - "Schutz (1980), Geometrical Methods of Mathematical Physics"
related: []
projects: []
---

> [!abstract] Definition
> **Tensor contraction** is an operation that pairs one contravariant index with one covariant index of a tensor, producing a tensor of lower order.
>
> For a tensor of type $(r,s)$, contraction produces a tensor of type
>
> $$(r-1,s-1)$$
>
> provided that $r\geq1$ and $s\geq1$.

> [!important] Component Definition
> Consider a tensor
>
> $$T^{i_1\cdots i_r}_{j_1\cdots j_s}$$
>
> Contracting one upper and one lower index means summing over the repeated index:
>
> $$S^{i_2\cdots i_r}_{j_2\cdots j_s}
> =
> T^{k i_2\cdots i_r}_{k j_2\cdots j_s}$$
>
> The contracted index is summed over the dimension of the underlying vector space.

> [!example] Trace of a Linear Operator
> For a tensor of type $(1,1)$ represented by $A^i{}_j$, its contraction is
>
> $$\operatorname{tr}(A)=A^i{}_i$$
>
> This produces a scalar and corresponds to the trace of the associated linear operator.

> [!example] Vector-Covector Pairing
> Given a vector $v^i$ and a covector $\omega_j$, their contraction is
>
> $$\omega_i v^i$$
>
> The result is a scalar.

> [!important] Coordinate Invariance
> Contraction is a coordinate-independent tensor operation.
>
> The transformation factors associated with the contracted upper and lower indices cancel, ensuring that the result transforms as a tensor of the reduced type.

> [!warning] Contraction Versus Inner Product
> General tensor contraction pairs one contravariant and one covariant slot without requiring a metric.
>
> However, contracting two covariant indices or two contravariant indices requires an additional structure, typically a nondegenerate metric or inverse metric.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Tensors — defines the objects being contracted.
> - Tensor Types and Ranks — identifies compatible index types.
> - Index Notation — expresses the summation operation.
>
> **Downstream Knowledge**
> - Ricci Tensor — obtained by contracting indices of the Riemann curvature tensor.
> - Scalar Curvature — obtained by contracting the Ricci tensor with the inverse metric.
> - Tensor Algebra — incorporates contraction as a fundamental operation.