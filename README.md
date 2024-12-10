# Linear Algebra

## Introduction

I am a self-taught individual, which means I have learned linear algebra independently.

---

# T1. Base

In linear algebra, a matrix is defined by a letter, and the dimensions of the matrix are indicated below the letter. For example, *A*₃ₓ₂ means the matrix has 3 rows and 2 columns. Each position in the matrix is defined by its row and column.
And the elemetns of the matrix repsents by aᵢⱼ where ᵢⱼ define position.

**Example**

*Aₘₓₙ* =

$$
\begin{pmatrix}
  a₁₁ & a₁₂ & \dots & a₁ₙ  \\
  a₂₁ & a₂₂ & \dots & a₂ₙ  \\
  aₙ₁ & aₙ₂ & \dots & aₙₙ 
\end{pmatrix}
$$

We have the first position, which is **a₁₁**. This means **a₁₁** is in the **first row and first column**.

More practice example:

*B₃ₓ₂* =

$$
\begin{pmatrix}
  1 & 2  \\
  3 & 4  \\
  5 & 6 
\end{pmatrix}
$$

The position of 5 is in the 3rd row, 1st column.  
The position of 2 is in the 1st row, 2nd column.

When a matrix has only 1 row, it is called a **Column Vector**.

*C* =

$$
\begin{pmatrix}
  a₁ \\
  a₂ \\
  aₙ
\end{pmatrix}
$$



> [!NOTE]  
> If matrix hase same numbre of column and rows,then that matrix is called square matrix
>
>**Example**
>
>*B₂ₓ₂* =
>
>$$
>\begin{pmatrix}
>  1 & 2  \\
>  3 & 4   
>\end{pmatrix}
>$$



---
There is such this that is called **main diagonal** which is defined by diagonal elements, their also have the same numbre of position, which is defined by aᵢⱼ , ᵢ = ⱼ. 
Also there is a side diagonal, that is vice versa. 
<p align="center">
   <img src="https://github.com/user-attachments/assets/fa011eb9-92aa-46f3-9918-ec3e09d4bbee" alt="Calculator screenshot" />
</p>


The **side diagonal** is from top-right to bottom-left:

<p align="center">
   <img src="https://github.com/user-attachments/assets/c50a5ba9-135f-4bab-91e7-a3290871f201" alt="Calculator screenshot" />
</p>

---

# T1.2. Base: Sum&Subtraction + multiplication


When we want to sum matrices, we need to know that after adding two matrices, *A+B*, the result will be one matrix. Also, we must know that we cannot sum matrices if their sizes are not the same.

If Aₘₓₙ B also has to be ₘₓₙ

Aₘₓₙ+Bₘₓₙ = Cₘₓₙ 

> [!IMPORTANT]  
> if they don't, arithmetic operations like addition are not possible..

**Example**

$$
A = \begin{pmatrix}
  1 & 2  \\
  3 & 4   
\end{pmatrix}
\quad + \quad
B = \begin{pmatrix}
  -2 & 0  \\
  1 & 2   
\end{pmatrix}
\quad = \quad
C = \begin{pmatrix}
  -1 & 2  \\
  4 & 6
\end{pmatrix}
$$

We doing this the next way:


A 1 + B -2 = C -1

A 2 + B 0 = C 2 

A 3 + B 1 = C 4

A 4 + B 2 = C 6


**Another example**


$$
A = \begin{pmatrix}
  1 & 2  \\
  3 & 4   
\end{pmatrix}
\quad - \quad
B = \begin{pmatrix}
  -2 & 0  \\
  1 & 2   
\end{pmatrix}
\quad = \quad
C = \begin{pmatrix}
  -3 & 2  \\
  2 & 2
\end{pmatrix}
$$

This is:

A 1 - B -2 = C 3

A 2 - B 0 = C 2

A 3 - B 1 = C 2

A 4 - B 2 = C 2 

--- 

Another very important step you need to have knowladge to is to doing multipy matrix by a single numbre.

> [!TIP]
> Lambda (λ): When lambda (λ) is defined, it means that the operation is applied to each element of the matrix.

**Example**

*λ*A

-2 А

$$
λ \times \begin{pmatrix}
    1 & 0 \\
    -3 & 5 \\
    0 & 1
\end{pmatrix}
= \begin{pmatrix}
    -2 & 0 \\
    6 & -10 \\
    0 & -2
\end{pmatrix}
$$

---

**Last example**

*A₃ₓ₂* =

$$
\begin{pmatrix}
  2 & -1  \\
  0 & 3  \\
  5 & 1 
\end{pmatrix}
$$

*B₃ₓ₂* =

$$
\begin{pmatrix}
  0 & 5  \\
  -1 & 2  \\
  3 & 4 
\end{pmatrix}
$$

λ = 2

A - λB ?



λB = 


$$
λ \times B\begin{pmatrix}
    0 & 5 \\
    -1 & 2 \\
    3 & 4
\end{pmatrix}
= \begin{pmatrix}
    0 & 10 \\
    -2 & 4 \\
    6 & 8
\end{pmatrix}
$$

jus multiply each element of the B matrix by λ(2).



$$
A \begin{pmatrix}
  2 & -1  \\
  0 & 3  \\
  5 & 1 
\end{pmatrix}
\quad - \quad
λB \begin{pmatrix}
    0 & 10 \\
    -2 & 4 \\
    6 & 8
\end{pmatrix}
\quad = \quad
 = \begin{pmatrix}
    2 & 11 \\
    2 & -1 \\
    -1 & -7
\end{pmatrix}
$$

same but now substract A matrix - λB.

<p align="right">
  <a href="https://github.com/21Sec0nds/LinearAlgebra/tree/T2">Next page</a>
</p>
