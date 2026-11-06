---
type: technical-term
title: "Antiderivatives"
aliases:
  - Primitive Functions
  - Nguyên hàm
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

# Antiderivatives

> [!abstract] Definition
> An antiderivative of a function is a function whose derivative equals the original function.
>
> Antiderivatives reverse the differentiation process and form the mathematical foundation of indefinite integration.

## 1. Definition

> [!definition] Antiderivative
> A function $F(x)$ is an antiderivative of $f(x)$ on an interval $I$ if:

$$
F'(x)=f(x)
$$

## 2. Family of Antiderivatives

> [!important] Constant of Integration
> If $F(x)$ is an antiderivative of $f(x)$, then every function of the form $F(x)+C$ is also an antiderivative.

$$
F(x)+C
$$

where $C$ is an arbitrary constant.

> [!note] Uniqueness
> Any two antiderivatives of the same function on an interval differ by a constant.

## 3. Basic Antiderivative Formulas

> [!info] Power Rule

$$
\int x^n\,dx
=
\frac{x^{n+1}}{n+1}+C
$$

for $n\neq -1$.

> [!info] Exponential Functions

$$
\int e^x\,dx=e^x+C
$$

$$
\int a^x\,dx=
\frac{a^x}{\ln a}+C
$$

> [!info] Trigonometric Functions

$$
\int \cos x\,dx=\sin x+C
$$

$$
\int \sin x\,dx=-\cos x+C
$$

$$
\int \sec^2x\,dx=\tan x+C
$$

## 4. Properties

> [!important] Linearity
> Antiderivatives preserve linear combinations.

$$
\int [af(x)+bg(x)]\,dx
=
a\int f(x)\,dx+b\int g(x)\,dx
$$

## 5. Existence of Antiderivatives

> [!info] Continuity
> Every continuous function on an interval has an antiderivative on that interval.
>
> However, not every function has an antiderivative everywhere on its domain.

## 6. Applications

- Reconstructing functions from their derivatives.
- Solving elementary differential equations.
- Constructing indefinite integrals.
- Recovering position from velocity and velocity from acceleration.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Antiderivatives reverse differentiation.
- **Differentiation Rules:** Provides the rules used to verify antiderivatives.
- **Functions:** Provides the mathematical objects being integrated.

### Downstream Knowledge
- **Indefinite Integrals:** Expresses families of antiderivatives using integral notation.
- **Definite Integrals:** Connects antiderivatives with accumulated quantities through the Fundamental Theorem of Calculus.
- **Ordinary Differential Equations:** Uses antiderivatives to solve certain differential equations.

## 8. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.