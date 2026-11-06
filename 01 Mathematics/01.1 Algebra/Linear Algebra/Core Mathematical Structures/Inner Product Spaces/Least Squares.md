---
type: technical-term
title: "Least Squares"
aliases:
  - Least-Squares Method
  - Least-Squares Approximation
abbreviation: "LS"
field:
  - Mathematics
subfield:
  - Linear Algebra
  - Numerical Linear Algebra
status: learning
confidence: 1
created: 2026-11-04
updated: 2026-11-04
tags:
  - technical-term
  - linear-algebra
  - least-squares
sources:
  - "Strang, Gilbert. Introduction to Linear Algebra. 5th ed., 2016."
  - "Trefethen, Lloyd N., and David Bau III. Numerical Linear Algebra. 1997."
  - "Golub, Gene H., and Charles F. Van Loan. Matrix Computations. 4th ed., 2013."
related: []
projects: []
---

> [!abstract] Definition
> **Least Squares** is a mathematical method for finding an approximate solution to a system of linear equations by minimizing the squared norm of the residual.
>
> It is particularly useful when a system is overdetermined or when no exact solution exists.
>
> Geometrically, the least-squares solution corresponds to an orthogonal projection onto the column space of the coefficient matrix.

## 1. Mathematical Problem

> [!definition] Least-Squares Problem
> Consider a linear system:
>
> $$Ax=b$$
>
> where:
> - $A\in\mathbb{R}^{m\times n}$ is the coefficient matrix.
> - $x\in\mathbb{R}^{n}$ is the unknown vector.
> - $b\in\mathbb{R}^{m}$ is the observed or target vector.
>
> When an exact solution does not exist, seek an approximate solution $\hat{x}$ minimizing:
>
> $$\hat{x}=\underset{x\in\mathbb{R}^n}{\operatorname{argmin}}\|Ax-b\|_2^2$$
>
> The residual is:
>
> $$r=b-A\hat{x}$$

## 2. Geometric Interpretation

> [!important] Projection onto the Column Space
> Every vector $Ax$ belongs to the column space of $A$:
>
> $$Ax\in\operatorname{Col}(A)$$
>
> Therefore, solving the least-squares problem means finding the vector in $\operatorname{Col}(A)$ closest to $b$.
>
> The optimal approximation is:
>
> $$p=A\hat{x}=\operatorname{proj}_{\operatorname{Col}(A)}(b)$$
>
> The residual is orthogonal to the column space:
>
> $$r\perp\operatorname{Col}(A)$$
>
> Equivalently:
>
> $$A^T(b-A\hat{x})=0$$
>
> This is the geometric foundation of the normal equations.

## 3. Normal Equations

> [!definition] Normal Equations
> Starting from the orthogonality condition:
>
> $$A^T(b-A\hat{x})=0$$
>
> Rearranging gives:
>
> $$A^TA\hat{x}=A^Tb$$
>
> This system is called the **normal equations**.

> [!important] Full Column Rank Case
> If the columns of $A$ are linearly independent, then $A^TA$ is invertible.
>
> The unique least-squares solution is:
>
> $$\hat{x}=(A^TA)^{-1}A^Tb$$
>
> This formula is mathematically useful, but explicitly computing the inverse is generally not recommended in numerical implementations.

> [!warning] Rank-Deficient Case
> If the columns of $A$ are linearly dependent, $A^TA$ is singular.
>
> The least-squares problem still has at least one solution, but the minimizing vector $\hat{x}$ may not be unique.
>
> The Moore-Penrose pseudoinverse provides a systematic way to select the minimum-norm least-squares solution.

## 4. Projection Matrix Formulation

> [!definition] Projection onto the Column Space
> If $A$ has full column rank, the orthogonal projection matrix is:
>
> $$P=A(A^TA)^{-1}A^T$$
>
> The projected vector is:
>
> $$p=Pb$$
>
> The residual is:
>
> $$r=(I-P)b$$
>
> The matrix $P$ satisfies:
>
> $$P^T=P,\qquad P^2=P$$

## 5. QR-Based Least Squares

> [!important] QR Factorization
> Suppose $A$ has full column rank and its reduced QR factorization is:
>
> $$A=QR$$
>
> where:
> - $Q^TQ=I$.
> - $R$ is an invertible upper triangular matrix.
>
> The least-squares problem becomes:
>
> $$\min_x\|QRx-b\|_2$$
>
> Since $Q$ has orthonormal columns, the solution satisfies:
>
> $$R\hat{x}=Q^Tb$$
>
> Therefore:
>
> $$\hat{x}=R^{-1}Q^Tb$$
>
> In practice, solve the triangular system $R\hat{x}=Q^Tb$ rather than explicitly computing $R^{-1}$.

> [!note] Numerical Consideration
> QR-based methods are generally preferable to directly solving the normal equations in numerical computation.
>
> Forming $A^TA$ can square the condition number:
>
> $$\kappa_2(A^TA)=\kappa_2(A)^2$$
>
> for full-column-rank $A$.

## 6. Least Squares and the Pseudoinverse

> [!definition] Moore-Penrose Pseudoinverse
> The Moore-Penrose pseudoinverse of $A$ is denoted by $A^+$.
>
> The minimum-norm least-squares solution is:
>
> $$\hat{x}=A^+b$$
>
> This solution is defined even when $A$ is rectangular or rank-deficient.
>
> The pseudoinverse can be computed using the singular value decomposition.

## 7. Important Properties

> [!important] Existence
> Every finite-dimensional least-squares problem has at least one minimizing solution.

> [!important] Uniqueness
> The least-squares solution is unique if and only if $A$ has full column rank.
>
> Equivalently:
>
> $$\operatorname{rank}(A)=n$$

> [!important] Orthogonality of Residual
> For every least-squares solution:
>
> $$A^Tr=0$$
>
> Thus, the residual belongs to the orthogonal complement of the column space:
>
> $$r\in\operatorname{Col}(A)^\perp$$

> [!important] Minimum Residual
> The optimal solution satisfies:
>
> $$\|A\hat{x}-b\|_2
> \leq\|Ax-b\|_2$$
>
> for every $x\in\mathbb{R}^n$.

## 8. Typical Applications

> [!example] Overdetermined Systems
> When $m>n$, there are more equations than unknowns.
>
> The equations may be inconsistent, so an exact solution may not exist. Least Squares finds the vector that minimizes the total squared residual.

> [!example] Data Fitting
> Given observations, a model can be represented as a linear system:
>
> $$Ax\approx b$$
>
> Least Squares estimates the model parameters by minimizing the squared prediction error.
>
> Statistical assumptions and regression theory are separate subjects and are not developed in this note.

## 9. Knowledge Relationships

### Foundation Knowledge
- **Inner Products** — define the Euclidean norm and residual orthogonality.
- **Norms** — provide the objective function being minimized.
- **Orthogonality** — characterizes the optimal residual.
- **Orthogonal Projections** — provide the geometric interpretation of the solution.
- **Matrix Operations** — support the normal equations and matrix formulations.

### Downstream Knowledge
- **QR Factorization** — provides a numerically preferable method for solving full-column-rank least-squares problems.
- **Singular Value Decomposition** — provides a robust framework for rank-deficient and ill-conditioned least-squares problems.
- **Moore-Penrose Pseudoinverse** — gives the minimum-norm least-squares solution.
- **Linear Regression** — applies least-squares optimization to statistical model fitting.

## 10. References
1. Strang, Gilbert. *Introduction to Linear Algebra*. 5th ed., Wellesley-Cambridge Press, 2016.
2. Trefethen, Lloyd N., and David Bau III. *Numerical Linear Algebra*. SIAM, 1997.
3. Golub, Gene H., and Charles F. Van Loan. *Matrix Computations*. 4th ed., Johns Hopkins University Press, 2013.