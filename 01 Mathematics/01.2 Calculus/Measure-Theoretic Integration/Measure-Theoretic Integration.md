---
type: technical-term
title: Measure-Theoretic Integration
aliases:
  - Lebesgue Integration
  - Integration Theory
field:
  - Mathematics
subfield:
  - Real Analysis
  - Measure Theory
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - real-analysis
  - measure-theory
  - integration
sources:
  - Royden & Fitzpatrick (2010), Real Analysis
  - "Folland (1999), Real Analysis: Modern Techniques and Their Applications"
  - "Stein & Shakarchi (2005), Real Analysis: Measure Theory, Integration, and Hilbert Spaces"
related:
  - "[[Measurable Sets]]"
  - "[[Simple Functions]]"
  - "[[Measure Spaces]]"
  - "[[Measurable Functions]]"
  - "[[Lebesgue Integral]]"
  - "[[Lebesgue–Stieltjes Integral]]"
  - "[[Almost-Everywhere Convergence]]"
  - "[[Monotone Convergence Theorem]]"
  - "[[Fatou's Lemma]]"
  - "[[Dominated Convergence Theorem]]"
  - "[[Product Measures]]"
  - "[[Tonelli's Theorem]]"
  - "[[Fubini's Theorem]]"
  - "[[Radon–Nikodym Theorem]]"
  - "[[Signed Measures]]"
  - "[[Complex Measures]]"
  - "[[Vector-Valued Integration]]"
projects: []
---
> [!abstract] Definition
> **Measure-Theoretic Integration** is the mathematical theory of integration constructed using measures and measurable functions. It generalizes classical Riemann integration by defining integrals over measurable spaces and allowing integration with respect to measures other than ordinary length, area, or volume.
>
> Its central construction is the **Lebesgue integral**, which approximates measurable functions using simple functions and extends integration to a much broader class of functions.

## 1. Mathematical Framework

> [!info] Measure Space
> A measure space is a triple:
>
> $$ (X,\mathcal{F},\mu) $$
>
> where:
> - $X$ is a set.
> - $\mathcal{F}$ is a $\sigma$-algebra of subsets of $X$.
> - $\mu:\mathcal{F}\rightarrow[0,\infty]$ is a measure.
>
> The measure assigns a nonnegative size to measurable sets and satisfies:
>
> 1. $\mu(\varnothing)=0$.
> 2. Nonnegativity.
> 3. Countable additivity for pairwise disjoint measurable sets.

> [!info] Measurable Functions
> A function $f:X\rightarrow\mathbb{R}$ is measurable if the preimage of every Borel set is measurable.
>
> Equivalently, for real-valued functions, it is sufficient that:
>
> $$\{x\in X:f(x)>a\}\in\mathcal{F}$$
>
> for every $a\in\mathbb{R}$.
>
> Measurability is the fundamental condition that makes the Lebesgue integral well-defined.

## 2. Simple Functions

> [!definition] Simple Function
> A measurable simple function takes only finitely many values:
>
> $$\phi(x)=\sum_{i=1}^{n}a_i\mathbf{1}_{A_i}(x)$$
>
> where:
> - $a_i$ are nonnegative real numbers.
> - $A_i$ are measurable sets.
> - $\mathbf{1}_{A_i}$ is the indicator function of $A_i$.
>
> Its integral is defined by:
>
> $$\int_X\phi\,d\mu
> =\sum_{i=1}^{n}a_i\mu(A_i)$$
>
> Simple functions provide the foundation for constructing the Lebesgue integral.

## 3. Lebesgue Integral

> [!definition] Nonnegative Measurable Functions
> For a nonnegative measurable function $f:X\rightarrow[0,\infty]$, define:
>
> $$\int_X f\,d\mu
> =
> \sup\left\{
> \int_X\phi\,d\mu:
> 0\leq\phi\leq f,\;
> \phi\text{ is simple}
> \right\}$$
>
> The integral is the supremum of the integrals of all nonnegative simple functions bounded above by $f$.

> [!definition] General Measurable Functions
> For a measurable function $f$, define its positive and negative parts:
>
> $$f^+=\max(f,0)$$
>
> $$f^-=\max(-f,0)$$
>
> Then:
>
> $$f=f^+-f^-$$
>
> If both integrals are finite, $f$ is integrable and:
>
> $$\int_X f\,d\mu
> =
> \int_X f^+\,d\mu
> -
> \int_X f^-\,d\mu$$
>
> Equivalently, $f$ is integrable when:
>
> $$\int_X |f|\,d\mu<\infty$$

## 4. Fundamental Properties

> [!important] Linearity
> For integrable functions $f,g$ and scalars $a,b$:
>
> $$\int_X(af+bg)\,d\mu
> =
> a\int_Xf\,d\mu+b\int_Xg\,d\mu$$

> [!important] Monotonicity
> If $f\leq g$ almost everywhere, then:
>
> $$\int_Xf\,d\mu\leq\int_Xg\,d\mu$$
>
> whenever the integrals are defined.

> [!important] Almost-Everywhere Equality
> If $f=g$ almost everywhere, then:
>
> $$\int_Xf\,d\mu=\int_Xg\,d\mu$$
>
> Thus, changing a function on a measure-zero set does not change its integral.

> [!important] Absolute Integrability
> If:
>
> $$\int_X|f|\,d\mu<\infty$$
>
> then $f$ is integrable and:
>
> $$\left|\int_Xf\,d\mu\right|
> \leq\int_X|f|\,d\mu$$

## 5. Convergence Theorems

> [!theorem] Monotone Convergence Theorem
> If $(f_n)$ is a sequence of nonnegative measurable functions satisfying:
>
> $$0\leq f_1\leq f_2\leq\cdots$$
>
> and $f_n(x)\rightarrow f(x)$ pointwise, then:
>
> $$\int_Xf\,d\mu
> =
> \lim_{n\rightarrow\infty}\int_Xf_n\,d\mu$$
>
> This theorem allows integration and increasing limits to be interchanged.

> [!theorem] Fatou's Lemma
> For a sequence of nonnegative measurable functions:
>
> $$\int_X\liminf_{n\rightarrow\infty}f_n\,d\mu
> \leq
> \liminf_{n\rightarrow\infty}
> \int_Xf_n\,d\mu$$
>
> Fatou's lemma provides a fundamental inequality for limits of integrals.

> [!theorem] Dominated Convergence Theorem
> Suppose:
> - $f_n\rightarrow f$ almost everywhere.
> - There exists an integrable function $g$ such that $|f_n|\leq g$ almost everywhere for every $n$.
>
> Then:
>
> $$\lim_{n\rightarrow\infty}\int_Xf_n\,d\mu
> =
> \int_Xf\,d\mu$$
>
> This is one of the most important tools for exchanging limits and integrals.

## 6. Important Integration Results

> [!theorem] Tonelli's Theorem
> For a nonnegative measurable function on a product measure space:
>
> $$\int_{X\times Y}f\,d(\mu\times\nu)
> =
> \int_X\left(\int_Yf(x,y)\,d\nu(y)\right)d\mu(x)$$
>
> The iterated integrals may be interchanged, including when their value is infinite.

> [!theorem] Fubini's Theorem
> If $f$ is integrable on a product measure space, then its iterated integrals exist almost everywhere and:
>
> $$\int_{X\times Y}f\,d(\mu\times\nu)
> =
> \int_X\left(\int_Yf(x,y)\,d\nu(y)\right)d\mu(x)$$
>
> Unlike Tonelli's theorem, Fubini's theorem requires integrability.

> [!theorem] Radon–Nikodym Theorem
> If $\nu$ is a $\sigma$-finite measure absolutely continuous with respect to a $\sigma$-finite measure $\mu$, then there exists a nonnegative measurable function $f$ such that:
>
> $$\nu(A)=\int_Af\,d\mu$$
>
> for every measurable set $A$.
>
> The function $f$ is the Radon–Nikodym derivative:
>
> $$f=\frac{d\nu}{d\mu}$$

## 7. Relationship to Riemann Integration

> [!important] Riemann and Lebesgue Integration
> Riemann integration partitions the domain into intervals and approximates function values over those intervals.
>
> Lebesgue integration instead measures the sizes of sets on which a function takes particular ranges of values.
>
> For a bounded function on a compact interval, Riemann integrability is equivalent to the set of discontinuities having Lebesgue measure zero.
>
> Every bounded Riemann-integrable function on a compact interval is Lebesgue integrable, and the two integrals agree.
>
> Lebesgue integration also handles many unbounded functions and functions with highly irregular discontinuities that are not Riemann integrable.

## 8. Limitations and Scope

> [!warning] Mathematical Conditions
> - Measurability is required for the standard Lebesgue integral.
> - Integrability requires finite absolute integral for a real-valued function.
> - Convergence theorems have distinct hypotheses and cannot be interchanged arbitrarily.
> - Product integration requires the appropriate product measure and measurability assumptions.
> - Some integration problems require extensions or alternatives, such as the Lebesgue–Stieltjes integral or more general integration theories.

## 9. Knowledge Relationships

### Foundation Knowledge

> [!note] Essential
> - **Measure Theory** — provides measurable spaces, measures, and measurable functions.
> - **Real Analysis** — provides limits, sequences, continuity, and convergence.
> - **Integral Calculus** — provides the classical integration framework that measure-theoretic integration generalizes.

> [!note] Relevant
> - **Set Theory** — supports the construction of measurable spaces and set operations.
> - **Topology** — contributes to Borel sets and the structure of measurable spaces.
> - **Infinite Sequences and Series** — supports the study of function sequences and convergence.

### Downstream Knowledge

> [!note] Relevant
> - **$L^p$ Spaces** — uses Lebesgue integration to define norms and function spaces.
> - **Probability Theory** — formulates expectations and probability distributions through measure-theoretic integration.
> - **Product Measures** — extends integration to product spaces.

> [!note] Advanced
> - **Functional Analysis** — develops integration within normed and Banach spaces.
> - **Fourier Analysis** — uses Lebesgue integration to define and analyze transforms.
> - **Harmonic Analysis** — studies operators and function spaces built on measure-theoretic foundations.
> - **Ergodic Theory** — uses measure-preserving transformations and integration.
> - **Stochastic Processes** — builds advanced probabilistic models using measure theory and integration.

## 10. References

> [!bibliography] Foundational References
> - Royden, H. L., & Fitzpatrick, P. M. (2010). *Real Analysis* (4th ed.).
> - Folland, G. B. (1999). *Real Analysis: Modern Techniques and Their Applications* (2nd ed.).
> - Stein, E. M., & Shakarchi, R. (2005). *Real Analysis: Measure Theory, Integration, and Hilbert Spaces*.
> - Rudin, W. (1987). *Real and Complex Analysis* (3rd ed.).