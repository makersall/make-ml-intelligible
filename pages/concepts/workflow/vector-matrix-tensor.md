---
layout: content
title: Vectors, Matrices, and Tensors
image: 'colorful-art-supplies-1445895-pxh.jpg'
---

Just like our noses can't smell as much as a dog's nose can,
and our eyes can't see parts of the light spectrum that other creatures can
we can't see space in more than three dimensions.

But the basic idea of a vector is the same whether you are talking about
a line in 2 dimensions
a line in three dimensions
a list of values -- e.g., the length, width, height, weight, color, price, manufacturer, make, model, average rating, etc. of an item in an online store

If you think of a vector visually:
2 values gives you a line in two-dimensional space: [X, Y]
3 values gives you one in three dimensional space: [X, Y, Z]
Just like our noses are much more limited in what they can smell then a dog's nose,

tensor: instead of having the words array (one dimension), matrix, etc., just have one word that covers all of it {need to check, get a slightly better definition}. Basically, when you see tensor, it's a list or table of numbers

 > when we see a picture like this number eight.  It's actually just a bunch of numbers. For this grayscale one, it's a matrix of numbers. If it was a color image, it would have a third dimension. So when you add an extra dimension, we call it a tensor rather than a matrix. It would be a 3D tensor of numbers ﹣ red, green, and blue
 > Like legos?  Like bathroom tiles?  Like bricks on a wall?  Like beads?  Knitting? Like spelling out at a football game?
Why?  Because computers don’t have eyeballs— and they’re super good with numbers 


scalar: a number/magnitude/size


scalar vector multiplication sounds scary,
but basically it's what you do if you increase/decrease the size of something

A vector can be a row vector or a column vector

dot product
it's one of the core building blocks of computer graphics
It allows you, for example, to do things like have a bunch of objects that you display where there are lights and reflections, called ray tracing

A matrix of 3 columns can represent 3 lines/vectors in 3D

Rules when you multiply matrixes:
let's say we have 2 matrixes: 3 x 2 and 2 x 4
The number of columns in the first matrix (2) has to be the same as the number of rows in the second matrix (2)

The new matrix will be the number of rows in the first matrix by the number of columns in the second (3 x 4)

How you do the multiple in:
a x b = c
c11 = a11*b11 + a12*b21

OR:
row 1, column 1 = 
for each number in A's row 1 and B's column 1:
	pair them up, multiply the pairs, then add all of the pairs together

I get _how_ you do matrix multiplication,
I'm still having trouble understanding _why_


## Matrix Vector Multiplication

Matrix Vector Multiplication Works by the Same Rules.

Suppose you have a matrix M with 4 rows and 3 columns.
To multiply it with a vector V, the vector needs to be three rows -- i.e., 4 x 3 * 3 x 1

In the final vector:
The first item, V[1] will be:
Pair up the items in matrix row 1 with the items in the vector,
multiply each of the pairs, then add them up

Why does it work this way?
I guess the answer is, because that's the way the math works out

for example, immersivemath.com has an example of a 2000-year-old Chinese word problem:
if 5 sheep, 4 dogs, 3 chickens and 2 rabbits cost 1496 coins,
4 sheep, 2 dogs, 6 chickens, and 5 rabbits cost 958 coins,
3 sheep, 1 dog, 7 chickens, and 5 rabbits cost 958 points
2 sheep, 3 dogs, 5 chickens, and 1 rabbit cost 861 coins
How much does a sheep, dog, chicken, and rabbit each cost?

The way you solve it is by "gaussian elimination"

But if you knew the cost of a sheep, dog, chicken, and rabbit,
and you had 3 orders,
you could use matrix Vector multiplication to figure out the total for each order

Because it would be represented as:
s d c r
5 4 3 2   s
4 2 6 5   d
3 1 7 5   c
2 3 5 1   r
[





## Practical Examples of Using 2D and 3D Matrixes

Rotating a 2D Object:
You can figure out the math for doing this quickly by "applying" (multiplying?) a 2 dimensional (2 x 2) rotation matrix of:

cos o	- sin o
sin o	  cos o

where o is the number of degrees you are rotating the object

If you are rotating in 3D, you need a 3 x 3 matrix for x, y, and z.


2D Scaling matrix:
fx	0
0	fy

Where fx is how much you are scaling X and fy is how much you are scaling y

To do it for three dimensions, you use:

fx	0	0
0	fy	0
0	0	fz

