---
layout: post
title: "2.2 Vector Basics"
date: 2026-03-31 12:00:00 -0800
categories:
   - machinelearning
---
In linear algebra, a scalar is a number describing only the magnitude of some aspect of a system. An example of a scalar is the mass of a rocket ship. In contrast, a vector is a number describing both the magnitude and direction of some system. An example is a rocket’s velocity of a planet, such as seven kilometers per second (km/s). 

A vector is an ordered list of numbers. The order matters. An example is a rocket has two elements in a vector set for mass and velocity. A rocket in low Earth orbit may have a mass of 150 metric tons and an orbital velocity of seven km/s, but not a mass of seven metric tons and an orbital velocity of 150 km/s (half the speed of light!)

Vectors have two key characteristics. The first is dimensionality, how many elements in this vector set. The second is orientation, which is how the vector is aligned. The orientation also matters. One may have a vector with four elements vertically in a column vector and horizontally in a row vector; they are different from the computer’s perspective.

By default, Python defines vectors as column-oriented unless specified with a superscript “t”, which indicates transposition where the column vector is changed into a row vector. The vector starts at the tail and ends at the head, and the angle relative to the positive x-axis defines the length and direction. Vectors are easily represented with a list or NumPy arrays.

VectorList = [1,2,3,4,5]   #Python list  
VectorArray = np.array([1,2,3,4,5])   #Orient-less array in NumPy  
rowVector = np.array([[1,2,3,4,5] ])   #Row Vector in NumPy  
columnVector = np.array([[1],[2],[3],[4],[5]])   #Column Vector in NumPy  

Vector addition, subtraction, multiplication, and division is a matter of adding and subtracting each corresponding element. The dimensionality, or size, must be the same. It is not possible to do these operations to one with four since they do not exist in the same vector space.  
	a = [6 5 1 8 10] and b = [4 3 1 9 -15]  
	a + b = [10 8 2 17 -5]  
	a - b = [2 2 0 -1 5]  
	a * b = [24 15 1 72 -150]  
	a / b = [1.5 1.667 1 0.889 -0.667]  

Another key operation is vector scalar multiplication. One may take the vector and multiply each corresponding vector element by a common scalar, like the number four.  
	4 * a = [24 20 4 32 40]  

Note that there is a difference between a Python list and an NumPy array. Multiplying a scalar by a Python list will just repeat the list twice. Multiplying a scalar by a vector made in a NumPy array will give the element-wise multiplication results. In general, there are four scalar multiplication cases, either the vector gets larger in the same direction when multiplying by values greater than 1, shrinks when multiplied by a value between 0 to 1, becomes 0 when multiplied by 0, and reverses direction when multiplied by values less than 0.

A cartesian coordinate system identifies the position of objects in n-dimensional space. For a 2D coordinate system, an xy-plane is used, while a 3D system uses an xyz-plane. For a coordinate plane, 2D is more typical. The x-axis is specified along left-and-right while the y-axis is specified along up-and-down. A point describes a pair of x and y coordinates to specify its position in space. The order matters, as (2,3) and (3,2) have the same numbers, but in a different order giving a completely different position in space.

Building on this, vectors are represented with the tail and head of an arrow in space. Vector addition is done by connecting the tail of one vector with the head of another for however many vectors are in the system. By drawing a line from the tail of the first vector to the head of the last vector, one obtains the final net vector for vector addition.
