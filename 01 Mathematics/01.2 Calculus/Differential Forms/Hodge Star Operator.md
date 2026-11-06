---
type: technical-term
title: "Hodge Star Operator"
aliases:
  - Hodge Star
  - Hodge Dual
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Riemannian Geometry
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
> The **Hodge star operator** is a metric- and orientation-dependent linear operator that maps differential $k$-forms to differential $(n-k)$-forms on an oriented $n$-dimensional Riemannian manifold.
>
> It is defined by
>
> $$*:\Omega^k(M)\rightarrow\Omega^{n-k}(M)$$

> [!important] Defining Identity
> The Hodge star is characterized by
>
> $$\alpha\wedge *\beta
> =
> \langle\alpha,\beta\rangle_g\,\mathrm{vol}_g$$
>
> for $k$-forms $\alpha$ and $\beta$, where:
> - $\langle\cdot,\cdot\rangle_g$ is the inner product induced by the metric.
> - $\mathrm{vol}_g$ is the metric volume form determined by the metric and orientation.

> [!note] Action on Basis Forms
> In an oriented orthonormal coframe in three dimensions:
>
> $$*1=e^1\wedge e^2\wedge e^3$$
>
> $$*e^1=e^2\wedge e^3$$
>
> $$*e^2=e^3\wedge e^1$$
>
> $$*e^3=e^1\wedge e^2$$
>
> The star maps forms to complementary degrees.

> [!important] Double Hodge Star
> On $k$-forms in an oriented Riemannian $n$-manifold:
>
> $$**\omega=(-1)^{k(n-k)}\omega$$
>
> This identity depends on the metric signature and convention. The displayed formula is for a positive-definite Riemannian metric.

> [!note] Hodge Inner Product
> The Hodge star induces an inner product on forms:
>
> $$\langle\alpha,\beta\rangle_{L^2}
> =
> \int_M\alpha\wedge *\beta$$
>
> for forms of the same degree, assuming the integral is well-defined.

> [!important] Metric Dependence
> Unlike the wedge product and exterior derivative, the Hodge star requires:
> - A metric.
> - An orientation.
>
> It therefore introduces geometric information beyond the smooth structure of the manifold.

> [!warning] Riemannian Versus Pseudo-Riemannian Metrics
> The double-star identity changes when the metric is indefinite.
>
> In pseudo-Riemannian geometry, the metric signature contributes an additional sign. Do not apply the Riemannian identity without checking the signature convention.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Differential Forms — provides the graded spaces.
> - Metric Tensor — induces inner products on forms.
> - Orientation — determines the volume form and star operation.
>
> **Downstream Knowledge**
> - Codifferential — is defined using the Hodge star and exterior derivative.
> - Hodge Laplacian — combines the exterior derivative and codifferential.
> - Hodge Theory — studies harmonic forms and cohomology.