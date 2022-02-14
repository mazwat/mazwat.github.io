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
    <!---next:
        content: Design Patterns
        url: '../design-patterns-lm'-->
---

# Data Structures

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

| | | | | | | | | | |
|---|:-:|---|---|---|---|---|---|---|---|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|**0**|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|
|X|X|X|X|X|X|X|X|X|X|

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
----ADD GRAPH IMAGE----

### Constant Notation - $$0(1)$$
**Pseudo Code**
```c#
FUNCTION getFirstElement(list)
	RETURN list[0]
END FUNCTION
```
**Graph**
----ADD GRAPH IMAGE----

The constant notation describes an algorithm that will always execute in the same execution time regardless of the size of the data set.

For instance, an algorithm to retrieve the first value of a data set, will always be completed in one step, regardless of the number of values in the data set.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDQ4NTkzMTM4LDE1NjEzMDkwNjAsLTEyNT
Q3NzExOCwtNzM0NzU4NjI5LC0zMTU3NzAzMDAsMTc0NzE1MjEz
NCw1ODkwMzcyOThdfQ==
-->