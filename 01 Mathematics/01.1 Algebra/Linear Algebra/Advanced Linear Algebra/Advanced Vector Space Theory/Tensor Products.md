---
type: technical-term
title: "Tensor Products"
aliases:
  - Tensor Product of Vector Spaces
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Multilinear Algebra
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - linear-algebra
  - multilinear-algebra
sources:
  - "Greub, Werner H. Multilinear Algebra, 2nd ed., 1978."
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
related: []
projects: []
---

> [!abstract] Definition
> Let $V$ and $W$ be vector spaces over a field $\mathbb{F}$.
>
> Their **tensor product**, denoted by:
>
> $$V\otimes W$$
>
> is a vector space equipped with a bilinear map:
>
> $$\tau:V\times W\rightarrow V\otimes W$$
>
> such that every bilinear map from $V\times W$ into another vector space factors uniquely through a linear map from $V\otimes W$.

> [!important] Universal Property
> For every vector space $X$ and every bilinear map:
>
> $$b:V\times W\rightarrow X$$
>
> there exists a unique linear map:
>
> $$\widetilde b:V\otimes W\rightarrow X$$
>
> satisfying:
>
> $$b(v,w)=\widetilde b(v\otimes w)$$
>
> This property characterizes the tensor product up to a unique isomorphism.
>
> The tensor product is therefore a construction that converts bilinear relationships into linear relationships.

> [!info] Pure Tensors
> Elements of the form:
>
> $$v\otimes w$$
>
> are called **pure tensors** or **decomposable tensors**.
>
> General elements of $V\otimes W$ are finite sums:
>
> $$t=\sum_{i=1}^{k}v_i\otimes w_i$$
>
> Not every tensor is necessarily expressible as a single pure tensor.

> [!important] Bilinearity Relations
> The tensor product satisfies:
>
> $$(v_1+v_2)\otimes w=v_1\otimes w+v_2\otimes w$$
>
> $$v\otimes(w_1+w_2)=v\otimes w_1+v\otimes w_2$$
>
> $$(av)\otimes w=a(v\otimes w)=v\otimes(aw)$$
>
> These relations encode bilinearity into the resulting vector space.

> [!example] Finite-Dimensional Basis
> Let:
>
> $$B=(v_1,\ldots,v_m)$$
>
> be a basis of $V$, and:
>
> $$C=(w_1,\ldots,w_n)$$
>
> be a basis of $W$.
>
> Then:
>
> $$\{v_i\otimes w_j\mid 1\leq i\leq m,\ 1\leq j\leq n\}$$
>
> forms a basis of $V\otimes W$.
>
> Consequently:
>
> $$\dim(V\otimes W)=\dim(V)\dim(W)$$

> [!important] Tensor Product of Linear Maps
> Given linear maps:
>
> $$S:V\rightarrow V'$$
>
> $$T:W\rightarrow W'$$
>
> there is an induced linear map:
>
> $$S\otimes T:V\otimes W\rightarrow V'\otimes W'$$
>
> defined by:
>
> $$(S\otimes T)(v\otimes w)=S(v)\otimes T(w)$$

> [!important] Tensor Product and Multilinear Maps
> The tensor product generalizes to multiple vector spaces:
>
> $$V_1\otimes\cdots\otimes V_k$$
>
> It provides a linear representation of multilinear maps:
>
> $$b:V_1\times\cdots\times V_k\rightarrow X$$
>
> through linear maps defined on the corresponding tensor product.

> [!note] Tensor Product and Dual Spaces
> For finite-dimensional vector spaces, there is a natural isomorphism:
>
> $$V^*\otimes W^*\cong(V\otimes W)^*$$
>
> This identifies tensors formed from dual vectors with linear functionals on the tensor product.

> [!warning] Common Misconceptions
> - A tensor is not simply a multidimensional array. Arrays are coordinate representations relative to chosen bases.
> - A tensor product is not the Cartesian product $V\times W$.
> - A general tensor need not be a pure tensor.
> - The tensor product is characterized by its universal property, not merely by a multiplication rule.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Defines the spaces being combined.
> - **Linear Maps:** Provides the linear structure of the universal property.
> - **Bilinear Maps:** Essential for understanding the defining property.
> - **Dual Vector Spaces:** Supports the construction of covariant and contravariant tensor spaces.

> [!success] Downstream Knowledge
> - **Relevant — Multilinear Algebra:** Generalizes the study of multilinear maps and tensor constructions.
> - **Relevant — Tensor Spaces:** Studies higher-order tensor products and their algebraic structure.
> - **Advanced — Tensor Algebra:** Constructs an associative algebra from all tensor powers of a vector space.
> - **Advanced — Exterior Algebra:** Constructs alternating tensors and wedge products.
> - **Advanced — Symmetric Algebra:** Constructs symmetric tensor structures.

> [!quote] References
> - Greub, Werner H. *Multilinear Algebra*, 2nd ed., 1978.
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.