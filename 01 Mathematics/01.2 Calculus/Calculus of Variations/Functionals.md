---
type: technical-term
title: "Functionals"
aliases: []
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
  - functional-analysis
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **functional** is a mapping whose input is a function and whose output is typically a scalar.
>
> Unlike an ordinary function, which maps elements of a domain to values, a functional maps functions to values.

> [!important] Mathematical Representation
> A functional can be represented abstractly as:
>
> $$J:\mathcal{A}\rightarrow\mathbb{R}$$
>
> where:
> - $\mathcal{A}$ is a space of admissible functions.
> - $J$ assigns a real number to each function in $\mathcal{A}$.
>
> A common integral functional is:
>
> $$J[y]=\int_a^b L(x,y(x),y'(x))\,dx$$
>
> Here, $L$ is the Lagrangian function, and $J[y]$ is the value of the functional evaluated at $y$.

## 2. Types of Functionals

> [!note] Integral Functionals
> An integral functional assigns a value through integration:
>
> $$J[y]=\int_a^b L(x,y,y')\,dx$$
>
> This is the standard form in classical calculus of variations.

> [!note] Functionals with Higher-Order Derivatives
> A functional may depend on derivatives beyond the first order:
>
> $$J[y]=\int_a^b L(x,y,y',y'',\ldots,y^{(n)})\,dx$$

> [!note] Functionals of Several Variables
> For a field $u:\Omega\rightarrow\mathbb{R}$:
>
> $$J[u]=\int_\Omega L(\mathbf{x},u,\nabla u)\,d\mathbf{x}$$

## 3. Optimization of Functionals

> [!important] Variational Optimization
> The central problem is to find a function $y^*$ that minimizes or maximizes the functional:
>
> $$y^*=\underset{y\in\mathcal{A}}{\operatorname{arg\,min}}J[y]$$
>
> This is an optimization problem over a function space rather than over a finite-dimensional vector space.

> [!warning] Important Distinction
> A functional is not necessarily an integral. Integral functionals are particularly important in classical variational calculus, but more general functionals can be defined through other mathematical constructions.

## 4. Knowledge Relationships

> [!note] Foundation Knowledge
> - **Functions and Function Spaces:** Functionals take functions as their inputs.
> - **Integral Calculus:** Classical integral functionals are defined through integration.
> - **Real Analysis:** Provides rigorous foundations for convergence and integration.
>
> [!note] Downstream Knowledge
> - **Variations:** Study perturbations of the input function.
> - **First Variation:** Measures the first-order change of a functional.
> - **Calculus of Variations:** Uses functionals as the central objects of optimization.
> - **Functional Analysis:** Develops the abstract theory of function spaces and functionals.

## 5. References

> [!note] References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Giaquinta, M., and Hildebrandt, S. (1996). *Calculus of Variations I: The Lagrangian Formalism*. Springer.