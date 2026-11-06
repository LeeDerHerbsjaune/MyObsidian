---
type: technical-term
title: "Multiple Dependent Variables"
aliases:
  - Variational Problems with Multiple Dependent Variables
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
> **Variational problems with multiple dependent variables** involve functionals whose integrands depend on two or more unknown functions and their derivatives.
>
> Instead of optimizing a single function, the problem seeks a collection of functions that jointly make the functional stationary or extremal.

## 2. Mathematical Formulation

> [!important] Vector-Valued Unknown Function
> Let:
>
> $$\mathbf{y}(x)=
> \begin{bmatrix}
> y_1(x)\\
> y_2(x)\\
> \vdots\\
> y_m(x)
> \end{bmatrix}$$
>
> Consider the functional:
>
> $$J[\mathbf{y}]
> =
> \int_a^b
> L(x,y_1,\ldots,y_m,y_1',\ldots,y_m')\,dx$$
>
> The objective is to determine the functions $y_1,\ldots,y_m$ that make $J$ stationary, subject to the admissibility conditions.

## 3. Euler–Lagrange System

> [!important] Generalized Euler–Lagrange Equations
> Each dependent variable produces one Euler–Lagrange equation:
>
> $$\boxed{
> \frac{\partial L}{\partial y_i}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial L}{\partial y_i'}
> \right)=0,
> \qquad i=1,\ldots,m
> }$$
>
> The resulting equations form a coupled or uncoupled system of differential equations, depending on the structure of $L$.

## 4. First Variation

> [!note] Vector Perturbation
> Introduce a variation for each dependent variable:
>
> $$y_{i,\varepsilon}(x)
> =
> y_i(x)+\varepsilon\eta_i(x)$$
>
> The first variation becomes:
>
> $$\delta J=
> \int_a^b
> \sum_{i=1}^{m}
> \left(
> L_{y_i}\eta_i+
> L_{y_i'}\eta_i'
> \right)dx$$
>
> Applying integration by parts independently to each component gives the system of Euler–Lagrange equations when the variations are arbitrary in the interior.

## 5. Interpretation

> [!note] Coupled Variational Systems
> The dependent variables may interact through the Lagrangian.
>
> For example, the integrand may contain products or nonlinear combinations of several functions and their derivatives.
>
> The stationarity conditions must therefore be solved as a system rather than as unrelated scalar equations.

> [!example] Two Dependent Variables
> For:
>
> $$J[y,z]=\int_a^b L(x,y,z,y',z')\,dx$$
>
> the equations are:
>
> $$L_y-\frac{d}{dx}L_{y'}=0$$
>
> $$L_z-\frac{d}{dx}L_{z'}=0$$

## 6. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Functionals:** Define the optimization objective.
> - **Variations:** Provide independent perturbations for each unknown function.
> - **Euler–Lagrange Equation:** Supplies the stationarity condition for each dependent variable.
> - **Linear Algebra:** Supports vector-valued representations and systems.
>
> [!note] Downstream Knowledge
> - **Multiple Independent Variables:** Extends variational problems to fields over multidimensional domains.
> - **Systems of Differential Equations:** The resulting Euler–Lagrange equations may form coupled systems.
> - **Field Theory:** Uses variational principles for multiple field components.

## 7. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Giaquinta, M., and Hildebrandt, S. (1996). *Calculus of Variations I: The Lagrangian Formalism*. Springer.