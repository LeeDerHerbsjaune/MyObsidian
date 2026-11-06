---
type: technical-term
title: "Integration Techniques"
aliases:
  - Methods of Integration
  - Techniques of Integration
  - Phương pháp tính tích phân
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
  - integration
sources: []
related: []
projects: []
---

# Integration Techniques

> [!abstract] Definition
> Integration Techniques are systematic mathematical methods used to evaluate integrals that cannot be directly computed using elementary integration formulas.
>
> They transform integrands into forms that are easier to integrate while preserving mathematical equivalence.

## 1. Substitution Method

> [!definition] Definition
> Substitution simplifies an integral by introducing a new variable to replace a suitable inner expression.

Let:

$$
u=g(x)
$$

Then:

$$
du=g'(x)\,dx
$$

Therefore:

$$
\int f(g(x))g'(x)\,dx
=
\int f(u)\,du
$$

## 2. Integration by Parts

> [!definition] Definition
> Integration by Parts is derived from the product rule of differentiation.

$$
\int u\,dv=uv-\int v\,du
$$

It is particularly useful for products of functions.

## 3. Trigonometric Integrals

> [!definition] Definition
> Trigonometric integration uses trigonometric identities and algebraic transformations to evaluate integrals involving trigonometric functions.

Common identities:

$$
\sin^2x+\cos^2x=1
$$

$$
1+\tan^2x=\sec^2x
$$

$$
1+\cot^2x=\csc^2x
$$

Typical cases:
- Powers of sine and cosine.
- Powers of tangent and secant.
- Powers of cotangent and cosecant.
- Products of trigonometric functions.

## 4. Trigonometric Substitution

> [!definition] Definition
> Trigonometric substitution replaces algebraic expressions involving square roots with trigonometric expressions.

Common substitutions:

$$
\sqrt{a^2-x^2}:
\quad x=a\sin\theta
$$

$$
\sqrt{a^2+x^2}:
\quad x=a\tan\theta
$$

$$
\sqrt{x^2-a^2}:
\quad x=a\sec\theta
$$

## 5. Partial Fraction Decomposition

> [!definition] Definition
> Partial Fraction Decomposition expresses a rational function as a sum of simpler rational functions whose integrals are easier to evaluate.

For example:

$$
\frac{1}{(x-a)(x-b)}
=
\frac{A}{x-a}
+
\frac{B}{x-b}
$$

The coefficients are determined by algebraic identities.

## 6. Algebraic Manipulation

> [!info] Additional Methods
> Some integrals become easier after algebraic transformations.

Common approaches:
- Polynomial expansion.
- Completing the square.
- Polynomial division.
- Rationalization.
- Trigonometric identities.
- Symmetry transformations.

## 7. Reduction Formulas

> [!definition] Definition
> Reduction formulas express an integral involving a parameter or exponent in terms of integrals of lower complexity.

A common example is:

$$
I_n=\int\sin^n x\,dx
$$

which can be transformed into a recurrence involving $I_{n-2}$.

## 8. Choosing an Integration Technique

> [!important] Method Selection
> - Composite functions: Consider substitution.
> - Products of different function types: Consider integration by parts.
> - Trigonometric powers: Consider trigonometric identities.
> - Algebraic square roots: Consider trigonometric substitution.
> - Rational functions: Consider partial fractions.
> - Repeated powers or parameterized integrals: Consider reduction formulas.

## 9. Knowledge Relationships

### Foundation Knowledge
- **Indefinite Integrals:** Defines the integration problems being evaluated.
- **Differentiation Rules:** Provides the theoretical basis for integration by parts and substitution.
- **Algebra:** Supports algebraic transformations and partial fractions.
- **Trigonometric Functions:** Supports trigonometric integration techniques.

### Downstream Knowledge
- **Definite Integrals:** Applies integration techniques to bounded integration problems.
- **Improper Integrals:** Uses integration techniques to evaluate certain limiting integrals.
- **Multiple Integrals:** Generalizes integration methods to multidimensional settings.
- **Differential Equations:** Uses integration techniques to solve differential equations.

## 10. References

- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.
- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.