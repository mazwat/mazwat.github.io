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

-   In programming we have the concept of reusable data structures which can be used to build applications
-   These can be used in order to build larger systems (e.g. Inventory Systems, AI Navigation etc)
-   Most programming languages have these built in
-   Before writing any system you should always examine these data structures and pick the appropriate one for your Use Case

## Big 'O' Notation

*“Measuring programming progress by lines of code is like measuring aircraft building progress by weight.”*
Bill Gates

How we want to define our code is based on two simple premises: **Simplicity** and **Purpose**.

### What is Bit 

One of the ways to make our code efficient is by optimising the search for data within a data set.
Let's consider how we search a data set of 100 items for a single data point. For example in a data set of 100 items, you are searching for an ‘O’ amongst ‘X’s.

| <!-- -->  | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> |
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

The **best case** for finding the data is **1 iteration**
The **worst case** is a **100 iterations**

Big ‘O’ is based on worse case scenario

100 records would take 100 iterations

N records would take N iterations

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMzc0OTAxMjQsLTEyNTQ3NzExOCwtNz
M0NzU4NjI5LC0zMTU3NzAzMDAsMTc0NzE1MjEzNCw1ODkwMzcy
OThdfQ==
-->