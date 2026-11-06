---
type: technical-term
title: "Variations"
aliases:
  - Function Variations
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
> A **variation** is an admissible perturbation of a function used to investigate how a functional changes when its input function is modified.
>
> Variations provide the mathematical foundation for deriving necessary conditions for extrema.

## 2. Mathematical Representation

> [!important] Perturbed Function
> Given a candidate function $y(x)$, consider the one-parameter family:
>
> $$y_\varepsilon(x)=y(x)+\varepsilon\eta(x)$$
>
> where:
> - $y(x)$ is the original function.
> - $\eta(x)$ is the variation function.
> - $\varepsilon$ is a real perturbation parameter.
>
> The function $\eta$ describes the direction of perturbation in the function space.

## 3. Boundary Restrictions

> [!note] Fixed Endpoints
> If the endpoints are fixed:
>
> $$y(a)=A,\qquad y(b)=B$$
>
> then the perturbed function must preserve these values. Consequently:
>
> $$\eta(a)=\eta(b)=0$$
>
> The variation must also satisfy the required regularity conditions.

## 4. Variations of a Functional

> [!important] Induced Functional Variation
> A variation of the input function produces a scalar-valued function of $\varepsilon$:
>
> $$\Phi(\varepsilon)=J[y+\varepsilon\eta]$$
>
> Studying $\Phi$ near $\varepsilon=0$ reveals how the functional changes in the selected perturbation direction.
>
> Its first and second derivatives at zero define the first and second variations.

## 5. Interpretation

> [!note] Geometric Interpretation
> A function space can be viewed as a space of possible candidate functions.
>
> A variation $\eta$ represents a direction in which the candidate function is perturbed. The parameter $\varepsilon$ controls the perturbation magnitude.
>
> This is analogous to directional perturbations in finite-dimensional optimization, but the variables are functions.

> [!warning] Important Distinction
> A variation $\eta$ is not the same as the perturbed function $y_\varepsilon$. The former describes the perturbation direction; the latter is the resulting family of functions.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Functionals:** Variations investigate changes in functional values.
> - **Admissible Functions:** Perturbations must respect admissibility requirements.
> - **Function Spaces:** Provide the setting in which perturbations are defined.
>
> [!note] Downstream Knowledge
> - **First Variation:** Uses the first derivative with respect to the perturbation parameter.
> - **Second Variation:** Uses the second derivative.
> - **Euler–Lagrange Equation:** Follows from requiring the first variation to vanish.
> - **Extremum Classification:** Uses second-order variation information.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.