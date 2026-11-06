---
type: technical-term
title: "Boundary Conditions"
aliases:
  - Variational Boundary Conditions
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus of Variations
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Boundary conditions** specify restrictions imposed on admissible functions or their derivatives at the boundary of the domain of a variational problem.
>
> They determine the admissible class and contribute to the boundary terms arising in the first variation.

## 2. Fixed and Free Endpoints

> [!important] Fixed Endpoints
> For a function defined on $[a,b]$, fixed endpoint conditions prescribe:
>
> $$y(a)=A,\qquad y(b)=B$$
>
> The admissible variations must satisfy:
>
> $$\eta(a)=\eta(b)=0$$

> [!important] Free Endpoints
> If an endpoint value is free, its variation need not vanish.
>
> The boundary term in the first variation must then vanish through an additional condition, producing a natural boundary condition.

## 3. Boundary Terms

> [!note] First Variation Boundary Term
> For:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> integration by parts gives:
>
> $$\delta J=
> [L_{y'}\eta]_a^b+
> \int_a^b
> \left(L_y-\frac{d}{dx}L_{y'}\right)\eta\,dx$$
>
> At a free endpoint, the corresponding boundary variation is unrestricted. For a simple free endpoint with freely varying $y$ and fixed endpoint location, the natural condition is:
>
> $$L_{y'}=0$$
>
> More general endpoint configurations produce more general transversality conditions.

## 4. Types of Boundary Conditions

> [!note] Essential Boundary Conditions
> These prescribe the value of the function itself, such as:
>
> $$y(a)=A$$
>
> They restrict the admissible function space directly.

> [!note] Natural Boundary Conditions
> These arise from the boundary terms in the variational stationarity condition.
>
> They commonly prescribe quantities involving derivatives of the Lagrangian.

> [!note] Mixed Boundary Conditions
> These combine prescribed function values with natural conditions or other boundary restrictions.

## 5. Higher-Order Problems

> [!important] Higher-Order Boundary Data
> If the functional depends on derivatives up to order $n$, integration by parts produces multiple boundary terms.
>
> Consequently, the problem may require boundary data involving:
>
> $$y,\ y',\ \ldots,\ y^{(n-1)}$$
>
> The precise conditions depend on which endpoint quantities are fixed and which are free.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Admissible Functions:** Boundary conditions restrict the admissible class.
> - **Variations:** Boundary restrictions determine allowable perturbations.
> - **First Variation:** Produces the boundary terms.
>
> [!note] Downstream Knowledge
> - **Euler–Lagrange Equation:** Must be combined with appropriate boundary conditions.
> - **Constrained Variational Problems:** Introduce additional boundary and interior restrictions.
> - **Higher-Order Variational Problems:** Require more involved boundary conditions.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Liberzon, D. (2012). *Calculus of Variations and Optimal Control Theory*. Princeton University Press.