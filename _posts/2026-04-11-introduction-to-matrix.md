---
layout: post
title: "2.4 Introduction to Matrices"
date: 2026-04-11 12:00:00 -0800
categories:
   - machinelearning
---
A matrix is a rectangular array consisting of rows and columns where data enters filled with observation data. It is a two-dimensional array of numbers depending on the number of rows and columns. Matrices are represented in uppercase, italic, and bold formatting. Each value inside of a matrix is called an element, similar to how they are called in a vector.

One can perform basic operations on matrices including addition, subtraction, multiplication, and division. Matrices can contain numbers, symbols, and expressions as well. A matrix can be any size, for example, a matrix of x by y has x rows and n columns (a 3 by 2 matrix has three rows and two columns. Transforming a particular matrix is often a desired end result for data processing and machine learning purposes. 

Each matrix element is identified with the position i and j, where i is the row and j is the column, as if the matrix were itself a coordinate plane. In Python, counting starts from 0, so the arrays will start with element a_00 and end with element a_(m-1n-1).

There are many types of matrices based on their common properties. There are seven different types that are helpful for data science and machine learning purposes.  
  1. Rectangular matrix is a matrix with a different number of rows and columns
  2. Square matrix is a subset of rectangular matrix with the same rows and columns
  3. Symmetric matrix is a subset of square matrix where the elements are mirrored diagonally
  4. Zero matrix is a matrix where all values in it are equal to zero such that any vector or matrix multiplied with it will become a zero matrix
  5. Identity matrix is a type of square matrix where only ones are in the diagonal and all off-diagonal values are zeros. It has a key role that when multiplying a vector or matrix with the identity matrix, the same vector or matrix emerges because the 1 in the diagonal selects the original diagonal components while the 0s in the off-diagonal eliminate those values
  6. A diagonal matrix is a type of matrix where all off-diagonal elements are equal to zero, but the diagonal elements are any number (including zero), not just one. When multiplying any scalar with an identity matrix, one gets a diagonal matrix
  7. Triangular matrix is a type of square matrix with elements on the upper right or lower left leaflet, while the opposing side of the diagonal is equal to zero


![Euler Matrix Diagram](/assets/machinelearning/EulerMatrixDiagram.png)
*Figure 1. Euler diagram depicting example matrix structures. All seven fall into the category of “rectangular matrix” (maroon). A zero matrix can have either a rectangular (red) or a square structure (purple). In the square matrix category (blue), there are three subtypes including the triangle matrix (green) where the upper or lower leaflet is occupied with numbers while the opposing side is filled with zeros, the diagonal matrix (yellow) where only the diagonals have numbers, and the identity matrix (orange), a diagonal subgroup where the diagonal is all 1.*

A linear transformation in a plane can be specified with vectors or matrices. In three-dimensional space, this is achieved using a matrix with nine elements. One can achieve scaling by a factor, reflection across the plane, rotation across any axis, or projection onto any plane. A linear transformation, like a linear equation, takes in a certain input and gives a corresponding output. If one multiplies an identity matrix by a vector [a,b], the result is the same vector [a,b]

Scaling is feasible by using a diagonal matrix, which can enable scaling the x-axis and y-axis by corresponding values. Inversion is also feasible with a diagonal matrix of elements [-1,0,0,-1], which will flip the x- and y-axis, such that points at (1,0) become (-1,0), or (0,1) becomes (0,-1). Rotation is feasible using trigonometric functions of elements [cos(x), -sin(x), sin(x), cos(x)] in a rotation matrix, which will rotate vectors by 90 degrees. Transformations can also combine two or more transformations, such as scaling and rotation or scaling and inversion. Challenge: show how to calculate the following matrix and vector multiplication equation, and create a new equation for visualization.

![Matrix Transformation](/assets/machinelearning/MatrixTransformation.png)
*Figure 2. Example of matrix transformation by taking a transformation matrix and multiplying it by a vector [1, 2] to receive an output vector [6,5].*

In linear algebra, one may combine any number of linear transformations to obtain a new linear transformation through a process known as composition of linear transformations. Any linear representation is represented with a matrix, so any composed linear transformation can be represented as matrices, which is useful for scaling many for machine learning.

One calculates a composition from left to right, calculating a product matrix to obtain a new matrix, which is the composition of linear transformations for matrix A and matrix B. These columns are the result of applying the transformation to each basis vector set.  One performs matrix multiplication by doing the dot product of rows and columns. Each corresponding element from the first row of A is multiplied by the corresponding element of the first column of B, and the values are added to get the first element of the combined matrix, A⋅B. At the end, one may multiply this new matrix by a vector to obtain the final linear combination.

