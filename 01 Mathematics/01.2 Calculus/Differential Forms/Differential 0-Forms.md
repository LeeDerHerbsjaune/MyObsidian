---
type: technical-term
title: "Differential 0-Forms"
aliases:
  - Zero-Forms
  - Smooth Scalar Fields
field:
  - Mathematics
subfield:
  - Differential Geometry
  - Differential Forms
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - differential-forms
sources:
  - "Lee (2012), Introduction to Smooth Manifolds"
  - "Spivak (1965), Calculus on Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> A **differential 0-form** on a smooth manifold $M$ is a smooth real-valued function:
>
> $$f:M\rightarrow\mathbb{R}$$
>
> The space of differential 0-forms is
>
> $$\Omega^0(M)=C^\infty(M)$$

> [!important] Algebraic Interpretation
> A 0-form is an element of
>
> $$\Lambda^0(T_p^*M)\cong\mathbb{R}$$
>
> at every point $p$.
>
> It has degree zero and requires no tangent-vector arguments for evaluation.

> [!note] Exterior Derivative
> The exterior derivative maps a 0-form to a 1-form:
>
> $$d:\Omega^0(M)\rightarrow\Omega^1(M)$$
>
> In local coordinates:
>
> $$df=\frac{\partial f}{\partial x^i}dx^i$$
>
> This is the differential of the scalar function.

> [!note] Wedge Product
> A 0-form acts as a scalar multiplier:
>
> $$f\wedge\omega=f\omega$$
>
> for any differential form $\omega$.

> [!note] Pullback
> For a smooth map $F:M\rightarrow N$ and a 0-form $f$ on $N$:
>
> $$F^*f=f\circ F$$
>
> The pullback of a scalar function is ordinary function composition.

> [!warning] Scope
> Differential 0-forms are not a separate algebraic object from smooth scalar fields. Their designation as forms places them within the graded differential-form framework.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Smooth Functions — provides the underlying scalar fields.
> - Differential Forms — provides the graded framework.
>
> **Downstream Knowledge**
> - Differential 1-Forms — the exterior derivative of a 0-form is a 1-form.
> - Exterior Derivative — generalizes the differential of scalar functions.