---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 7

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: UML
        url: '../uml-lm'
    next:
        content: Design Patterns
        url: '../design-patterns-lm'
---

# Data Structures

![Hero Banner Image](images/data-hero-banner.png)

-   In programming we have the concept of reusable data structures which can be used to build applications
-   These can be used in order to build larger systems (e.g. Inventory Systems, AI Navigation etc)
-   Most programming languages have these built in
-   Before writing any system you should always examine these data structures and pick the appropriate one for your Use Case

## Big 'O' Notation

*“Measuring programming progress by lines of code is like measuring aircraft building progress by weight.”*
Bill Gates

How we want to define our code is based on two simple premises: **Simplicity** and **Purpose**.

### What is Big 'O'?

-   The efficiency of an algorithm can be gauged by how long it takes
-   This is known as *Time Complexity*
-   Big O Notation is used to describe this

One of the ways to make our code efficient is by optimising the search for data within a data set.
Let's consider how we search a data set of 100 items for a single data point. For example in a data set of 100 items, you are searching for an ‘0’ amongst ‘X’s.

![100 data points](images/100-data-points.png)
*Fig. 1 - 100 data points in a data set*

 - The **best case** for finding the data is **1 iteration**
 - The **worst case** is a **100 iterations**

Big ‘O’ is always based on worse case scenario. 
- So **100 records** would take **100 iterations**
- Therefore **N records** would take **N iterations**.
- This can be written like this:

$$0(N)$$

**Performance** is represented by the **O** and the **N** represents **execution time or space used** - Hence the term Big ‘O’.

## Different Notation in Big 'O'

The previous example is known as:

### Linear Notation - $$0(N)$$

**Pseudo Code**
```c#
FUNCTION  linearSearch(list, value)
	FOR EACH element IN list
		IF (element == value)
			RETURN true
		END IF
	NEXT
		RETURN false
END FUNCTION
```
**Graph**
![Linear Notation Graph](images/linear.png)
*Fig. 2 - Linear Notation Graph*

### Constant Notation - $$0(1)$$
**Pseudo Code**
```c#
FUNCTION getFirstElement(list)
	RETURN list[0]
END FUNCTION
```
**Graph**
![Constant Notation Graph](images/constant.png)
*Fig. 3 - Constant Notation Graph*

The constant notation describes an algorithm that will always execute in the same execution time regardless of the size of the data set. For instance, an algorithm to retrieve the first value of a data set, will always be completed in one step, regardless of the number of values in the data set.

#### Hashing Tables

A hashing algorithm is an $$0(1)$$ algorithm that can be used to very effectively locate/search a value/key when the data is stored using a hash table.

![Hashing Tables](images/hashing.png)
*Fig. 4 - Hashing Tables*

A hash table locates the actual data at an address called an index that is always a whole number and therefore is always associated with that record.

A bit like a book in a library its location is always known because of it’s numbering system. It resides at a fixed location no matter if the book is replaced with a newer copy. No sorting is required.

### Polynomial 	Notation - $$0(N^2)$$
**Pseudo Code**
```c#
PROCEDURE emptyChessboardGrid()
	FOR row FROM 0 to 7
		FOR col FROM 0 to 7
			grid[row][col] = 0
		NEXT col
	NEXT row
END PROCEDURE
```
**Graph**
![Polynomial Notation Graph](images/polynomial.png)
*Fig. 5 - Polynomial Notation Graph*

$$O(N2)$$ represents an algorithm whose performance is directly proportional to the square of the size of the data set. Algorithms which are based on nested loops are more likely to have a quadratic $$O(N2)$$ and so are 2 dimensional arrays like the one above. Where we are plotting the grid of a chessboard.

### Exponential Notation - $$0(2^N)$$
**Pseudo Code**
```c#
FUNCTION  fibonacci(number)
	IF  (number <= 1)
		RETURN  number
	END  IF
	RETURN fibonacci(number - 2) + fibonacci(number -  1)
END FUNCTION
```
**Graph**
![Exponential Notation Graph](images/exponential.png)
*Fig. 5 - Exponential Notation Graph*

The exponential notation O(2N) describes an algorithm whose growth doubles with each addition to the data set.
An example of an $$0(2^N)$$ function is the recursive calculation of Fibonacci numbers:

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjE0NDI3NDgyMywtMzA5MjEwNzI2LC0xND
U2MjE4MTI4LC0xMTQyMTAzNjc0LDE2MDY0MTQ0MTAsLTY4MTA0
NTMwMSwtNDM1MTE3MTQ2LC0xNDY2MDM0NjQ2LDQ0ODU5MzEzOC
wxNTYxMzA5MDYwLC0xMjU0NzcxMTgsLTczNDc1ODYyOSwtMzE1
NzcwMzAwLDE3NDcxNTIxMzQsNTg5MDM3Mjk4XX0=
-->