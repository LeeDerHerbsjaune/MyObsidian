---
type: technical-term
title: "Surface Integrals"
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Vector Calculus
  - Integral Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - vector-calculus
  - integration
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **Surface Integral** is an integral that accumulates scalar or vector quantities over a surface embedded in a higher-dimensional space.
>
> Surface integrals generalize ordinary double integrals by incorporating the geometry and orientation of a surface.

## 1. Surface Parameterization

> [!definition] Parametric Surface
> A smooth surface $S$ can be parameterized by:
>
> $$\mathbf{r}(u,v)=
> \begin{bmatrix}
> x(u,v)\\
> y(u,v)\\
> z(u,v)
> \end{bmatrix}$$
>
> The tangent vectors are:
>
> $$\mathbf{r}_u=\frac{\partial\mathbf{r}}{\partial u},
> \qquad
> \mathbf{r}_v=\frac{\partial\mathbf{r}}{\partial v}$$
>
> The differential surface area is:
>
> $$dS=\|\mathbf{r}_u\times\mathbf{r}_v\|\,du\,dv$$

## 2. Scalar Surface Integrals

> [!definition] Scalar Integration over a Surface
> For a scalar field $f$ defined on a surface $S$:
>
> $$\iint_S f\,dS
> =
> \iint_D
> f(\mathbf{r}(u,v))
> \|\mathbf{r}_u\times\mathbf{r}_v\|
> \,du\,dv$$
>
> This integral accumulates scalar quantities over the surface area.

> [!example] Interpretation
> If $f$ represents surface mass density, then:
>
> $$m=\iint_Sf\,dS$$
>
> gives the total mass of a thin surface.

## 3. Vector Surface Integrals and Flux

> [!definition] Flux Integral
> For a vector field $\mathbf{F}$ and an oriented surface $S$:
>
> $$\iint_S\mathbf{F}\cdot\mathbf{n}\,dS$$
>
> where $\mathbf{n}$ is the chosen unit normal vector.
>
> The integral measures the net flow of the vector field through the oriented surface.

> [!important] Parametric Flux Formula
> For a parameterized surface:
>
> $$\iint_S\mathbf{F}\cdot\mathbf{n}\,dS
> =
> \iint_D
> \mathbf{F}(\mathbf{r}(u,v))
> \cdot(\mathbf{r}_u\times\mathbf{r}_v)
> \,du\,dv$$
>
> The cross product determines the orientation of the surface.

## 4. Orientation

> [!important] Surface Orientation
> An oriented surface has a consistent choice of normal direction.
>
> Reversing the normal changes the sign of the flux integral:
>
> $$\iint_S\mathbf{F}\cdot(-\mathbf{n})\,dS
> =
> -\iint_S\mathbf{F}\cdot\mathbf{n}\,dS$$
>
> Scalar surface integrals are independent of orientation.

> [!note] Closed Surfaces
> A closed surface encloses a three-dimensional region.
>
> Its outward orientation is defined by choosing normals directed away from the enclosed region.

## 5. Properties

> [!important] Linearity
> $$\iint_S(a\mathbf{F}+b\mathbf{G})\cdot\mathbf{n}\,dS
> =
> a\iint_S\mathbf{F}\cdot\mathbf{n}\,dS
> +b\iint_S\mathbf{G}\cdot\mathbf{n}\,dS$$

> [!important] Surface Decomposition
> If a surface is composed of pieces $S_1$ and $S_2$, the integral can be evaluated as the sum of the integrals over those pieces, with consistent orientations.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Parameterization of Surfaces:** Provides a mathematical representation of surfaces.
- **Multiple Integrals:** Provides the double integration used to compute surface integrals.
- **Vector Fields:** Provides the fields used in flux integrals.
- **Scalar Fields:** Provides the integrands for scalar surface integrals.

### Downstream Knowledge
- **Stokes' Theorem:** Relates surface integrals of curl to boundary circulation.
- **Divergence Theorem:** Relates closed-surface flux to volume divergence.
- **Flux Analysis:** Uses surface integrals to quantify field transport through surfaces.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Stewart, J. *Calculus: Early Transcendentals*. 8th edition, 2015.