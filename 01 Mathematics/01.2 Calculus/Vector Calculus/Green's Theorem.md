---
type: technical-term
title: "Green's Theorem"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Integral Theorems
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - integral-theorems
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Green's Theorem** is an integral theorem in two-dimensional vector calculus that relates a line integral around a positively oriented, simple closed curve to a double integral over the planar region enclosed by that curve.
>
> It establishes a relationship between circulation along a boundary and the scalar curl within the enclosed region.

## 1. Mathematical Formulation

> [!definition] Circulation Form
> Let $C$ be a positively oriented, piecewise-smooth, simple closed curve bounding a region $D$.
>
> If $P$ and $Q$ have continuous first-order partial derivatives on an open region containing $D$, then:
>
> $$\oint_C(P\,dx+Q\,dy)
> =
> \iint_D
> \left(
> \frac{\partial Q}{\partial x}
> -
> \frac{\partial P}{\partial y}
> \right)dA$$
>
> The boundary orientation is counterclockwise for a positively oriented planar region.

## 2. Flux Form

> [!important] Flux Version
> Green's Theorem also has a flux formulation:
>
> $$\oint_C(P\,dy-Q\,dx)
> =
> \iint_D
> \left(
> \frac{\partial P}{\partial x}
> +
> \frac{\partial Q}{\partial y}
> \right)dA$$
>
> The right-hand side is the two-dimensional divergence of the vector field.
>
> The left-hand side represents outward flux across the boundary when $C$ has positive orientation.

## 3. Geometric Interpretation

> [!important] Boundary and Interior
> Green's Theorem connects:
>
> - A line integral around the boundary of a planar region.
> - A double integral of a local differential quantity over the region.
>
> In the circulation form, the local quantity is the two-dimensional scalar curl:
>
> $$\frac{\partial Q}{\partial x}
> -
> \frac{\partial P}{\partial y}$$
>
> In the flux form, it is the two-dimensional divergence:
>
> $$\frac{\partial P}{\partial x}
> +
> \frac{\partial Q}{\partial y}$$

## 4. Important Properties

> [!important] Orientation
> Reversing the orientation of $C$ changes the sign of the line integral.
>
> The standard theorem assumes positive, counterclockwise orientation.

> [!important] Region Decomposition
> A planar region can be partitioned into smaller regions.
>
> When Green's Theorem is applied to each region, integrals along shared interior boundaries cancel because they are traversed in opposite directions.

## 5. Applications Within Vector Calculus

> [!note] Common Uses
> - Converting difficult line integrals into double integrals.
> - Converting planar flux integrals into area integrals.
> - Computing circulation over closed planar curves.
> - Establishing relationships between planar boundary behavior and interior field behavior.

## 6. Relationship with Other Integral Theorems

> [!important] Connection to Stokes' Theorem
> Green's Theorem is a two-dimensional special case of the generalized Stokes' Theorem.
>
> Its circulation form can be interpreted as Stokes' Theorem applied to a planar surface.

> [!important] Connection to the Divergence Theorem
> Its flux form is the two-dimensional analogue of the Divergence Theorem.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Line Integrals:** Provides the boundary integral.
- **Double Integrals:** Provides integration over the enclosed planar region.
- **Partial Derivatives:** Provides the differential quantities in the theorem.
- **Vector Fields:** Provides the fields whose circulation or flux is integrated.

### Downstream Knowledge
- **Stokes' Theorem:** Generalizes the circulation relationship to oriented surfaces in three dimensions.
- **Divergence Theorem:** Extends the flux relationship to closed surfaces enclosing volumes.

## 8. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Stewart, J. *Calculus: Early Transcendentals*. 8th edition, 2015.