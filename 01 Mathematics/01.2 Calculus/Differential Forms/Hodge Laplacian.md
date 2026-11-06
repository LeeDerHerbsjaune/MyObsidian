---
type: technical-term
title: "Hodge Laplacian"
aliases:
  - Laplace-de Rham Operator
  - Laplacian on Differential Forms
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
> The **Hodge Laplacian**, also called the Laplace-de Rham operator, is a second-order differential operator acting on differential forms.
>
> It is defined by combining the exterior derivative and codifferential:
>
> $$\boxed{\Delta_H=d\delta+\delta d}$$
>
> It preserves form degree:
>
> $$\Delta_H:\Omega^k(M)\rightarrow\Omega^k(M)$$

> [!important] Operator Structure
> The two terms have different compositions:
>
> $$d\delta:\Omega^k(M)\rightarrow\Omega^k(M)$$
>
> $$\delta d:\Omega^k(M)\rightarrow\Omega^k(M)$$
>
> Their sum produces a degree-preserving second-order operator.

> [!note] Action on Scalar Functions
> For a 0-form $f$:
>
> $$\Delta_H f=\delta df$$
>
> Under the convention used here, this is the nonnegative Laplacian:
>
> $$\Delta_H f=-\operatorname{div}(\operatorname{grad}f)$$
>
> Some mathematical and physical references use the opposite sign convention.

> [!important] Harmonic Forms
> A differential form is harmonic if
>
> $$\Delta_H\omega=0$$
>
> On a compact oriented Riemannian manifold without boundary:
>
> $$\langle\Delta_H\omega,\omega\rangle
> =
> \|d\omega\|^2+\|\delta\omega\|^2$$
>
> Therefore, harmonicity is equivalent to
>
> $$d\omega=0,\qquad\delta\omega=0$$
>
> under these assumptions.

> [!note] Hodge Decomposition
> On a compact oriented Riemannian manifold without boundary, the space of differential $k$-forms admits the orthogonal decomposition
>
> $$\Omega^k(M)
> =
> \mathcal{H}^k(M)
> \oplus d\Omega^{k-1}(M)
> \oplus\delta\Omega^{k+1}(M)$$
>
> in the appropriate smooth or completed functional-analytic formulation.
>
> Here $\mathcal{H}^k(M)$ denotes the space of harmonic $k$-forms.

> [!important] Relation to de Rham Cohomology
> Hodge theory establishes that every de Rham cohomology class on a compact oriented Riemannian manifold without boundary has a unique harmonic representative.
>
> Consequently:
>
> $$H^k_{\mathrm{dR}}(M)\cong\mathcal{H}^k(M)$$
>
> This connects the topology of a manifold with the analysis of a metric-dependent differential operator.

> [!warning] Assumptions and Boundary Conditions
> The decomposition and harmonic-representative results above require compactness, orientation, a Riemannian metric, and no boundary in the stated form.
>
> Manifolds with boundary require suitable boundary conditions, such as absolute or relative boundary conditions.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Exterior Derivative — provides $d$.
> - Codifferential — provides $\delta$.
> - Hodge Star Operator — defines the codifferential.
> - Metric Tensor — induces the inner product on forms.
>
> **Downstream Knowledge**
> - Hodge Theory — studies harmonic forms and decomposition.
> - De Rham Cohomology — is represented by harmonic forms under suitable compactness assumptions.
> - Elliptic Differential Operators — provides the analytical framework for studying the Hodge Laplacian.