---
type: technical-term
title: "Differential 1-Forms"
aliases:
  - One-Forms
  - Covector Fields
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
> A **differential 1-form** is a smooth section of the cotangent bundle $T^*M$.
>
> At each point $p$, it is a linear functional on the tangent space:
>
> $$\omega_p:T_pM\rightarrow\mathbb{R}$$

> [!important] Coordinate Representation
> In local coordinates:
>
> $$\omega=\omega_i\,dx^i$$
>
> where $\omega_i$ are smooth component functions and $dx^i$ are coordinate covectors.

> [!note] Evaluation
> A 1-form acts on a tangent vector:
>
> $$\omega_p(v)=\omega_i(p)v^i$$
>
> The result is a scalar.
>
> This pairing is coordinate-independent.

> [!example] Differential of a Function
> For a smooth scalar function $f$:
>
> $$df=\frac{\partial f}{\partial x^i}dx^i$$
>
> The differential measures the first-order variation of $f$ in tangent directions:
>
> $$df_p(v)=v(f)$$

> [!note] Pullback and Integration
> A 1-form can be pulled back along a smooth map.
>
> It can also be integrated along an oriented curve $\gamma$:
>
> $$\int_\gamma\omega$$
>
> This is the differential-form formulation of a line integral of a covector field.

> [!warning] Covector Versus Vector
> A 1-form belongs to the cotangent space, while a vector belongs to the tangent space.
>
> A metric can identify vectors with covectors, but this identification is not intrinsic to the definition of a 1-form.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Cotangent Spaces — provide the vector spaces of covectors.
> - Differential Forms — provides the general definition.
>
> **Downstream Knowledge**
> - Higher-Degree Differential Forms — generalizes 1-forms to higher degrees.
> - Exterior Derivative — maps 1-forms to 2-forms.
> - Integration of Differential Forms — integrates 1-forms along curves.