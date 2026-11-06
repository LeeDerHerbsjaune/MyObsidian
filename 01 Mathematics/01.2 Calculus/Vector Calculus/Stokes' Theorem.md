---
type: technical-term
title: "Stokes' Theorem"
aliases:
  - Kelvin-Stokes Theorem
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
> **Stokes' Theorem** relates the circulation of a vector field around the boundary of an oriented surface to the surface integral of the curl of that field.
>
> It is a central result connecting local rotational behavior with global circulation.

## 1. Mathematical Formulation

> [!definition] Classical Stokes' Theorem
> Let $S$ be an oriented, sufficiently smooth surface with positively oriented boundary curve $\partial S$.
>
> If $\mathbf{F}$ has continuous first-order partial derivatives on an open region containing $S$, then:
>
> $$\oint_{\partial S}\mathbf{F}\cdot d\mathbf{r}
> =
> \iint_S
> (\nabla\times\mathbf{F})\cdot\mathbf{n}\,dS$$
>
> Here:
> - $\partial S$ is the boundary curve.
> - $\mathbf{n}$ is the chosen unit normal.
> - $\nabla\times\mathbf{F}$ is the curl of the vector field.
> - The orientation of $\partial S$ is determined by the right-hand rule.

## 2. Geometric Interpretation

> [!important] Circulation and Curl
> The left-hand side measures circulation around the boundary curve.
>
> The right-hand side measures the total flux of curl through the surface.
>
> Therefore, the total boundary circulation equals the accumulated local rotational contribution across the surface.

## 3. Orientation

> [!important] Right-Hand Rule
> The orientation of the boundary curve and the surface normal must be compatible.
>
> Point the thumb of the right hand in the direction of the chosen normal. The curled fingers indicate the positive direction of traversal along the boundary.
>
> Reversing the normal requires reversing the boundary orientation.

## 4. Important Consequences

> [!important] Surface Independence
> If two suitably oriented surfaces share the same boundary curve, and the vector field is sufficiently smooth on a region containing both surfaces and the region between them, their curl flux integrals are equal.
>
> Both equal the same boundary circulation.

> [!important] Curl-Free Fields
> If:
>
> $$\nabla\times\mathbf{F}=\mathbf{0}$$
>
> throughout an appropriate surface, then:
>
> $$\oint_{\partial S}\mathbf{F}\cdot d\mathbf{r}=0$$
>
> This conclusion concerns the boundary curves that bound the relevant surfaces.

## 5. Relationship with Green's Theorem

> [!important] Generalization
> Green's Theorem is a special planar case of Stokes' Theorem.
>
> In Green's Theorem, the surface is a region in the $xy$-plane, and its boundary is a planar closed curve.
>
> Stokes' Theorem extends the relationship to oriented surfaces embedded in three-dimensional space.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Curl:** Provides the local rotational quantity integrated over the surface.
- **Line Integrals:** Provides the boundary circulation.
- **Surface Integrals:** Provides integration of curl through an oriented surface.
- **Vector Fields:** Provides the field to which the theorem is applied.

### Downstream Knowledge
- **Generalized Stokes' Theorem:** Extends the theorem using differential forms.
- **Differential Geometry:** Provides the mathematical setting for integration over manifolds.
- **Differential Forms:** Unifies Stokes' Theorem with other fundamental integral theorems.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Hubbard, J. H., and Hubbard, B. B. *Vector Calculus, Linear Algebra, and Differential Forms: A Unified Approach*. 5th edition, 2015.