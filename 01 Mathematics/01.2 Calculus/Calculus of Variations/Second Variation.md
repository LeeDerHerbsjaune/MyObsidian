---
type: technical-term
title: "Second Variation"
aliases:
  - Second Functional Variation
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
> The **second variation** is the second-order derivative of a functional with respect to an admissible perturbation parameter.
>
> It describes the second-order change of the functional near a stationary function and provides information for classifying extrema.

## 2. Mathematical Formulation

> [!important] Definition
> Let:
>
> $$y_\varepsilon=y+\varepsilon\eta$$
>
> The second variation is:
>
> $$\boxed{
> \delta^2J[y;\eta]
> =
> \left.
> \frac{d^2}{d\varepsilon^2}
> J[y+\varepsilon\eta]
> \right|_{\varepsilon=0}
> }$$
>
> It measures the curvature of the functional along the perturbation direction $\eta$.

## 3. Second Variation of an Integral Functional

> [!note] Classical Form
> For:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> the second variation is:
>
> $$\delta^2J[y;\eta]
> =
> \int_a^b
> \left(
> L_{yy}\eta^2
> +2L_{yy'}\eta\eta'
> +L_{y'y'}(\eta')^2
> \right)dx$$
>
> All partial derivatives of $L$ are evaluated along the unperturbed function $y$.

## 4. Relation to Taylor Expansion

> [!important] Functional Expansion
> Under sufficient differentiability:
>
> $$J[y+\varepsilon\eta]
> =
> J[y]
> +\varepsilon\delta J[y;\eta]
> +\frac{\varepsilon^2}{2}\delta^2J[y;\eta]
> +o(\varepsilon^2)$$
>
> At a stationary function, the first-order term vanishes:
>
> $$J[y+\varepsilon\eta]
> =
> J[y]
> +\frac{\varepsilon^2}{2}\delta^2J[y;\eta]
> +o(\varepsilon^2)$$

## 5. Interpretation

> [!note] Positive and Negative Second Variations
> - Positive second variation in every nonzero admissible direction is associated with a strict local minimum under suitable regularity and coercivity conditions.
> - Negative second variation in every nonzero admissible direction is associated with a strict local maximum under suitable conditions.
> - An indefinite second variation indicates directions of both increase and decrease, ruling out a local extremum under the usual second-order assumptions.
> - A degenerate second variation may require higher-order analysis.

> [!warning] Important Distinction
> The second variation is a quadratic form on admissible perturbations. Its sign must be assessed over the relevant variation space, not merely for one arbitrarily selected perturbation.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Variations:** Define perturbation directions.
> - **First Variation:** Establishes stationarity.
> - **Functionals:** Provide the object being differentiated.
>
> [!note] Downstream Knowledge
> - **Extremum Classification:** Uses second-order information to assess candidate extrema.
> - **Second-Order Necessary and Sufficient Conditions:** Develop criteria for local optimality.
> - **Direct Methods:** Address existence independently of local second-order tests.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Giaquinta, M., and Hildebrandt, S. (1996). *Calculus of Variations I: The Lagrangian Formalism*. Springer.