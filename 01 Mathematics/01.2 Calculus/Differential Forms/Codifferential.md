---
type: technical-term
title: "Codifferential"
aliases:
  - Formal Adjoint of Exterior Derivative
  - Hodge Codifferential
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Hodge Theory
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
  - hodge-theory
sources:
  - "Warner (1983), Foundations of Differentiable Manifolds and Lie Groups"
  - "Jost (2017), Riemannian Geometry and Geometric Analysis"
related: []
projects: []
---

> [!abstract] Definition
> The **codifferential** is a differential operator on differential forms that lowers degree by one.
>
> On an oriented Riemannian $n$-manifold:
>
> $$\delta:\Omega^k(M)\rightarrow\Omega^{k-1}(M)$$
>
> It is the formal $L^2$-adjoint of the exterior derivative under suitable boundary conditions or compact-support assumptions.

> [!important] Hodge Star Formula
> With the convention that the Hodge Laplacian is positive-semidefinite,
>
> $$\delta=(-1)^{n(k+1)+1}*d*$$
>
> on $k$-forms in a Riemannian $n$-manifold.
>
> Sign conventions for $\delta$ vary across references, so the convention should always be stated.

> [!note] Degree Reduction
> The codifferential reverses the degree change of the exterior derivative:
>
> $$d:\Omega^k(M)\rightarrow\Omega^{k+1}(M)$$
>
> $$\delta:\Omega^k(M)\rightarrow\Omega^{k-1}(M)$$
>
> For 0-forms:
>
> $$\delta f=0$$

> [!important] Formal Adjoint Property
> Under suitable conditions:
>
> $$\langle d\alpha,\beta\rangle_{L^2}
> =
> \langle\alpha,\delta\beta\rangle_{L^2}$$
>
> Boundary terms must be accounted for when the manifold has a boundary and the forms do not satisfy appropriate boundary conditions.

> [!note] Relation to Divergence
> On a Riemannian manifold, the codifferential acting on a 1-form is related to the negative divergence of its metric-dual vector field.
>
> If $\alpha=V^\flat$, then
>
> $$\delta\alpha=-\operatorname{div}V$$
>
> under the stated sign convention.

> [!important] Fundamental Properties
> The codifferential satisfies
>
> $$\delta^2=0$$
>
> and is metric-dependent because its definition uses the Hodge star.

> [!warning] Codifferential Versus Exterior Derivative
> The exterior derivative is defined from the smooth structure alone.
>
> The codifferential depends on the metric and orientation through the Hodge star.
>
> They are related but have different degrees, dependencies, and geometric interpretations.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Hodge Star Operator — defines the codifferential formula.
> - Exterior Derivative — provides the differential operator whose adjoint is taken.
> - Metric Tensor — determines the inner product on forms.
>
> **Downstream Knowledge**
> - Hodge Laplacian — combines $d$ and $\delta$.
> - Harmonic Forms — characterized by vanishing Hodge Laplacian.
> - Hodge Theory — studies the relationship between harmonic forms and cohomology.