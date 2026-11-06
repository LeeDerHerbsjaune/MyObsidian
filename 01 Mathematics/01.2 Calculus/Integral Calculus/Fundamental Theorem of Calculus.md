---
type: technical-term
title: "Fundamental Theorem of Calculus"
aliases:
  - FTC
  - Định lý cơ bản của giải tích
abbreviation: "FTC"
field:
  - Mathematics
subfield:
  - Calculus
  - Integral Calculus
  - Differential Calculus
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - mathematics
  - calculus
  - integral-calculus
  - differential-calculus
sources: []
related: []
projects: []
---

# Fundamental Theorem of Calculus

> [!abstract] Definition
> The Fundamental Theorem of Calculus establishes the fundamental relationship between differentiation and integration.
>
> It demonstrates that differentiation and definite integration are inverse operations under appropriate mathematical conditions.
>
> The theorem consists of two closely related parts that connect continuous accumulation with antiderivatives.

## 1. First Part of the Fundamental Theorem

> [!definition] FTC Part I
> If $f$ is continuous on $[a,b]$ and:

$$
F(x)=\int_a^x f(t)\,dt
$$

then $F$ is differentiable on $(a,b)$ and:

$$
F'(x)=f(x)
$$

> [!important] Interpretation
> The derivative of an accumulation function equals its original integrand.
>
> This establishes a direct connection between accumulated quantities and instantaneous rates of change.

## 2. Second Part of the Fundamental Theorem

> [!definition] FTC Part II
> If $f$ is continuous on $[a,b]$ and $F$ is an antiderivative of $f$, then:

$$
\int_a^b f(x)\,dx
=
F(b)-F(a)
$$

> [!important] Interpretation
> A definite integral can be evaluated by finding an antiderivative and calculating its difference at the integration limits.

## 3. Relationship Between Differentiation and Integration

> [!important] Inverse Operations
> The Fundamental Theorem establishes two complementary relationships:

Differentiation after accumulation:

$$
\frac{d}{dx}
\left[
\int_a^x f(t)\,dt
\right]
=f(x)
$$

Integration after differentiation:

$$
\int_a^b F'(x)\,dx
=
F(b)-F(a)
$$

## 4. Accumulation Functions

> [!definition] Definition
> An accumulation function represents the total signed contribution of an integrand from a fixed starting point to a variable endpoint.

$$
A(x)=\int_a^x f(t)\,dt
$$

Its instantaneous rate of change is:

$$
A'(x)=f(x)
$$

## 5. Variable Integration Limits

> [!info] Differentiation with Variable Bounds
> If $f$ is continuous and $u(x)$ and $v(x)$ are differentiable:

$$
\frac{d}{dx}
\int_{u(x)}^{v(x)}f(t)\,dt
=
f(v(x))v'(x)
-
f(u(x))u'(x)
$$

This is the Leibniz rule for differentiation of an integral with variable limits and a fixed integrand.

## 6. Mathematical Significance

> [!important] Fundamental Consequences
> - Connects differential and integral calculus.
> - Provides an efficient method for evaluating definite integrals.
> - Establishes the derivative of accumulation functions.
> - Explains why antiderivatives can evaluate definite integrals.
> - Forms a foundation for advanced integration theory.

## 7. Conditions and Limitations

> [!warning] Mathematical Conditions
> The standard formulations use continuity of the integrand on a closed and bounded interval.
>
> More general versions can be established under weaker assumptions using appropriate integration and regularity frameworks.
>
> The theorem should not be applied indiscriminately to divergent improper integrals.

## 8. Knowledge Relationships

### Foundation Knowledge
- **Derivatives:** Provides the differentiation operation connected to integration.
- **Antiderivatives:** Supplies the functions used to evaluate definite integrals.
- **Indefinite Integrals:** Represents families of antiderivatives.
- **Definite Integrals:** Provides the accumulated quantity connected to antiderivatives.
- **Continuity:** Provides the standard regularity condition in the classical theorem.

### Downstream Knowledge
- **Real Analysis:** Generalizes and rigorously develops the relationship between differentiation and integration.
- **Lebesgue Integration:** Establishes broader versions of fundamental integration theorems.
- **Multivariable Calculus:** Extends the relationship between differentiation and integration to higher dimensions.
- **Vector Calculus:** Develops multidimensional integral theorems, including Green's, Stokes', and the Divergence Theorem.

## 9. References

- Apostol, Tom M. (1969). *Calculus, Volume 2*. Wiley.
- Spivak, Michael (2008). *Calculus*. 4th Edition.
- Rudin, Walter (1976). *Principles of Mathematical Analysis*. 3rd Edition.