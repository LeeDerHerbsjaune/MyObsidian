---
type: technical-term
title: Calculus of Variations
aliases:
  - Variational Calculus
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
  - calculus
  - optimization
sources: []
related:
  - "[[Functionals]]"
  - "[[Admissible Functions]]"
  - "[[Variations]]"
  - "[[First Variation]]"
  - "[[Boundary Conditions]]"
  - "[[Second Variation]]"
  - "[[Extremum Classification]]"
  - "[[Constraints]]"
  - "[[Multiple Dependent Variables]]"
  - "[[Multiple Independent Variables]]"
  - "[[Euler–Lagrange Equation]]"
projects: []
---

> [!abstract] Definition
> **Calculus of Variations** is a branch of mathematical analysis concerned with finding extrema of functionals defined over spaces of admissible functions.
>
> Instead of optimizing a function with respect to finite-dimensional variables, it seeks an entire function or curve that minimizes or maximizes a given functional.

> [!note] Scope
> This subject studies:
> - Functionals and admissible function spaces.
> - Variations and first-order variations.
> - Necessary conditions for extrema.
> - Euler–Lagrange equations.
> - Boundary conditions and constraints.
> - Second-order variations and sufficient conditions.
> - Variational problems involving multiple independent and dependent variables.
>
> Its central objective is to derive mathematical conditions that candidate optimal functions must satisfy.

## 2. Definition and Core Concepts

> [!important] Functionals
> A **functional** is a mapping whose input is a function and whose output is typically a real number.
>
> A general functional can be represented as:
>
> $$
> J[y] = \mathcal{F}(y)
> $$
>
> where:
> - $y$ is an admissible function.
> - $\mathcal{F}$ is an operator acting on functions.
> - $J[y]$ is the scalar value assigned to the function.
>
> A common integral functional is:
>
> $$
> J[y] =
> \int_a^b
> L(x,y(x),y'(x))\,dx
> $$
>
> Here, $L$ is called the **Lagrangian** or **Lagrangian density** in this one-dimensional setting.

> [!important] Variational Problem
> A variational problem seeks a function $y^*$ that minimizes or maximizes a functional:
>
> $$
> y^* = \underset{y\in\mathcal{A}}{\operatorname{arg\,min}}\,J[y]
> $$
>
> where $\mathcal{A}$ is the set of admissible functions satisfying the problem's boundary conditions and other constraints.
>
> Unlike ordinary optimization, the unknown is an entire function rather than a finite-dimensional vector.

> [!important] Variation
> A **variation** describes a perturbation of an admissible function.
>
> Consider a family of functions:
>
> $$
> y_\varepsilon(x)=y(x)+\varepsilon\eta(x)
> $$
>
> where:
> - $y(x)$ is the candidate function.
> - $\eta(x)$ is an admissible perturbation.
> - $\varepsilon$ is a scalar parameter.
>
> For fixed endpoints, the variation generally satisfies:
>
> $$
> \eta(a)=\eta(b)=0
> $$
>
> The perturbation is used to examine how the functional changes near the candidate function.

## 3. First Variation and Stationary Functions

> [!important] First Variation
> The **first variation** measures the first-order change of a functional under an admissible perturbation.
>
> It is defined as:
>
> $$
> \delta J[y;\eta]
> =
> \left.
> \frac{d}{d\varepsilon}
> J[y+\varepsilon\eta]
> \right|_{\varepsilon=0}
> $$
>
> If $y^*$ is a sufficiently regular local extremum in the interior of the admissible function space, a necessary condition is:
>
> $$
> \delta J[y^*;\eta]=0
> $$
>
> for every admissible variation $\eta$.

> [!note] Stationary Function
> A function satisfying the vanishing first variation condition is called a **stationary function** or **extremal**.
>
> A stationary function is a candidate for a minimum or maximum, but the vanishing first variation alone does not establish that an extremum exists or determine its type.

## 4. Euler–Lagrange Equation

> [!important] Euler–Lagrange Equation
> For an integral functional:
>
> $$
> J[y]=\int_a^b L(x,y,y')\,dx
> $$
>
> a sufficiently smooth stationary function with fixed endpoints satisfies:
>
> $$
> \boxed{
> \frac{\partial L}{\partial y}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial L}{\partial y'}
> \right)=0
> }
> $$
>
> This is the **Euler–Lagrange equation**, the fundamental necessary condition of classical variational calculus.
>
> It transforms an optimization problem over functions into a differential equation that stationary functions must satisfy.

> [!note] Derivation Principle
> The Euler–Lagrange equation follows from:
> 1. Perturbing the candidate function.
> 2. Differentiating the perturbed functional with respect to the perturbation parameter.
> 3. Applying integration by parts.
> 4. Using the vanishing boundary variations.
> 5. Applying the fundamental lemma of the calculus of variations.
>
> The resulting differential equation is a necessary stationarity condition.

## 5. Boundary Conditions

> [!important] Boundary Conditions
> Boundary conditions determine which functions are admissible and influence the form of the variational equations.
>
> Common cases include:
>
> - **Fixed endpoints:** The function values are prescribed at the boundaries.
> - **Free endpoints:** One or both endpoint values may vary.
> - **Mixed conditions:** Some boundary quantities are prescribed while others remain free.
>
> When endpoints are free, integration by parts produces additional boundary conditions, commonly called **natural boundary conditions** or **transversality conditions**, depending on the problem.

## 6. Higher-Order and Generalized Variational Problems

> [!note] Higher-Order Variational Problems
> Some functionals depend on higher-order derivatives:
>
> $$
> J[y]=
> \int_a^b
> L(x,y,y',y'',\ldots,y^{(n)})\,dx
> $$
>
> Their Euler–Lagrange equation generalizes to:
>
> $$
> \sum_{k=0}^{n}
> (-1)^k
> \frac{d^k}{dx^k}
> \left(
> \frac{\partial L}{\partial y^{(k)}}
> \right)=0
> $$
>
> Appropriate boundary conditions must account for the additional derivatives.

> [!note] Multiple Dependent Variables
> For several unknown functions $y_1,\ldots,y_m$, the Euler–Lagrange equations become a system:
>
> $$
> \frac{\partial L}{\partial y_i}
> -
> \frac{d}{dx}
> \left(
> \frac{\partial L}{\partial y_i'}
> \right)=0,
> \qquad i=1,\ldots,m
> $$

> [!note] Multiple Independent Variables
> Variational problems can also involve fields defined over multidimensional domains.
>
> For a scalar field $u(\mathbf{x})$ and a functional:
>
> $$
> J[u]=
> \int_\Omega
> L(\mathbf{x},u,\nabla u)\,d\mathbf{x}
> $$
>
> the corresponding Euler–Lagrange equation is:
>
> $$
> \frac{\partial L}{\partial u}
> -
> \nabla\cdot
> \left(
> \frac{\partial L}{\partial(\nabla u)}
> \right)=0
> $$
>
> This extends variational analysis from curves and functions of one variable to fields over multidimensional domains.

## 7. Second Variation and Extremum Classification

> [!important] Second Variation
> The **second variation** examines the second-order change of a functional under perturbations:
>
> $$
> \delta^2J[y;\eta]
> =
> \left.
> \frac{d^2}{d\varepsilon^2}
> J[y+\varepsilon\eta]
> \right|_{\varepsilon=0}
> $$
>
> Under suitable regularity and admissibility conditions:
>
> - Positive second variation is associated with a local minimum.
> - Negative second variation is associated with a local maximum.
> - An indefinite or degenerate second variation requires further analysis.
>
> The second variation provides necessary and, under stronger conditions, sufficient information for classifying stationary functions.

## 8. Constraints in Variational Problems

> [!note] Constrained Variational Problems
> Some variational problems impose additional restrictions on admissible functions.
>
> Examples include:
> - Integral constraints.
> - Pointwise constraints.
> - Boundary constraints.
> - Isoperimetric constraints.
>
> Integral constraints can often be incorporated through Lagrange multipliers, producing modified Euler–Lagrange equations.
>
> More general constraints require additional analytical tools.

## 9. Limitations and Mathematical Considerations

> [!warning] Important Distinctions
> - Satisfying the Euler–Lagrange equation does not guarantee a global minimum or maximum.
> - A stationary function need not be an extremizer.
> - Existence of an optimizer requires additional assumptions about the functional and admissible function space.
> - Smoothness and differentiability assumptions are important when deriving classical Euler–Lagrange equations.
> - Boundary conditions are part of the mathematical problem, not merely supplementary information.
>
> Modern variational analysis often uses functional analysis, weak derivatives, Sobolev spaces, and lower semicontinuity to address existence and regularity questions.

## 10. Knowledge Relationships

> [!note] Foundation Knowledge
> **Essential**
> - Single-Variable Calculus — differentiation, integration, and integration by parts are central to classical variational derivations.
> - Differential Equations — Euler–Lagrange equations are differential equations governing stationary functions.
>
> **Relevant**
> - Real Analysis — provides rigorous foundations for convergence, continuity, differentiability, and integration.
> - Multivariable Calculus — supports problems involving multiple variables, partial derivatives, and gradients.
> - Linear Algebra — supports quadratic forms and second-variation analysis.
> - Functional Analysis — provides the framework for studying function spaces and functionals rigorously.

> [!note] Downstream Knowledge
> **Relevant**
> - Functional Analysis — develops the abstract theory of spaces of functions, operators, and functionals.
> - Partial Differential Equations — many PDEs arise as Euler–Lagrange equations of variational functionals.
> - Optimal Control Theory — connects variational optimization with optimization of dynamical systems.
>
> **Advanced**
> - Geometric Calculus of Variations — studies variational problems involving geometric objects such as curves, surfaces, and manifolds.
> - Direct Methods in the Calculus of Variations — develops existence theory using compactness and lower semicontinuity.
> - Variational Methods for Nonlinear PDEs — applies variational principles to establish solutions of nonlinear differential equations.

## 11. Further Development

> [!todo] Recommended Independent Notes
> The following subjects and concepts are suitable for further decomposition:
>
> - Functionals
> - Variations and First Variation
> - Euler–Lagrange Equation
> - Boundary Conditions and Transversality
> - Second Variation
> - Constrained Variational Problems
> - Isoperimetric Problems
> - Direct Methods in the Calculus of Variations
> - Variational Problems for Multiple Integrals
>
> These are proposed note boundaries, not necessarily a list of equally independent subjects. Their granularity should be evaluated as the knowledge base develops.

## 12. References

> [!note] Recommended References
> - Gelfand, I. M., and Fomin, S. V. (1963). *Calculus of Variations*. Prentice-Hall.
> - Liberzon, D. (2012). *Calculus of Variations and Optimal Control Theory: A Concise Introduction*. Princeton University Press.
> - Giaquinta, M., and Hildebrandt, S. (1996). *Calculus of Variations I: The Lagrangian Formalism*. Springer.