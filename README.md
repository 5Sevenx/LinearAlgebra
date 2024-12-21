# Linear Algebra

---

# T2. Matrix Multiplication

When a matrix is multiplied by another matrix, the result is a third matrix. However, there is one simple rule: the number of columns in matrix *A* must match the number of rows in matrix *B*.

Let’s view it in practice:

Matrix *A* has *m* rows and *n* columns. This means that the matrix *B* we are going to multiply *A* by must have *n* rows and *k* columns.

Important here is *n*. *n* must be the same in both matrices.

As a result, the product of these matrices will be a new matrix with dimensions *m* × *k*.

Aₘₓₙ × Bₙₓₖ → Cₘₓₖ

### How to find C matrix elements

To compute the element Cᵢⱼ, take the *i*-th row of matrix *A* and the *j*-th column of matrix *B*. Multiply corresponding elements and sum them up.

---

**Example:**

$$
\begin{pmatrix}
  1 & 2  \\
  3 & 4   
\end{pmatrix}
\quad \times \quad
\begin{pmatrix}
  1 & 0  \\
  2 & 3   
\end{pmatrix}
$$

First of all, we need to know the size of each matrix. The first matrix is 2×2, and the second one is also 2×2. 

(A 2×2 × B 2×2, where the number of columns in A equals the number of rows in B, so we can multiply these matrices.)

The resulting matrix will be C₂×₂.

**Next step:**

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
  5 & 6  \\
  11 & 12
\end{pmatrix}
$$

To find all elements of matrix *C*:

C₁₁ = A₁₁ × B₁₁ + A₁₂ × B₂₁ = 1 × 1 + 2 × 2 = 5

C₁₂ = A₁₁ × B₁₂ + A₁₂ × B₂₂ = 1 × 0 + 2 × 3 = 6

C₂₁ = A₂₁ × B₁₁ + A₂₂ × B₂₁ = 3 × 1 + 4 × 2 = 11

C₂₂ = A₂₁ × B₁₂ + A₂₂ × B₂₂ = 3 × 0 + 4 × 3 = 12

$$
C \begin{pmatrix}
  5 & 6  \\
  11 & 12
\end{pmatrix}
$$

> [!TIP]  
> To find Cᵢⱼ, multiply the *i*-th row of matrix *A* by the *j*-th column of matrix *B* and sum the results.
> 
> To get C₁₁, multiply the first row of *A* by the first column of *B*.
> 
> To get C₁₂, multiply the first row of *A* by the second column of *B*, and so on.

---

**Another example:**

$$
A \begin{pmatrix}
  5 & -1 & 0  \\
  2 & 1 & 1  \\
\end{pmatrix} 
\quad \times \quad
B \begin{pmatrix}
  0 & 2  \\
  3 & 1 \\
 -1 & -2 
\end{pmatrix}
$$

Here, A is 2×3, B is 3×2, so the result will be C₂×₂.

Now let’s compute the elements of *C*:

C₁₁ = 5 × 0 + (-1) × 3 + 0 × (-1) = -3

C₁₂ = 5 × 2 + (-1) × 1 + 0 × (-1) = 9

C₂₁ = 2 × 0 + 1 × 3 + 1 × (-1) = 2

C₂₂ = 2 × 2 + 1 × 1 + 1 × (-2) = 3

$$
C \begin{pmatrix}
  -3 & 9  \\
  2 & 3
\end{pmatrix}
$$

But what if we want to multiply matrix *B* by matrix *A*?

B₃×₂ × A₂×3 results in a 3×3 matrix.

For the first element of *C*, we multiply the first row of matrix *B* by the columns of matrix *A*:

C₁₁ = 0 × 5 + 2 × 2 = 4

C₁₂ = 3 × 5 + 1 × 2 = 17

C₁₃ = 3 × (-1) + 1 × 1 = -2

And so on for other elements of *C*.

$$
C \begin{pmatrix}
  4 & 17 & -2  \\
  2 & -2 & 1 \\
  -9 & -1 & -2 
\end{pmatrix}
$$

> [!IMPORTANT]  
> AB ≠ BA 
>
>$$
>A \begin{pmatrix}
>  5 & -1 & 0  \\
>  2 & 1 & 1  \\
>\end{pmatrix} 
>\quad \times \quad
>B \begin{pmatrix}
>  0 & 2  \\
>  3 & 1 \\
> -1 & -2 
>\end{pmatrix}
>\quad = \quad
>C \begin{pmatrix}
>  -3 & 9  \\
>  2 & 3
>\end{pmatrix}
>$$
>
>
>$$
>B \begin{pmatrix}
>  0 & 2  \\
>  3 & 1 \\
> -1 & -2 
>\end{pmatrix}
>\quad \times \quad
>A \begin{pmatrix}
>  5 & -1 & 0  \\
>  2 & 1 & 1  \\
>\end{pmatrix} 
>\quad = \quad
>C \begin{pmatrix}
>  4 & 17 & -2  \\
>  2 & -2 & 1 \\
>  -9 & -1 & -2 
>\end{pmatrix}
>$$

---

**Last thing:**

$$
A \begin{pmatrix}
  1 & 2   \\
  3 & 4  \\
  5 & 6  
\end{pmatrix}
\quad \times \quad
B \begin{pmatrix}
  1 \\
  2  
\end{pmatrix}
$$

> [!TIP]  
> This matrix is called a Column Vector.
> 
> $$
>B \begin{pmatrix}
>  1 \\
>  2  
>\end{pmatrix}
>$$
>
> This matrix has one column and multiple rows.

Let’s check the multiplication:

Matrix *A* is 3×2 and matrix *B* is 2×1, so the result matrix will be C₃×1.

Now we multiply the columns of *A* by the column vector *B*:

C₁ = 1 × 1 + 2 × 2 = 4

C₂ = 3 × 1 + 4 × 2 = 10

C₃ = 5 × 1 + 6 × 2 = 16

$$
C \begin{pmatrix}
  4 \\
  10  \\
  16
\end{pmatrix}
$$




If we try to multiply B₂×1 and A₃×2, we would not be able to do it, because the number of columns in matrix *A* does not match the number of rows in matrix *B*.
