# Linear Algebra 

---

# T2. Matrix multiplication

When a matrix is multiplied by another matrix, the result is a third matrix. However, there is one simple rule: the number of columns in matrix *A* must match the number of rows in matrices *B*.

Lets view it in practice:

Matrix A has m rows and **n** columns. This means that the matrix B we are going to multiply A by must have **n** rows and k columns. 

Important here is **n**, **n** must tu be the same on both matrices.

As a result, the product of these matrices will be a new matrix with dimensions m × k.

Aₘₓₙ × Bₙₓₖ → Cₘₓₖ


### How to find C matrix elements

To compute the element Cᵢⱼ, you need to Take the i-th row of matrix A.Take the j-th column of matrix B. Multiply corresponding elements and sum them up.

**Example:**

$$
\begin{pmatrix}
  1 & 2  \\
  3 & 4   
\end{pmatrix}
\quad x \quad
\begin{pmatrix}
  1 & 0  \\
  2 & 3   
\end{pmatrix}
$$

First of all we need to know the size of each matrix. First is 2x2 and second one 2x2 

(A 2x`2` B `2`x2 rows and colums has the same value so we can multiply this matrices)

Size of each gonna be  A= `2`x2 B=2x`2` == C₂ₓ₂

Next step:

$$
A\begin{pmatrix}
  1 & 2  \\
  3 & 4   
\end{pmatrix}
\quad + \quad
B\begin{pmatrix}
  1 & 0  \\
  2 & 3   
\end{pmatrix}
\quad = \quad
C \begin{pmatrix}
  5 & X  \\
  X & X
\end{pmatrix}
$$


How to find all:
`Cᵢⱼ = multiply first matrix rowsᵢ by second matrix columsⱼ `

C₁₁ = A₁₁ x  B₁₁ + A₁₂ x B₂₁ = 1 x 1 + 2 x 2 = 5
С₁₂ = A₂₁ x  B₁₂ + A₂₂ x B₂₂ = 1 x 0 + 2 x 3 = 6

