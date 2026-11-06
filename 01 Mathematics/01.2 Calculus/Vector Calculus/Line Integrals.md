---
type: technical-term
title: "Line Integrals"
aliases:
  - Curve Integrals
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
> A **Line Integral** is an integral that accumulates a scalar or vector quantity along a parameterized curve.
>
> Unlike ordinary definite integrals, which accumulate quantities over intervals, line integrals accumulate quantities over geometric paths.

## 1. Parameterization of a Curve

> [!definition] Curve Representation
> A smooth curve $C$ in three-dimensional space can be parameterized by:
>
> $$\mathbf{r}(t)=
> \begin{bmatrix}
> x(t)\\y(t)\\z(t)
> \end{bmatrix},
> \qquad a\leq t\leq b$$
>
> Its differential displacement is:
>
> $$d\mathbf{r}=\mathbf{r}'(t)\,dt$$
>
> The differential arc length is:
>
> $$ds=\|\mathbf{r}'(t)\|\,dt$$

## 2. Scalar Line Integrals

> [!definition] Scalar Integration Along a Curve
> For a scalar field $f$ defined along a piecewise-smooth curve $C$:
>
> $$\int_C f\,ds
> =
> \int_a^b f(\mathbf{r}(t))
> \|\mathbf{r}'(t)\|\,dt$$
>
> This integral accumulates scalar values weighted by arc length.
>
> It is independent of the orientation of the curve.

> [!example] Interpretation
> If $f$ represents linear mass density, then:
>
> $$m=\int_C f\,ds$$
>
> gives the total mass of a thin wire following the curve $C$.

## 3. Vector Line Integrals

> [!definition] Integration of a Vector Field
> For a vector field $\mathbf{F}$:
>
> $$\int_C\mathbf{F}\cdot d\mathbf{r}
> =
> \int_a^b
> \mathbf{F}(\mathbf{r}(t))
> \cdot\mathbf{r}'(t)\,dt$$
>
> This integral measures the tangential component of the vector field accumulated along the curve.

> [!important] Work and Circulation
> - In mechanics, the line integral can represent the work performed by a force along a path.
> - For a closed curve, it is commonly interpreted as circulation.
>
> The integral depends on the orientation of the curve.

## 4. Properties

> [!important] Linearity
> $$\int_C(a\mathbf{F}+b\mathbf{G})\cdot d\mathbf{r}
> =
> a\int_C\mathbf{F}\cdot d\mathbf{r}
> +b\int_C\mathbf{G}\cdot d\mathbf{r}$$

> [!important] Orientation Reversal
> If $-C$ denotes the same curve with reversed orientation:
>
> $$\int_{-C}\mathbf{F}\cdot d\mathbf{r}
> =
> -\int_C\mathbf{F}\cdot d\mathbf{r}$$
>
> For scalar line integrals:
>
> $$\int_{-C}f\,ds=\int_Cf\,ds$$

> [!important] Path Concatenation
> If a curve consists of consecutive pieces $C_1$ and $C_2$:
>
> $$\int_C\mathbf{F}\cdot d\mathbf{r}
> =
> \int_{C_1}\mathbf{F}\cdot d\mathbf{r}
> +
> \int_{C_2}\mathbf{F}\cdot d\mathbf{r}$$

## 5. Fundamental Theorem for Line Integrals

> [!important] Gradient Field Integration
> If $\mathbf{F}=\nabla f$ and $C$ runs from point $A$ to point $B$:
>
> $$\int_C\mathbf{F}\cdot d\mathbf{r}
> =
> f(B)-f(A)$$
>
> The integral depends only on the endpoints, not on the particular path.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Parameterization of Curves:** Describes the geometric paths over which integration occurs.
- **Integral Calculus:** Provides definite integration and limiting procedures.
- **Vector Fields:** Provides the fields integrated along curves.
- **Scalar Fields:** Provides the integrands for scalar line integrals.

### Downstream Knowledge
- **Conservative Vector Fields:** Explains path independence of vector line integrals.
- **Green's Theorem:** Relates planar closed line integrals to double integrals.
- **Stokes' Theorem:** Relates circulation to surface integrals of curl.

## 7. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Stewart, J. *Calculus: Early Transcendentals*. 8th edition, 2015.