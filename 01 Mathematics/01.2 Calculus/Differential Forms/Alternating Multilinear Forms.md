---
type: technical-term
title: "Alternating Multilinear Forms"
aliases:
  - Alternating Forms
  - Alternating Multilinear Maps
field:
  - Mathematics
subfield:
  - Multilinear Algebra
  - Exterior Algebra
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - multilinear-algebra
sources:
  - "Greub (1978), Multilinear Algebra"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> An **alternating multilinear form** of degree $k$ on a vector space $V$ is a multilinear map
>
> $$\omega:\underbrace{V\times\cdots\times V}_{k}
> \rightarrow\mathbb{R}$$
>
> that vanishes whenever two of its arguments are equal.
>
> Equivalently, exchanging any two arguments changes the sign of the output.

> [!important] Alternating Property
> For any permutation $\sigma$ of the arguments:
>
> $$\omega(v_{\sigma(1)},\ldots,v_{\sigma(k)})
> =\operatorname{sgn}(\sigma)
> \omega(v_1,\ldots,v_k)$$
>
> In particular, if two arguments coincide, then
>
> $$\omega(v_1,\ldots,v_k)=0$$

> [!note] Degree Examples
> - Degree 0: a scalar.
> - Degree 1: a linear functional.
> - Degree 2: an alternating bilinear form.
> - Degree $k$: an alternating $k$-linear functional.

> [!example] Alternating Bilinear Form
> On $\mathbb{R}^2$, define
>
> $$\omega(u,v)=u^1v^2-u^2v^1$$
>
> Then
>
> $$\omega(v,u)=-\omega(u,v)$$
>
> This expression measures the signed area of the parallelogram spanned by $u$ and $v$.

> [!note] Determinant
> The determinant is an important example of an alternating multilinear form:
>
> $$\det:V^n\rightarrow\mathbb{R}$$
>
> for an $n$-dimensional vector space with a chosen basis or volume form.

> [!important] Connection to Exterior Algebra
> The space of alternating $k$-linear forms is naturally identified with
>
> $$\Lambda^k(V^*)$$
>
> This identification provides the algebraic foundation for differential $k$-forms.

> [!warning] Alternating Versus Symmetric
> An alternating multilinear form changes sign under an exchange of arguments.
>
> A symmetric multilinear form remains unchanged.
>
> These are distinct subspaces of multilinear forms and support different algebraic constructions.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Multilinear Algebra — provides multilinear maps.
> - Dual Vector Spaces — provides covariant arguments.
>
> **Downstream Knowledge**
> - Exterior Algebra — organizes alternating forms into a graded algebra.
> - Wedge Product — combines alternating forms.
> - Differential Forms — makes alternating forms vary smoothly over manifolds.