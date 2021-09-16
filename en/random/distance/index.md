# Distance

Write a program that contains a function that calculates the average distance
between two random points that fall (uniformly) somewhere in a square with a dimension of $$1\times 1$$.


## Background

This is a classic example of a clear and apparently simple problem, which is difficult to analytically solve. Give it a try, then you'll soon find yourself quite stuck. Do at least try to make an estimation, so you can assess whether the answer of your program is somewhat realistic, before handing in your assignment.

![](../../../assets/vierkant.png)


## Specification

* The name of the program should be `distance.py`.

* Declare a function `square(n)` that takes a number `n`, the number of iterations, as a parameter, and returns the average distance between two random points in a $1 \times 1$ square.


## Problem analysis

* Generate two random points (so, two random $$x$$-values and two random $$y$$-values) and calculate the distance between these two points.

* Repeat this many times and keep track of the total distance in a separate variable.

* Calculate the average distance by dividing the total distance by $$N$$.


## Testing

	checkpy distance.py
