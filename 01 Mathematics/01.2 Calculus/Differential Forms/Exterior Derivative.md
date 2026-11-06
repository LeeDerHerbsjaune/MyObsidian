---
type: technical-term
title: "Exterior Derivative"
aliases:
  - Exterior Differential
  - de Rham Differential
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
  - "Spivak (1965), Calculus on Manifolds"
  - "Lee (2012), Introduction to Smooth Manifolds"
related: []
projects: []
---

> [!abstract] Definition
> The **exterior derivative** is a linear differential operator that maps differential $k$-forms to differential $(k+1)$-forms:
>
> $$d:\Omega^k(M)\rightarrow\Omega^{k+1}(M)$$
>
> It generalizes the differential of scalar functions and provides a coordinate-independent differentiation operation on differential forms.

> [!note] Coordinate Formula
> For a $k$-form:
>
> $$\omega=\frac{1}{k!}\omega_{i_1\cdots i_k}
> dx^{i_1}\wedge\cdots\wedge dx^{i_k}$$
>
> its exterior derivative is
>
> $$d\omega=
> \frac{1}{k!}
> \frac{\partial\omega_{i_1\cdots i_k}}{\partial x^j}
> dx^j\wedge dx^{i_1}\wedge\cdots\wedge dx^{i_k}$$

> [!important] Fundamental Properties
> **Linearity**
>
> $$d(a\alpha+b\beta)=a\,d\alpha+b\,d\beta$$
>
> **Graded Leibniz rule**
>
> $$d(\alpha\wedge\beta)
> =d\alpha\wedge\beta
> +(-1)^k\alpha\wedge d\beta$$
>
> where $\alpha$ has degree $k$.
>
> **Nilpotency**
>
> $$d^2=0$$

> [!example] Exterior Derivative of a 1-Form
> In three-dimensional coordinates, let
>
> $$\omega=P\,dx+Q\,dy+R\,dz$$
>
> Then
>
> $$\begin{aligned}
> d\omega={}&
> \left(\frac{\partial Q}{\partial x}
> -\frac{\partial P}{\partial y}\right)dx\wedge dy\\
> &+\left(\frac{\partial R}{\partial x}
> -\frac{\partial P}{\partial z}\right)dx\wedge dz\\
> &+\left(\frac{\partial R}{\partial y}
> -\frac{\partial Q}{\partial z}\right)dy\wedge dz
> \end{aligned}$$

> [!important] Metric Independence
> The exterior derivative requires only the smooth structure of the manifold.
>
> It does not require a metric or a connection.

> [!warning] Exterior Derivative Versus Covariant Derivative
> The exterior derivative acts on differential forms and increases their degree.
>
> The covariant derivative acts on general tensor fields and introduces a connection.
>
> They are different operators with different mathematical roles.

> [!summary] Knowledge Relationships
> **Foundation Knowledge**
> - Differential Forms — defines the objects being differentiated.
> - Wedge Product — determines the graded Leibniz rule.
> - Smooth Manifolds — supplies the differentiable structure.
>
> **Downstream Knowledge**
> - Closed Forms — defined by vanishing exterior derivative.
> - Exact Forms — defined as images of the exterior derivative.
> - Generalized Stokes' Theorem — relates exterior differentiation to integration.
> - De Rham Cohomology — studies the kernel and image of the exterior derivative.