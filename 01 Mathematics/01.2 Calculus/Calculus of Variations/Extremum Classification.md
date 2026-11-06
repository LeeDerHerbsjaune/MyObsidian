---
type: technical-term
title: "Extremum Classification"
aliases:
  - Classification of Variational Extrema
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
> **Extremum classification** in the calculus of variations concerns determining whether a stationary function is a local minimum, local maximum, or neither.
>
> It requires examining the behavior of the functional under admissible perturbations.

## 2. Types of Extrema

> [!note] Local Minimum
> A function $y^*$ is a local minimum if there exists a suitable neighborhood of $y^*$ such that:
>
> $$J[y]\geq J[y^*]$$
>
> for every admissible $y$ in that neighborhood.

> [!note] Local Maximum
> A function $y^*$ is a local maximum if:
>
> $$J[y]\leq J[y^*]$$
>
> for every admissible $y$ in a suitable neighborhood.

> [!note] Global Extremum
> A global minimum or maximum satisfies the corresponding inequality over the entire admissible class.

> [!note] Saddle-Type Stationary Function
> A stationary function may have admissible perturbation directions that increase the functional and other directions that decrease it. Such a function is not a local extremum.

## 3. First- and Second-Order Conditions

> [!important] First-Order Necessary Condition
> Under appropriate assumptions, a local extremum must satisfy:
>
> $$\delta J[y^*;\eta]=0$$
>
> for every admissible variation $\eta$.
>
> This is the stationarity condition.

> [!important] Second-Order Necessary Conditions
> At a sufficiently regular local minimum:
>
> $$\delta^2J[y^*;\eta]\geq 0$$
>
> At a sufficiently regular local maximum:
>
> $$\delta^2J[y^*;\eta]\leq 0$$
>
> These conditions are necessary under suitable assumptions, but they are not generally sufficient.

## 4. Sufficient Conditions

> [!note] Positive Definiteness
> If the second variation is strictly positive for every nonzero admissible variation, with appropriate uniformity and regularity conditions, this can establish a strict local minimum.
>
> Similarly, strict negativity can establish a strict local maximum.
>
> The exact sufficient conditions depend on the function space, topology, and variational problem.

> [!warning] Degenerate Cases
> If the second variation vanishes in some nonzero directions, second-order tests may be inconclusive. Higher-order terms or other analytical methods may be necessary.

## 5. Local Versus Global Optimality

> [!important] Distinction
> Local optimality concerns perturbations near a candidate function.
>
> Global optimality compares the candidate with every admissible function.
>
> A local minimum need not be a global minimum. Convexity and other structural properties of the functional can help establish global optimality.

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **First Variation:** Establishes the stationarity condition.
> - **Second Variation:** Provides second-order information.
> - **Admissible Functions:** Determine the domain over which optimality is assessed.
>
> [!note] Downstream Knowledge
> - **Convex Analysis:** Provides tools for establishing global optimality.
> - **Direct Methods:** Develop existence results for minimizers.
> - **Functional Analysis:** Supplies the function-space framework for rigorous optimality analysis.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Dacorogna, B. (2008). *Direct Methods in the Calculus of Variations*. Springer.