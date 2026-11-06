---
type: technical-term
title: "Admissible Functions"
aliases:
  - Admissible Curves
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
  - function-spaces
sources: []
related: []
projects: []
---

> [!abstract] Definition
> **Admissible functions** are functions that satisfy the regularity, boundary, and other constraints specified by a variational problem.
>
> They form the set over which a functional is optimized.

## 2. Mathematical Representation

> [!important] Admissible Function Class
> Let a variational problem be defined by:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> Its admissible class can be written as:
>
> $$\mathcal{A}=\{y\in X:y(a)=A,\ y(b)=B\}$$
>
> where $X$ is an appropriate function space and $A,B$ are prescribed endpoint values.
>
> The minimization problem is:
>
> $$\inf_{y\in\mathcal{A}}J[y]$$

## 3. Requirements for Admissibility

> [!note] Regularity
> An admissible function must possess sufficient regularity for the functional to be well-defined.
>
> In classical problems, this may require continuous differentiability. In more general problems, weaker conditions such as absolute continuity or membership in a Sobolev space may be sufficient.

> [!note] Boundary Conditions
> Admissible functions may be required to satisfy prescribed endpoint values:
>
> $$y(a)=A,\qquad y(b)=B$$

> [!note] Additional Constraints
> Admissibility may also require:
> - Integral constraints.
> - Pointwise restrictions.
> - Periodicity.
> - Geometric or physical restrictions.
>
> These conditions determine which functions are allowed in the optimization problem.

## 4. Admissible Class and Existence

> [!important] Admissible Set
> The admissible class defines the search space of the variational problem.
>
> The existence of an admissible function does not automatically guarantee that a minimizer exists.
>
> Existence requires additional mathematical conditions on the functional and the admissible space.

> [!warning] Important Distinction
> An admissible function is not necessarily an optimizer or stationary function. It only satisfies the problem's requirements.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Function Spaces:** Define the mathematical environment containing admissible functions.
> - **Boundary Conditions:** Specify restrictions at the boundaries.
> - **Real Analysis:** Provides regularity and convergence concepts.
>
> [!note] Downstream Knowledge
> - **Variations:** Perturbations must respect admissibility.
> - **First Variation:** Requires admissible perturbations around a candidate function.
> - **Constrained Variational Problems:** Introduce additional restrictions on admissible functions.
> - **Direct Methods:** Study existence of minimizers within admissible classes.

## 6. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Dacorogna, B. (2008). *Direct Methods in the Calculus of Variations*. Springer.