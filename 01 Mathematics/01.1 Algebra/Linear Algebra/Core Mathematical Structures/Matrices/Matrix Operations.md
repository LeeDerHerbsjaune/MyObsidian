---
type: technical-term
title: "Matrix Operations"
aliases:
  - Matrix Arithmetic
field:
  - Mathematics
subfield:
  - Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - mathematics
  - linear-algebra
  - matrix-operations
sources:
  - "Strang, Introduction to Linear Algebra, 5th Edition, 2016"
related: []
projects: []
---
> [!abstract] Definition
> Matrix operations are algebraic operations performed on matrices, including addition, subtraction, scalar multiplication, and matrix multiplication.

## 1. Matrix Addition

> [!definition] Addition
> Two matrices can be added only when they have identical dimensions.
>
> For $A,B\in\mathbb{F}^{m\times n}$:
>
> $$
> (A+B)_{ij}=a_{ij}+b_{ij}
> $$

## 2. Matrix Subtraction

> [!definition] Subtraction
> $$
> (A-B)_{ij}=a_{ij}-b_{ij}
> $$
>
> Matrix subtraction is defined only for matrices with identical dimensions.

## 3. Scalar Multiplication

> [!definition] Scalar Multiplication
> For $\alpha\in\mathbb{F}$:
>
> $$
> (\alpha A)_{ij}=\alpha a_{ij}
> $$
>
> Every entry of the matrix is multiplied by the same scalar.

## 4. Algebraic Properties

> [!important] Addition Properties
> For compatible matrices $A,B,C$:
>
> **Commutativity**
> $$
> A+B=B+A
> $$
>
> **Associativity**
> $$
> (A+B)+C=A+(B+C)
> $$
>
> **Additive Identity**
> $$
> A+0=A
> $$
>
> **Additive Inverse**
> $$
> A+(-A)=0
> $$

> [!important] Scalar Multiplication Properties
> $$
> \alpha(A+B)=\alpha A+\alpha B
> $$
>
> $$
> (\alpha+\beta)A=\alpha A+\beta A
> $$
>
> $$
> \alpha(\beta A)=(\alpha\beta)A
> $$

## 5. Noncommutativity of Matrix Multiplication

> [!warning] Important Distinction
> Matrix multiplication is generally not commutative:
>
> $$
> AB\neq BA
> $$
>
> Even when both products exist, their values may differ.

## 6. Knowledge Relationships

### Foundation Knowledge
- **Matrices** — defines matrix structure and dimensions.
- **Fields and Number Systems** — defines scalar arithmetic.

### Downstream Knowledge
- **Matrix Multiplication** — develops the matrix product.
- **Matrix Transpose** — develops transpose identities.
- **Matrix Inverse** — develops multiplicative inverses.
- **Matrix Algebra** — studies the broader algebraic structure of matrices.

## 7. References

- Strang, Gilbert. *Introduction to Linear Algebra*, 5th Edition, 2016.
- Meyer, Carl D. *Matrix Analysis and Applied Linear Algebra*, 2000.