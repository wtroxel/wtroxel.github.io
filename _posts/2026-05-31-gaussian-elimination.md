---
layout: post
title: "2.5 Gaussian Elimination"
date: 2026-05-31 12:00:00 -0800
categories:
   - machinelearning
---
Karl Gauss invented a method to solve linear equation systems, known as Gaussian Elimination. The method involves taking a matrix, A, and combining it with a constant vector, b into an augmented matrix combining the coefficients and constants into one grid. A series of elementary row operations on that augmented or partitioned matrix are short-hand summaries used to prove that the system of linear equations either has a solution, no solutions, or an infinite number of solutions. These "elementary row operations" may entail interchanging two equations (row interchange), multiplying the equation by a non-zero constant (row scaling), or adding a multiple of one matrix row to another matrix row for a certain number of times.

![Gaussian Elimination](/assets/machinelearning/GaussianElimination.png)  
Figure 1. Example workflow for solving set of linear equations with Gaussian Elimination  

The method entails setting up a "counting board" for the coefficients and to use one linear system as the reference. In the example provided, the x-coefficient is organized from smallest to largest, and the middle column is multiplied by four such that subtracting the right-most column twice will give a 0-value for the x-coefficient. The same thing is done for the left-most column to render a 0-value for the x-coefficient. The next step is to eliminate another coefficient (in this case, the z-coefficient) in the left and middle columns to isolate one variable, the y-coefficient. Re-inserting the y-, z-, and x-coefficients in that order yields the one solution for the set of linear equations.

Linear equations can be solved in several ways. Another technique to solve linear equations is matrix inversion. Inversion means that if there is some number, A, there is a corresponding number, B, that will give a product of one when A and B are multiplied. A general idea also applies to matrices where given some matrix A, it is possible to find a matrix A^-1 that gives an identity matrix where every value along the diagonal is one.
![Inverse Matrix](/assets/machinelearning/MatrixInversion.png)
Figure 2. The method by which to calculate the inverse matrix  

The "determinant" of a matrix is used to determine if a matrix is invertible. The determinant for some matrix A is denoted as "det(A)." When det(A) = 0, it means that the inverse matrix is not computable, since the inverse of matrix A is 1/det(A), or 1/0, which is undefined. In this situation, matrix A is "singular" and has only linearly-dependent columns.

The determinant for a 2x2 matrix is given by det(A) = a*d - b*c. See the below example for a visual example of solving the matrix determinant.

![Matrix Determinant](/assets/machinelearning/DeterminantParallelogram.png)
Figure 3. A visualization to solve the area of a parallelogram using the matrix determinant
