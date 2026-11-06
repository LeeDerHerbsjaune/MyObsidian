---
type: technical-term
title: Vector Calculus
aliases: []
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Multivariable Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - calculus
  - vector-calculus
sources: []
related:
  - "[[Scalar Fields]]"
  - "[[Vector Fields]]"
  - "[[Divergence]]"
  - "[[Curl]]"
  - "[[Line Integrals]]"
  - "[[Surface Integrals]]"
  - "[[Volume Integrals]]"
  - "[[Conservative Vector Fields]]"
  - "[[Green's Theorem]]"
  - "[[Stokes' Theorem]]"
  - "[[Divergence Theorem]]"
projects: []
---

> [!abstract] Definition
> **Vector Calculus** is the branch of mathematics that studies scalar and vector fields using differentiation and integration in multidimensional spaces.
>
> It develops differential operators such as the gradient, divergence, and curl, together with integration over curves, surfaces, and volumes.
>
> Its central purpose is to describe how fields vary locally and how their behavior accumulates over geometric domains.

> [!info] Scope
> This subject focuses on:
> - Scalar and vector fields.
> - Differential operators acting on fields.
> - Line, surface, and volume integrals.
> - Integral theorems connecting local differential behavior with global integral quantities.
>
> Vector Calculus primarily concerns fields defined over Euclidean spaces, especially two- and three-dimensional spaces.

## 1. Mathematical Setting

> [!definition] Scalar and Vector Fields
> A scalar field assigns a scalar value to each point in a domain:
>
> $$f:\Omega\subseteq\mathbb{R}^n\rightarrow\mathbb{R}$$
>
> A vector field assigns a vector to each point:
>
> $$\mathbf{F}:\Omega\subseteq\mathbb{R}^n\rightarrow\mathbb{R}^m$$
>
> In three-dimensional Euclidean space, a vector field commonly has the form:
>
> $$\mathbf{F}(x,y,z)=
> \begin{bmatrix}
> P(x,y,z)\\
> Q(x,y,z)\\
> R(x,y,z)
> \end{bmatrix}$$

> [!important] Geometric Interpretation
> - A scalar field describes a spatially varying quantity.
> - A vector field describes a spatially varying magnitude and direction.
> - Differential operators characterize local variation and structure.
> - Integrals measure accumulated quantities over curves, surfaces, and volumes.

## 2. Core Structure

### 2.1 Fields

> [!abstract] Field Representation
> - **Scalar Fields:** Assign scalar values to spatial points.
> - **Vector Fields:** Assign vectors to spatial points.
>
> These fields are the fundamental objects studied in Vector Calculus.

### 2.2 Differential Operators

> [!abstract] Local Differential Analysis
> Differential operators describe how fields vary in space.
>
> - **Gradient:** Measures the direction and rate of greatest increase of a scalar field.
> - **Divergence:** Measures the local net outward flux density of a vector field.
> - **Curl:** Measures the local rotational tendency of a vector field in three dimensions.

### 2.3 Integral Calculus over Geometric Domains

> [!abstract] Geometric Integration
> Integrals accumulate field quantities over geometric objects.
>
> - **Line Integrals:** Integrate scalar or vector quantities along curves.
> - **Surface Integrals:** Integrate scalar or vector quantities over surfaces.
> - **Volume Integrals:** Integrate scalar quantities over three-dimensional regions.

### 2.4 Integral Theorems

> [!abstract] Fundamental Integral Relationships
> Integral theorems connect local differential operators with global integrals.
>
> - **Green's Theorem:** Relates circulation or flux around a planar boundary to a double integral over the enclosed region.
> - **Stokes' Theorem:** Relates circulation around a surface boundary to the surface integral of curl.
> - **Divergence Theorem:** Relates outward flux through a closed surface to the volume integral of divergence.

## 3. Fundamental Mathematical Operators

> [!important] Del Operator
> The differential operators of classical Vector Calculus are expressed using the del operator:
>
> $$\nabla=
> \begin{bmatrix}
> \frac{\partial}{\partial x}\\
> \frac{\partial}{\partial y}\\
> \frac{\partial}{\partial z}
> \end{bmatrix}$$
>
> Its action depends on the mathematical object to which it is applied.
>
> - $\nabla f$: Gradient of a scalar field.
> - $\nabla\cdot\mathbf{F}$: Divergence of a vector field.
> - $\nabla\times\mathbf{F}$: Curl of a vector field.

## 4. Fundamental Integral Theorems

> [!important] Green's Theorem
> For a positively oriented, piecewise-smooth, simple closed curve $C$ bounding a planar region $D$:
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
> It relates planar circulation around a boundary to the scalar curl integrated over the enclosed region.
>
> A corresponding flux form also exists.

> [!important] Stokes' Theorem
> For an oriented smooth surface $S$ with positively oriented boundary $\partial S$:
>
> $$\oint_{\partial S}\mathbf{F}\cdot d\mathbf{r}
> =
> \iint_S(\nabla\times\mathbf{F})\cdot\mathbf{n}\,dS$$
>
> It relates the circulation along a boundary curve to the flux of curl through the surface.

> [!important] Divergence Theorem
> For a sufficiently regular volume $V$ with closed boundary surface $\partial V$ and outward unit normal $\mathbf{n}$:
>
> $$\iint_{\partial V}\mathbf{F}\cdot\mathbf{n}\,dS
> =
> \iiint_V(\nabla\cdot\mathbf{F})\,dV$$
>
> It relates the outward flux through a closed surface to the total divergence inside the enclosed volume.

## 5. Conceptual Relationships

> [!abstract] Relationship Between Differential and Integral Calculus
> Vector Calculus generalizes the central relationship of single-variable calculus:
>
> - Differentiation describes local behavior.
> - Integration describes accumulated behavior.
> - Integral theorems establish relationships between local derivatives and global integrals.
>
> The three major integral theorems are higher-dimensional generalizations of the Fundamental Theorem of Calculus.

> [!note] Conceptual Dependencies
> 1. Scalar and vector fields establish the objects being studied.
> 2. Gradient, divergence, and curl characterize local field behavior.
> 3. Line, surface, and volume integrals quantify field quantities over geometric domains.
> 4. Green's, Stokes', and the Divergence Theorems connect differential operators to geometric integrals.
> 5. Conservative vector fields connect potential functions, gradient fields, and path-independent line integrals.

## 6. Knowledge Relationships

### Foundation Knowledge

**Essential**
- **Multivariable Calculus:** Provides partial derivatives, multiple integrals, coordinate transformations, and multivariable differentiation.
- **Linear Algebra:** Provides vector spaces, dot products, cross products, matrices, and linear transformations.
- **Three-Dimensional Euclidean Space:** Provides the geometric setting for vector fields, curves, surfaces, and volumes.

**Relevant**
- **Differential Calculus:** Provides the limiting and differentiation concepts underlying field operators.
- **Integral Calculus:** Provides the foundations of definite, multiple, and accumulated integration.
- **Coordinate Systems:** Supports the representation and computation of fields and integrals.

### Downstream Knowledge

**Relevant**
- **Differential Equations:** Uses gradient, divergence, and other field operators in equations describing spatially distributed systems.
- **Classical Field Theory:** Uses scalar and vector fields to model physical quantities.
- **Electromagnetism:** Uses divergence, curl, and integral theorems to formulate Maxwell's equations.

**Advanced**
- **Differential Geometry:** Generalizes vector calculus to curved spaces and manifolds.
- **Tensor Calculus:** Generalizes differential operations and field representations beyond elementary Euclidean vector calculus.
- **Differential Forms:** Provides a coordinate-independent mathematical framework that unifies the major integral theorems.
- **Geometric Measure Theory:** Extends integration and geometric analysis to more general spaces and irregular domains.

## 7. Scope Boundaries

> [!warning] Topics Outside This Note
> This note organizes Vector Calculus rather than teaching every downstream discipline.
>
> - Differential Equations should contain the independent theory of ordinary and partial differential equations.
> - Differential Geometry should contain manifolds, tangent spaces, differential forms, and geometric structures.
> - Tensor Calculus should contain tensor operations and their coordinate transformations.
> - Electromagnetism should contain its physical laws and field equations.
>
> These subjects use Vector Calculus but have independent conceptual structures.

## 8. Further Development

> [!todo] Recommended Study Order
> 1. Scalar Fields
> 2. Vector Fields
> 3. Gradient
> 4. Divergence
> 5. Curl
> 6. Line Integrals
> 7. Conservative Vector Fields
> 8. Surface Integrals
> 9. Volume Integrals
> 10. Green's Theorem
> 11. Stokes' Theorem
> 12. Divergence Theorem
>
> This order is pedagogical rather than a strict dependency chain. In particular, surface and volume integration can be studied before all differential operators are mastered.

## 9. References

> [!bibliography] Recommended References
> - Marsden, J. E., and Tromba, A. J. *Vector Calculus*. 6th edition, 2012.
> - Stewart, J. *Calculus: Early Transcendentals*. 8th edition, 2015.
> - Hubbard, J. H., and Hubbard, B. B. *Vector Calculus, Linear Algebra, and Differential Forms: A Unified Approach*. 5th edition, 2015.