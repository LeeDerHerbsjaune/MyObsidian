---
type: technical-term
title: "Sequences"
aliases:
  - Infinite Sequences
abbreviation: ""
field:
  - Mathematics
subfield:
  - Calculus
  - Mathematical Analysis
status: learning
confidence: 1
created: 2026-11-05
updated: 2026-11-05
tags:
  - technical-term
  - mathematics
  - sequences
sources: []
related: []
projects: []
---

> [!abstract] Definition
> A **sequence** is an ordered collection of elements arranged according to an index, typically the natural numbers.
>
> A real sequence is a function:
>
> $$a:\mathbb{N}\to\mathbb{R}$$
>
> Its terms are conventionally written as:
>
> $$a_1,a_2,a_3,\ldots$$
>
> The value $a_n$ is the $n$-th term.

## 1. Representation

> [!definition] Explicit Formula
> A sequence can be defined directly as a function of its index.
>
> $$a_n=\frac{1}{n}$$
>
> This produces:
>
> $$1,\frac12,\frac13,\frac14,\ldots$$

> [!definition] Recursive Formula
> A sequence can also be defined using one or more initial terms and a recurrence relation.
>
> For example:
>
> $$a_1=1,\qquad a_{n+1}=2a_n$$
>
> This produces:
>
> $$1,2,4,8,\ldots$$

## 2. Convergence

> [!important] Sequence Limit
> A sequence $(a_n)$ converges to $L$ if its terms approach $L$ as the index increases.
>
> $$\lim_{n\to\infty}a_n=L$$
>
> Formally, for every $\varepsilon>0$, there exists an integer $N$ such that:
>
> $$n\geq N\implies |a_n-L|<\varepsilon$$
>
> If no finite real limit exists, the sequence is divergent.

## 3. Important Properties

> [!note] Boundedness
> A sequence is bounded if there exists $M>0$ such that:
>
> $$|a_n|\leq M$$
>
> for every $n$.

> [!note] Monotonicity
> A sequence is:
> - Increasing if $a_{n+1}\geq a_n$.
> - Strictly increasing if $a_{n+1}>a_n$.
> - Decreasing if $a_{n+1}\leq a_n$.
> - Strictly decreasing if $a_{n+1}<a_n$.

> [!important] Monotone Convergence Theorem
> Every bounded monotone real sequence converges.
>
> This theorem is a consequence of the completeness of the real numbers.

> [!important] Subsequences
> A subsequence is formed by selecting terms with strictly increasing indices:
>
> $$a_{n_1},a_{n_2},a_{n_3},\ldots$$
>
> If a sequence converges to $L$, every subsequence also converges to $L$.

## 4. Important Concepts

> [!note] Cauchy Sequence
> A sequence is Cauchy if its terms become arbitrarily close to one another:
>
> $$\forall\varepsilon>0,\ \exists N:
> m,n\geq N\implies |a_m-a_n|<\varepsilon$$
>
> Every convergent real sequence is Cauchy, and every Cauchy real sequence converges.

> [!note] Limit Superior and Limit Inferior
> For bounded real sequences, the limit superior and limit inferior describe the largest and smallest subsequential limiting values, respectively.
>
> They are useful when a sequence does not converge.

## 5. Knowledge Relationships

### Foundation Knowledge
- **Functions:** A sequence is a function defined on an integer index set.
- **Limits:** Provide the formal definition of convergence.
- **Real Numbers:** Completeness guarantees convergence of Cauchy sequences.

### Downstream Knowledge
- **Series:** A series is constructed by summing sequence terms.
- **Convergence and Divergence:** Develops the limiting behavior of sequences.
- **Real Analysis:** Generalizes sequence theory to rigorous analysis.
- **Numerical Analysis:** Uses sequences to study iterative approximations and numerical algorithms.