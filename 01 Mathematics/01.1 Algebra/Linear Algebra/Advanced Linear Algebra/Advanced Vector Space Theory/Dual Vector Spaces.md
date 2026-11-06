---
type: technical-term
title: "Dual Vector Spaces"
aliases:
  - Dual Space
abbreviation: ""
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Functional Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - linear-algebra
  - vector-spaces
sources:
  - "Axler, Sheldon. Linear Algebra Done Right, 3rd ed., 2015."
  - "Roman, Steven. Advanced Linear Algebra, 3rd ed., 2008."
related: []
projects: []
---

> [!abstract] Definition
> Let $V$ be a vector space over a field $\mathbb{F}$.
>
> The **dual vector space** of $V$, denoted by $V^*$, is the vector space consisting of all linear functionals from $V$ to $\mathbb{F}$:
>
> $$V^* = \operatorname{Hom}(V,\mathbb{F})$$
>
> A linear functional is a linear map:
>
> $$f:V\rightarrow\mathbb{F}$$

> [!info] Core Concept
> While vectors represent elements of a vector space, linear functionals assign scalars to vectors while preserving linearity.
>
> The dual space collects all possible linear functionals defined on the original vector space.

> [!note] Vector Space Operations
> For $f,g\in V^*$ and $a\in\mathbb{F}$:
>
> $$(f+g)(v)=f(v)+g(v)$$
>
> $$(af)(v)=af(v)$$
>
> These operations make $V^*$ a vector space over $\mathbb{F}$.

> [!important] Dual Basis
> Suppose $V$ is finite-dimensional and has an ordered basis:
>
> $$B=(v_1,\ldots,v_n)$$
>
> The corresponding **dual basis** is:
>
> $$B^*=(v^1,\ldots,v^n)$$
>
> where each $v^i\in V^*$ satisfies:
>
> $$v^i(v_j)=\delta_{ij}$$
>
> Here, $\delta_{ij}$ is the Kronecker delta.
>
> Every linear functional $f\in V^*$ can be expressed uniquely as:
>
> $$f=\sum_{i=1}^{n}f(v_i)v^i$$

> [!example] Coordinate Functionals
> Let $V=\mathbb{R}^3$ with its standard basis.
>
> For $v=(x_1,x_2,x_3)$, define:
>
> $$f_1(v)=x_1,\quad f_2(v)=x_2,\quad f_3(v)=x_3$$
>
> These functionals form the dual basis of the standard basis.
>
> Each functional extracts one coordinate of a vector.

> [!important] Dimension
> If $V$ is finite-dimensional:
>
> $$\dim(V^*)=\dim(V)$$
>
> This dimension equality does not imply that $V$ and $V^*$ are canonically identical.

> [!important] Double Dual
> The **double dual** is:
>
> $$V^{**}=(V^*)^*$$
>
> There is a canonical linear map:
>
> $$J:V\rightarrow V^{**}$$
>
> defined by:
>
> $$J(v)(f)=f(v)$$
>
> This map is always injective. If $V$ is finite-dimensional, it is an isomorphism.
>
> In infinite-dimensional vector spaces, it is generally not surjective.

> [!note] Dual of a Linear Transformation
> Let:
>
> $$T:V\rightarrow W$$
>
> be a linear transformation.
>
> Its **dual map** is:
>
> $$T^*:W^*\rightarrow V^*$$
>
> defined by:
>
> $$T^*(\varphi)=\varphi\circ T$$
>
> Equivalently:
>
> $$(T^*\varphi)(v)=\varphi(Tv)$$
>
> Notice that the direction of the map is reversed.

> [!important] Matrix Representation
> If $T$ has matrix $A$ with respect to chosen bases, the matrix of its dual map is represented by the transpose matrix $A^T$ with respect to the corresponding dual bases.
>
> This is the algebraic origin of the transpose operation in the study of dual linear maps.

> [!warning] Important Distinction
> A dual vector is not automatically the same object as a vector.
>
> Identifying $V$ with $V^*$ requires additional structure or a chosen isomorphism. An inner product, for example, can induce such an identification in finite-dimensional inner product spaces.

> [!success] Foundation Knowledge
> - **Vector Spaces:** Defines the domain on which linear functionals act.
> - **Linear Transformations:** Provides the definition of linear functionals and dual maps.
> - **Basis and Dimension:** Supports the construction of dual bases and finite-dimensional dimension results.

> [!success] Downstream Knowledge
> - **Relevant — Annihilators:** Characterizes subspaces of $V^*$ that vanish on a given subspace of $V$.
> - **Relevant — Dual Linear Maps:** Develops the contravariant relationship between linear transformations and their duals.
> - **Advanced — Double Dual and Reflexivity:** Studies when the canonical embedding into the double dual is surjective.
> - **Advanced — Tensor Products:** Uses dual spaces to construct tensor spaces and multilinear representations.

> [!quote] References
> - Axler, Sheldon. *Linear Algebra Done Right*, 3rd ed., 2015.
> - Roman, Steven. *Advanced Linear Algebra*, 3rd ed., 2008.