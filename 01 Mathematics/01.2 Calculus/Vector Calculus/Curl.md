---
type: technical-term
title: "Curl"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Differential Operators
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - differential-operators
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Curl** is a vector differential operator that measures the local rotational tendency of a three-dimensional vector field.
>
> Its direction indicates the local axis of rotation, while its magnitude measures the corresponding rotational strength.

## 1. Mathematical Formulation

> [!definition] Curl in Cartesian Coordinates
> For a differentiable vector field:
>
> $$\mathbf{F}=
> \begin{bmatrix}
> P\\Q\\R
> \end{bmatrix}$$
>
> Its curl is:
>
> $$\nabla\times\mathbf{F}
> =
> \begin{bmatrix}
> \frac{\partial R}{\partial y}
> -\frac{\partial Q}{\partial z}\\
> \frac{\partial P}{\partial z}
> -\frac{\partial R}{\partial x}\\
> \frac{\partial Q}{\partial x}
> -\frac{\partial P}{\partial y}
> \end{bmatrix}$$
>
> The result is another vector field.

> [!note] Determinant Representation
> The curl can also be represented symbolically as:
>
> $$\nabla\times\mathbf{F}
> =
> \begin{vmatrix}
> \mathbf{i}&\mathbf{j}&\mathbf{k}\\
> \frac{\partial}{\partial x}&
> \frac{\partial}{\partial y}&
> \frac{\partial}{\partial z}\\
> P&Q&R
> \end{vmatrix}$$
>
> This is a computational mnemonic rather than an ordinary determinant of numerical entries.

## 2. Geometric Interpretation

> [!important] Local Rotation
> Curl measures the infinitesimal circulation per unit area in a specified orientation.
>
> Its direction follows the right-hand rule.
>
> - Nonzero curl indicates local rotational tendency.
> - Zero curl indicates an irrotational field.
>
> Curl is a local differential property; it should not be confused with the total circulation around an arbitrary finite curve.

## 3. Mathematical Properties

> [!important] Linearity
> For differentiable vector fields $\mathbf{F}$ and $\mathbf{G}$:
>
> $$\nabla\times(a\mathbf{F}+b\mathbf{G})
> =
> a(\nabla\times\mathbf{F})
> +b(\nabla\times\mathbf{G})$$

> [!important] Curl of a Gradient
> For a sufficiently smooth scalar field $f$:
>
> $$\nabla\times(\nabla f)=\mathbf{0}$$
>
> Therefore, gradient fields are irrotational.

> [!important] Curl of a Curl
> For sufficiently smooth vector fields:
>
> $$\nabla\times(\nabla\times\mathbf{F})
> =
> \nabla(\nabla\cdot\mathbf{F})
> -\nabla^2\mathbf{F}$$
>
> Here, $\nabla^2\mathbf{F}$ denotes the componentwise vector Laplacian in Cartesian coordinates.

## 4. Irrotational Vector Fields

> [!definition] Irrotational Field
> A vector field is called **irrotational** if:
>
> $$\nabla\times\mathbf{F}=\mathbf{0}$$
>
> A curl-free field is locally a gradient field under suitable regularity conditions.
>
> Global existence of a scalar potential additionally depends on the topology of the domain.

## 5. Stokes' Theorem

> [!important] Integral Relationship
> Stokes' Theorem relates the circulation around a boundary curve to the surface integral of curl:
>
> $$\oint_{\partial S}\mathbf{F}\cdot d\mathbf{r}
> =
> \iint_S(\nabla\times\mathbf{F})\cdot\mathbf{n}\,dS$$
>
> It converts a line integral around a closed curve into a surface integral over a surface bounded by that curve.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Vector Fields:** Curl operates on differentiable vector fields.
- **Partial Derivatives:** Provides the derivatives required by the curl operator.
- **Cross Product:** Provides the three-dimensional vector algebra underlying its coordinate representation.

### Downstream Knowledge
- **Stokes' Theorem:** Relates curl to circulation.
- **Irrotational Vector Fields:** Studies fields whose curl vanishes.
- **Conservative Vector Fields:** Under suitable domain conditions, curl-free fields admit scalar potentials.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Schey, H. M. *Div, Grad, Curl, and All That: An Informal Text on Vector Calculus*. 4th edition, 2005.