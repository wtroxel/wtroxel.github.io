---
layout: post
title: "2.1 Introduction to Linear Algebra"
date: 2026-03-28 12:00:00 -0800
categories:
   - networkengineer
---

Linear algebra is a branch of mathematics focusing on linear equations, vectors, matrices, and linear transformations. It provides a mechanism by which to describe and perform operations on coordinates and planes in higher dimensions. These are the building blocks for machine learning (ML), as it relies on vectors, matrices, linear transformations, determinants, and vector spaces. Large data sets are essentially matrices and performing operations like splitting the data into training and testing data requires linear algebra.

Linear algebra is necessary to understand and modify machine learning algorithms. The most important elements of linear algebra for ML include:

1. Data set and data files - The model is fit to a data set, either a matrix or a vector
2. Images and photographs - All images are stored as a matrix, and manipulating the image such as rotation, scaling, or contorting rely on linear algebra
3. Data preparation - Dimensionality reduction and one hot encoding require linear algebra to reduce complexity in the model. Data sets are matrices, and matrix factorization reduces it to key components. One-hot encoding classifies categorical variables, like if a compound has dermal toxicity, genotoxicity or carcinogenicity, with ones and zeros.
4. Linear regression - Predicts numeric values in simple regression problems, a supervised ML algorithm and statistical approach to find relations between independent (x) and dependent (y) variables with a straight line from a linear equation, like y = mx + b. A common approach to solve linear regression is least squares optimization by minimizing the differences between the observed and predicted values with matrix factorization
5. Regularization - Used to mitigate the effects of overfitting, where models fit too close for available data and cannot perform well with new data. Encourages a model to reduce the size of coefficients while fitting on the data. An analogy is the use of the taylor expansion to approximate sin(x), where using more terms increasing the precision at values close a desired point, but it gets more divergent further from that point (Figure 1)

![Sin(x) Taylor Expansion](/assets/machinelearning/SinxTaylorExpansion.png)
*Figure 1. y = sin(x) shown in red. Taylor expansions with increasing terms shown in blue, green, purple, and black. As the number of terms increases, the precision close to x = 0 is better. As x increases or decreases, the divergence gets increasingly fast.*


6. Principal Component Analysis (PCA) - Matrix factorization method to create lower-dimensional projections of high-dimensional data for visualization and training. 
7. Latent Semantic Analysis (LSA) - Data preparation method used for natural language processing, where documents are represented as word occurrence matrices. Matrix factorization is used to compare, query, and use them in ML models.
8. Recommender systems - Predictive modeling system to recommend products or services. An example is the YouTube algorithm, which gives recommendations for new videos based on previous viewing history and the viewing trends of similar users 
9. Deep learning - Subset of machine learning using higher dimensions involving vectors, matrices, and tensors of inputs and coefficients

