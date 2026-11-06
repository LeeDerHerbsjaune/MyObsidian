---
type: technical-term
title: "Jordan Canonical Form"
aliases:
  - Jordan Normal Form
  - Jordan Form
abbreviation: "JCF"
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Matrix Theory
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - matrix-decompositions
sources:
  - "Axler, Sheldon. Linear Algebra Done Right. 3rd ed., 2015."
  - "Horn, Roger A., and Charles R. Johnson. Matrix Analysis. 2nd ed., 2012."
  - "Meyer, Carl D. Matrix Analysis and Applied Linear Algebra. 2000."
related: []
projects: []
---

> [!abstract] Definition
> **Jordan Canonical Form** is a canonical block-diagonal representation of a square matrix under similarity transformations.
>
> It extends diagonalization to matrices that may not possess a complete basis of eigenvectors.
>
> The representation reveals eigenvalues, algebraic multiplicities, eigenspace dimensions, and generalized eigenvector structure.

## 1. Mathematical Definition

> [!definition] Similarity Transformation
> Two square matrices $A,B\in\mathbb{F}^{n\times n}$ are similar if there exists an invertible matrix $P$ such that:
>
> $$B=P^{-1}AP$$
>
> Similar matrices represent the same linear operator in different bases.
>
> The Jordan Canonical Form is a special representative of a similarity class.

> [!definition] Jordan Canonical Form
> Over an algebraically closed field, such as $\mathbb{C}$, every square matrix $A$ is similar to a block-diagonal matrix $J$:
>
> $$A=PJP^{-1}$$
>
> where $P$ is invertible and $J$ consists of Jordan blocks.

## 2. Jordan Blocks

> [!definition] Jordan Block
> A Jordan block associated with eigenvalue $\lambda$ and size $k$ is:
>
> $$J_k(\lambda)=
> \begin{bmatrix}
> \lambda & 1 & 0 & \cdots & 0\\
> 0 & \lambda & 1 & \cdots & 0\\
> 0 & 0 & \lambda & \ddots & \vdots\\
> \vdots & \vdots & \ddots & \ddots & 1\\
> 0 & 0 & \cdots & 0 & \lambda
> \end{bmatrix}$$
>
> The eigenvalue appears on the diagonal, and ones appear immediately above the diagonal.

> [!important] Block-Diagonal Structure
> The Jordan matrix has the form:
>
> $$J=
> \operatorname{diag}
> \left(
> J_{k_1}(\lambda_1),
> J_{k_2}(\lambda_2),
> \ldots,
> J_{k_s}(\lambda_s)
> \right)$$
>
> The eigenvalues and block sizes determine the Jordan structure.

## 3. Generalized Eigenvectors

> [!definition] Generalized Eigenvector
> A nonzero vector $v$ is a generalized eigenvector associated with eigenvalue $\lambda$ if:
>
> $$ (A-\lambda I)^k v=0$$
>
> for some positive integer $k$.
>
> Ordinary eigenvectors are the special case:
>
> $$(A-\lambda I)v=0$$

> [!important] Jordan Chain
> A Jordan chain of length $k$ consists of vectors $v_1,\ldots,v_k$ satisfying:
>
> $$(A-\lambda I)v_1=0$$
>
> $$(A-\lambda I)v_2=v_1$$
>
> $$\vdots$$
>
> $$(A-\lambda I)v_k=v_{k-1}$$
>
> The first vector is an eigenvector, while the remaining vectors are generalized eigenvectors.
>
> The vectors in the chains form a basis in which the matrix has Jordan block structure, under the stated convention.

## 4. Relationship to Diagonalization

> [!important] Diagonalizable Matrices
> A matrix is diagonalizable if it is similar to a diagonal matrix:
>
> $$A=PDP^{-1}$$
>
> This occurs exactly when all Jordan blocks have size one.
>
> Therefore:
>
> - Diagonalizable matrices have a basis of ordinary eigenvectors.
> - Nondiagonalizable matrices require generalized eigenvectors to construct a Jordan basis.

> [!note] Algebraic and Geometric Multiplicity
> For an eigenvalue $\lambda$:
>
> - Its algebraic multiplicity equals the sum of the sizes of its Jordan blocks.
> - Its geometric multiplicity equals the number of Jordan blocks associated with it.
>
> The geometric multiplicity cannot exceed the algebraic multiplicity.

## 5. Important Properties

> [!important] Uniqueness
> Over an algebraically closed field, the Jordan canonical form is unique up to the ordering of its Jordan blocks.
>
> The matrix $P$ that transforms $A$ into Jordan form is generally not unique.

> [!important] Characteristic Polynomial
> The characteristic polynomial is determined by the diagonal entries:
>
> $$p_A(t)=\prod_{\lambda}(t-\lambda)^{a_\lambda}$$
>
> where $a_\lambda$ is the algebraic multiplicity of $\lambda$.

> [!important] Minimal Polynomial
> The exponent of $(t-\lambda)$ in the minimal polynomial equals the size of the largest Jordan block associated with $\lambda$.
>
> Thus, the minimal polynomial reveals the maximum Jordan block size for each eigenvalue.

> [!important] Matrix Powers
> A Jordan block can be written:
>
> $$J_k(\lambda)=\lambda I+N$$
>
> where $N$ is nilpotent:
>
> $$N^k=0$$
>
> For nonnegative integer $m$:
>
> $$J_k(\lambda)^m=
> \sum_{j=0}^{k-1}
> \binom{m}{j}\lambda^{m-j}N^j$$
>
> with the expression interpreted through the binomial expansion. This form is useful for understanding powers of matrices and their long-term behavior.

## 6. Field Dependence and Limitations

> [!warning] Field Dependence
> Jordan canonical form in the usual complex-eigenvalue block representation is guaranteed over an algebraically closed field such as $\mathbb{C}$.
>
> A real matrix may have complex eigenvalues, so its Jordan form may require complex entries.
>
> Over $\mathbb{R}$, a corresponding real canonical representation can use real blocks for complex-conjugate eigenvalue pairs.

> [!warning] Numerical Limitations
> Jordan form is highly sensitive to small perturbations.
>
> A matrix that is theoretically defective can become diagonalizable after an arbitrarily small perturbation.
>
> Therefore, Jordan canonical form is primarily a theoretical tool rather than a preferred numerical decomposition.

## 7. Knowledge Relationships

### Foundation Knowledge
- **Eigenvalues and Eigenvectors** — provide the eigenvalues and ordinary eigenvectors underlying Jordan structure.
- **Characteristic Polynomial** — determines eigenvalues and algebraic multiplicities.
- **Eigenspaces** — determine geometric multiplicities.
- **Linear Independence and Basis** — provide the framework for constructing generalized eigenvector bases.
- **Similarity Transformations** — define the equivalence relation under which Jordan form is obtained.

### Downstream Knowledge
- **Minimal Polynomial** — encodes the maximum Jordan block size for each eigenvalue.
- **Matrix Functions** — Jordan form can be used to derive functions of matrices.
- **Differential Equations** — Jordan structure helps analyze linear systems of differential equations.
- **Spectral Theory** — studies eigenvalue and operator structure beyond diagonalization.

## 8. References
1. Axler, Sheldon. *Linear Algebra Done Right*. 3rd ed., Springer, 2015.
2. Horn, Roger A., and Charles R. Johnson. *Matrix Analysis*. 2nd ed., Cambridge University Press, 2012.
3. Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*. SIAM, 2000.