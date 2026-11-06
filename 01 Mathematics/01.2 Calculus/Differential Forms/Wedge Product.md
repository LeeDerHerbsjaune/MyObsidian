---
type: technical-term
title: "Wedge Product"
aliases:
  - Exterior Product
  - Alternating Product
field:
  - Mathematics
subfield:
  - Exterior Algebra
  - Differential Geometry
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
sources:
  - "Flanders (1963), Differential Forms with Applications to the Physical Sciences"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> The **wedge product** is the bilinear multiplication operation on exterior algebra and differential forms. It combines forms while preserving their alternating structure.
>
> If $\alpha$ is a $k$-form and $\beta$ is an $\ell$-form, then
>
> $$\alpha\wedge\beta\in\Omega^{k+\ell}(M)$$

> [!important] Graded Commutativity
> The wedge product satisfies
>
> $$\alpha\wedge\beta=(-1)^{k\ell}\beta\wedge\alpha$$
>
> where $k$ and $\ell$ are the degrees of the forms.
>
> For two $1$-forms:
>
> $$\alpha\wedge\beta=-\beta\wedge\alpha$$
>
> Consequently,
>
> $$\alpha\wedge\alpha=0$$
>
> for every $1$-form $\alpha$.

> [!note] Coordinate Expression
> For coordinate $1$-forms $dx^i$:
>
> $$dx^i\wedge dx^j=-dx^j\wedge dx^i$$
>
> and
>
> $$dx^i\wedge dx^i=0$$
>
> A $k$-form can be expanded using wedge products of coordinate $1$-forms.

> [!note] Product of General Forms
> If
>
> $$\alpha=\frac{1}{k!}\alpha_{i_1\cdots i_k}
> dx^{i_1}\wedge\cdots\wedge dx^{i_k}$$
>
> and $\beta$ is an $\ell$-form, their wedge product is obtained by multiplying the expressions and applying antisymmetry.
>
> The resulting form has degree $k+\ell$.

> [!important] Associativity and Leibniz Compatibility
> The wedge product is associative:
>
> $$(\alpha\wedge\beta)\wedge\gamma
> =\alpha\wedge(\beta\wedge\gamma)$$
>
> It also interacts with the exterior derivative through the graded Leibniz rule:
>
> $$d(\alpha\wedge\beta)
> =d\alpha\wedge\beta
> +(-1)^k\alpha\wedge d\beta$$

> [!warning] Wedge Product Versus Tensor Product
> The tensor product combines tensor factors without imposing antisymmetry.
>
> The wedge product is the alternating product induced from the tensor product. It is therefore a specialized operation rather than an ordinary tensor product.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Exterior Algebra — provides the algebraic setting.
> - Alternating Multilinear Forms — explains the antisymmetry being imposed.
>
> **Downstream Knowledge**
> - Differential Forms — uses wedge products to combine forms.
> - Exterior Derivative — satisfies a graded Leibniz rule with respect to the wedge product.
> - Hodge Star Operator — acts on the resulting graded spaces.