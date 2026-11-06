---
type: technical-term
title: Differential Calculus
aliases:
  - Differential Calculus
  - Vi phân
field:
  - Mathematics
subfield:
  - Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - differential-calculus
sources: []
related:
  - "[[Derivatives]]"
  - "[[Differentiability]]"
  - "[[Differentiation Rules]]"
  - "[[Higher-Order Derivatives]]"
  - "[[Related Rates]]"
  - "[[Taylor Series and Taylor Approximation]]"
  - "[[Applications of Derivatives]]"
  - "[[Implicit Differentiation|Implicit Derivative]]"
projects: []
---

# Differential Calculus

> [!abstract] Definition
> Differential Calculus is a branch of calculus that studies the instantaneous rates of change of functions and the local behavior of mathematical relationships.
>
> Its central mathematical operation is differentiation, which determines derivatives describing how a function changes with respect to its independent variables.
>
> Differential calculus provides the mathematical foundations for analyzing slopes, rates of change, local extrema, function approximation, and optimization.

## 1. Mathematical Foundations

> [!info] Prerequisites
> Differential calculus relies on limits and continuity to establish the mathematical definition of derivatives and differentiability.

- Functions
- Real Numbers
- Limits
- Continuity
- Sequences and Series

## 2. Derivatives

> [!abstract] Definition
> A derivative measures the instantaneous rate of change of a function with respect to its independent variable.
>
> Geometrically, it represents the slope of the tangent line to a function's graph at a given point.

### Core Concepts

- Derivative Definition
- Geometric Interpretation of Derivatives
- Physical Interpretation of Derivatives
- Tangent Lines
- Normal Lines
- One-Sided Derivatives
- Derivative Notations

### Mathematical Formulation

The derivative of a function $f(x)$ at a point $x$ is defined as:

$$
f'(x)=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}
$$

> [!important] Key Principle
> A derivative is defined through a limiting process. Its existence requires the corresponding difference quotient to approach a finite limit.

## 3. Differentiability

> [!abstract] Definition
> Differentiability describes whether a function possesses a derivative at a given point or throughout a specified domain.
>
> It characterizes the local smoothness of a function and establishes conditions under which its behavior can be approximated linearly.

### Core Concepts

- Differentiability at a Point
- Differentiability on an Interval
- Differentiability and Continuity
- Local Linear Approximation
- Differentiability of Piecewise Functions
- Left and Right Differentiability
- Conditions for Non-Differentiability

> [!important] Fundamental Relationship
> Differentiability at a point implies continuity at that point, but continuity does not necessarily imply differentiability.

## 4. Differentiation Rules

> [!abstract] Definition
> Differentiation Rules are mathematical procedures used to calculate derivatives efficiently without repeatedly applying the limit definition.

### Core Rules

- Constant Rule
- Power Rule
- Constant Multiple Rule
- Sum and Difference Rules
- Product Rule
- Quotient Rule
- Chain Rule

### Derivatives of Elementary Functions

- Polynomial Functions
- Rational Functions
- Exponential Functions
- Logarithmic Functions
- Trigonometric Functions
- Inverse Trigonometric Functions
- Hyperbolic Functions

## 5. Higher-Order Derivatives

> [!abstract] Definition
> Higher-Order Derivatives are derivatives obtained by repeatedly differentiating a function.
>
> They describe successive rates of change and provide information about the local behavior and curvature of functions.

### Core Concepts

- Second Derivative
- Third Derivative
- Higher-Order Derivatives
- Derivative Notation
- Second Derivative Test
- Concavity and Convexity
- Inflection Points
- Leibniz's Rule

### Mathematical Formulation

$$
f''(x)=\frac{d^2f}{dx^2}
$$

The general $n$-th derivative is expressed as:

$$
f^{(n)}(x)=\frac{d^nf}{dx^n}
$$

## 6. Implicit Differentiation

> [!abstract] Definition
> Implicit Differentiation is a differentiation technique used when a relationship between variables is expressed implicitly rather than explicitly as a function.
>
> It differentiates both sides of an equation with respect to an independent variable while applying the chain rule to dependent variables.

### Core Concepts

- Explicit and Implicit Functions
- Implicit Differentiation Procedure
- Chain Rule in Implicit Differentiation
- First-Order Implicit Derivatives
- Higher-Order Implicit Derivatives
- Tangent Lines to Implicit Curves

### Mathematical Formulation

For an implicitly defined relationship:

$$
F(x,y)=0
$$

Differentiating with respect to $x$ gives:

$$
F_x+F_y\frac{dy}{dx}=0
$$

When $F_y\neq 0$:

$$
\frac{dy}{dx}=-\frac{F_x}{F_y}
$$

## 7. Related Rates

> [!abstract] Definition
> Related Rates is an application of differential calculus that determines how multiple quantities change with respect to time when those quantities are related by a mathematical equation.

### Core Concepts

- Time-Dependent Variables
- Relationships Between Changing Quantities
- Differentiation with Respect to Time
- Chain Rule Applications
- Rate of Change Problems
- Geometric Related Rates

### General Formulation

For a relationship:

$$
F(x,y)=0
$$

where $x$ and $y$ depend on time $t$:

$$
F_x\frac{dx}{dt}
+
F_y\frac{dy}{dt}=0
$$

## 8. Taylor Series and Taylor Approximation

> [!abstract] Definition
> Taylor Series represents a sufficiently differentiable function as an infinite power series around a specified expansion point, under appropriate convergence and equality conditions.
>
> Taylor Approximation uses a finite Taylor polynomial to approximate a function locally using its derivatives at an expansion point.

### Core Concepts

- Taylor Polynomial
- Taylor Series
- Maclaurin Series
- Expansion Point
- Taylor Coefficients
- Taylor Remainder
- Lagrange Remainder
- Order of Approximation
- Local Function Approximation
- Error Estimation

### Mathematical Formulation

The Taylor polynomial of degree $n$ centered at $a$ is:

$$
T_n(x)=
\sum_{k=0}^{n}
\frac{f^{(k)}(a)}{k!}(x-a)^k
$$

The corresponding Taylor series is:

$$
\sum_{k=0}^{\infty}
\frac{f^{(k)}(a)}{k!}(x-a)^k
$$

> [!important] Mathematical Distinction
> A Taylor polynomial is a finite approximation. A Taylor series is an infinite expansion.
>
> The existence of derivatives of all orders does not guarantee that the Taylor series converges to the original function.

## 9. Applications of Derivatives

> [!abstract] Definition
> Applications of Derivatives use differential calculus to analyze and solve mathematical problems involving rates of change, local behavior, and optimization.

### Function Analysis

- Increasing and Decreasing Functions
- Critical Points
- Local Maximum and Minimum
- Absolute Maximum and Minimum
- Concavity and Convexity
- Inflection Points
- Curve Sketching

### Optimization

- Optimization Problems
- Local Optimization
- Global Optimization
- First Derivative Test
- Second Derivative Test
- Constrained Optimization (introductory treatment)

### Approximation and Analysis

- Linear Approximation
- Differential Approximation
- Error Estimation
- Sensitivity Analysis
- Rate of Change Analysis

## 10. Knowledge Relationships

### Foundation Knowledge

- **Functions:** Provides the mathematical objects whose rates of change are studied.
- **Real Numbers:** Establishes the number system underlying classical differential calculus.
- **Limits:** Provides the mathematical foundation for defining derivatives.
- **Continuity:** Establishes an important property implied by differentiability.
- **Sequences and Series:** Provides the convergence theory needed to understand Taylor series.

### Downstream Knowledge

- **Integral Calculus:** Develops the complementary operation of integration, connected to differentiation through the Fundamental Theorem of Calculus.
- **Multivariable Calculus:** Generalizes differentiation to functions of multiple independent variables.
- **Ordinary Differential Equations:** Uses derivatives to formulate equations describing unknown functions and their rates of change.
- **Partial Differential Equations:** Extends differential equations to functions involving multiple independent variables.
- **Optimization Theory:** Develops derivative-based methods for finding extrema and optimal solutions.
- **Numerical Analysis:** Develops numerical techniques for approximating derivatives and solving derivative-based problems.

## 11. Fundamental Theorems

- Rolle's Theorem
- Mean Value Theorem
- Generalized Mean Value Theorem
- Taylor's Theorem
- Fermat's Theorem on Stationary Points

## 12. References

- Apostol, Tom M. (1967). *Calculus, Volume 1: One-Variable Calculus, with an Introduction to Linear Algebra*. Wiley.
- Spivak, Michael (2008). *Calculus*. 4th Edition. Publish or Perish.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition. Cengage Learning.