---
type: technical-term
title: "Indefinite Integrals"
aliases:
  - Indefinite Integration
  - Tích phân bất định
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Integral Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - integral-calculus
sources: []
related: []
projects: []
---

# Indefinite Integrals

> [!abstract] Definition
> An indefinite integral represents the family of all antiderivatives of a function on a specified interval.
>
> It is the inverse operation of differentiation, up to an arbitrary constant of integration.

## 1. Mathematical Definition

> [!definition] Indefinite Integral

$$
\int f(x)\,dx=F(x)+C
$$

where:

- $f(x)$: Integrand.
- $dx$: Differential notation identifying the integration variable.
- $F(x)$: An antiderivative of $f(x)$.
- $C$: Constant of integration.

## 2. Relationship with Differentiation

> [!important] Inverse Relationship

$$
\frac{d}{dx}
\left[\int f(x)\,dx\right]=f(x)
$$

The integration operation recovers an antiderivative, while differentiation recovers the original integrand.

## 3. Properties

> [!info] Linearity

$$
\int [af(x)+bg(x)]\,dx
=
a\int f(x)\,dx+b\int g(x)\,dx
$$

> [!info] Constant of Integration
> The arbitrary constant must be included because differentiation eliminates constants.

## 4. Basic Integration Formulas

> [!info] Power Rule

$$
\int x^n\,dx=
\frac{x^{n+1}}{n+1}+C
$$

for $n\neq -1$.

> [!info] Logarithmic Integral

$$
\int\frac{1}{x}\,dx
=
\ln|x|+C
$$

> [!info] Exponential Integral

$$
\int e^x\,dx=e^x+C
$$

> [!info] Trigonometric Integrals

$$
\int\sin x\,dx=-\cos x+C
$$

$$
\int\cos x\,dx=\sin x+C
$$

## 5. Integration as an Operation

> [!note] Integrand and Integration Variable
> An indefinite integral operates on an integrand with respect to a specified variable.
>
> The result is a family of functions rather than a single numerical value.

## 6. Applications

- Finding antiderivatives.
- Solving elementary differential equations.
- Recovering functions from known derivatives.
- Establishing expressions for later definite integration.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Antiderivatives:** Provides the mathematical concept represented by indefinite integrals.
- **Derivatives:** Establishes the inverse relationship underlying integration.
- **Differentiation Rules:** Supports verification of integration results.

### Downstream Knowledge
- **Integration Techniques:** Develops systematic methods for evaluating indefinite integrals.
- **Definite Integrals:** Introduces integration over bounded intervals.
- **Fundamental Theorem of Calculus:** Establishes the connection between indefinite and definite integration.

## 8. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.