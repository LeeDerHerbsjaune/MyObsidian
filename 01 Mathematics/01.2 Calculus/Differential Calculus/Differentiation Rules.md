---
type: technical-term
title: "Differentiation Rules"
aliases:
  - Derivative Rules
  - Quy tắc đạo hàm
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Differential Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - differentiation
sources: []
related: []
projects: []
---

# Differentiation Rules

> [!abstract] Definition
> Differentiation Rules are mathematical rules used to calculate derivatives of functions systematically.
>
> They establish how differentiation interacts with algebraic operations, function composition, and elementary mathematical functions.

## 1. Basic Differentiation Rules

> [!definition] Constant Rule

$$
\frac{d}{dx}(c)=0
$$

> [!definition] Power Rule

$$
\frac{d}{dx}(x^n)=nx^{n-1}
$$

> [!definition] Constant Multiple Rule

$$
\frac{d}{dx}[cf(x)]=cf'(x)
$$

> [!definition] Sum Rule

$$
\frac{d}{dx}[f(x)+g(x)]
=f'(x)+g'(x)
$$

> [!definition] Difference Rule

$$
\frac{d}{dx}[f(x)-g(x)]
=f'(x)-g'(x)
$$

## 2. Product Rule

> [!definition] Definition
> The Product Rule determines the derivative of a product of two differentiable functions.

$$
\frac{d}{dx}[f(x)g(x)]
=
f'(x)g(x)+f(x)g'(x)
$$

## 3. Quotient Rule

> [!definition] Definition
> The Quotient Rule determines the derivative of the ratio of two differentiable functions, where the denominator is nonzero.

$$
\frac{d}{dx}
\left[\frac{f(x)}{g(x)}\right]
=
\frac{f'(x)g(x)-f(x)g'(x)}
{[g(x)]^2}
$$

## 4. Chain Rule

> [!definition] Definition
> The Chain Rule determines the derivative of a composite function.

$$
\frac{d}{dx}f(g(x))
=
f'(g(x))g'(x)
$$

> [!important] Key Principle
> Differentiate the outer function while keeping the inner function unchanged, then multiply by the derivative of the inner function.

## 5. Elementary Function Derivatives

> [!info] Exponential Functions

$$
\frac{d}{dx}e^x=e^x
$$

$$
\frac{d}{dx}a^x=a^x\ln a
$$

> [!info] Logarithmic Functions

$$
\frac{d}{dx}\ln x=\frac{1}{x}
$$

$$
\frac{d}{dx}\log_a x
=
\frac{1}{x\ln a}
$$

> [!info] Trigonometric Functions

$$
\frac{d}{dx}\sin x=\cos x
$$

$$
\frac{d}{dx}\cos x=-\sin x
$$

$$
\frac{d}{dx}\tan x=\sec^2 x
$$

> [!info] Inverse Trigonometric Functions

$$
\frac{d}{dx}\arcsin x
=
\frac{1}{\sqrt{1-x^2}}
$$

$$
\frac{d}{dx}\arctan x
=
\frac{1}{1+x^2}
$$

## 6. Hyperbolic Function Derivatives

> [!info] Common Formulas

$$
\frac{d}{dx}\sinh x=\cosh x
$$

$$
\frac{d}{dx}\cosh x=\sinh x
$$

$$
\frac{d}{dx}\tanh x=\operatorname{sech}^2x
$$

## 7. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Establishes the mathematical operation being calculated.
- **Functions:** Provides the objects to which differentiation rules apply.
- **Limits:** Provides the theoretical foundation for differentiation.

### Downstream Knowledge
- **Higher-Order Derivatives:** Applies differentiation rules repeatedly.
- **Implicit Differentiation:** Uses the chain rule to differentiate implicit relationships.
- **Related Rates:** Uses differentiation rules with time-dependent variables.
- **Taylor Approximation:** Uses derivatives to construct polynomial approximations.

## 8. References

- Stewart, James (2015). *Calculus: Early Transcendentals*. 8th Edition.
- Apostol, Tom M. (1967). *Calculus, Volume 1*. Wiley.