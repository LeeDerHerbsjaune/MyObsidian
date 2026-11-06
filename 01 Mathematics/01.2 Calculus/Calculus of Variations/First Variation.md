---
type: technical-term
title: "First Variation"
aliases:
  - First Functional Variation
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
> The **first variation** is the first-order derivative of a functional with respect to an admissible perturbation of its input function.
>
> It measures the first-order change of the functional in a selected variation direction.

## 2. Mathematical Formulation

> [!important] Definition
> Let $J[y]$ be a functional and let:
>
> $$y_\varepsilon=y+\varepsilon\eta$$
>
> The first variation is:
>
> $$\boxed{
> \delta J[y;\eta]
> =
> \left.
> \frac{d}{d\varepsilon}
> J[y+\varepsilon\eta]
> \right|_{\varepsilon=0}
> }$$
>
> Here, $\eta$ is an admissible variation.

## 3. First Variation of an Integral Functional

> [!important] Classical Derivation
> Consider:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> Under the perturbation $y_\varepsilon=y+\varepsilon\eta$:
>
> $$J[y_\varepsilon]
> =
> \int_a^b
> L(x,y+\varepsilon\eta,y'+\varepsilon\eta')\,dx$$
>
> Differentiating at $\varepsilon=0$ gives:
>
> $$\delta J[y;\eta]
> =
> \int_a^b
> \left(
> \frac{\partial L}{\partial y}\eta
> +
> \frac{\partial L}{\partial y'}\eta'
> \right)dx$$
>
> Applying integration by parts:
>
> $$\delta J[y;\eta]
> =
> \left[
> \frac{\partial L}{\partial y'}\eta
> \right]_a^b
> +
> \int_a^b
> \left[
> \frac{\partial L}{\partial y}
> -
> \frac{d}{dx}
> \left(\frac{\partial L}{\partial y'}\right)
> \right]\eta\,dx$$

## 4. Stationarity Condition

> [!important] Necessary Condition
> If $y$ is a sufficiently regular local extremum and admissible perturbations can be taken in both positive and negative directions, then:
>
> $$\delta J[y;\eta]=0$$
>
> for every admissible variation $\eta$.
>
> For fixed endpoints, the boundary term vanishes. The resulting condition leads to the Euler–Lagrange equation.

> [!warning] Interpretation
> A vanishing first variation establishes stationarity under the relevant assumptions. It does not by itself prove that the function is a minimum or maximum.

## 5. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Functionals:** The first variation measures changes in a functional.
> - **Variations:** Define the perturbation direction.
> - **Integration by Parts:** Essential in the classical derivation.
>
> [!note] Downstream Knowledge
> - **Euler–Lagrange Equation:** Obtained from the stationarity condition.
> - **Boundary Conditions:** Arise from the boundary term.
> - **Second Variation:** Extends the analysis to second-order changes.
> - **Extremum Classification:** Uses first- and second-order conditions.

## 6. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.