---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 8

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: Data Structures
        url: '../data-structures-lm'
---

# Design Patterns

![Hero Banner Image](images/patterns-hero-banner.png)

The following materials are derived from the *Design Patterns lecture*. The video lecture is included at the bottom of the [*document*](#video-lecture).
{: .callout .callout--warning}


## Introduction

Design patterns was written in 1994 by the ‘Gang of Four’ - Erich Gamma, John Vlissides, Richard Helm &  Ralph Johnson. Design patterns are set of procedures or patterns that help to make OOP code more effective and reusable.

Design patterns establish consistency that helps developers build and modify code safely avoiding common architecting problems. 

- Using consistent methods to fix and to avoid issues. 
- Having a shared language to understand common problems
- Adhering to the SOLID principles of object-oriented programming.

### Object Oriented Design Basics

Design Patterns are intended for object orientated systems as they tend to exhibit recurring structures that promote:

-   **Abstraction**
-   **Flexibility**
-   **Modularity**
-   **Elegance**

Abstracts a recurring design structure and comprises class and/or object:

-   **dependencies**
-   **structures**
-   **interactions**
-   **conventions**

Names and specifies the design structure explicitly and thereby distils design experience

### Formalising the Relationship between Objects

Design patterns have some basic similarities there is almost always a **client** that requests something or makes use of the pattern. There is also a **subject** that is usually creating, producing, changing, observing or providing access to the object which is usually a **product** in the system or a game object on screen.

![Relationships between objects](images/objects-dp.svg)
*Fig. 1 - Relationships between objects*


### The Design Pattern Categories

Design patterns are divided into 3 principle types which relate to their role in a process or application.

![Relationships between objects](images/dp-categories.svg)
*Fig. 1 - The 3 main categories of Design Patterns*

Within these categories are the patterns themselves. I have listed the principle ones below. In this lecture we are going to explore a small subsection which are in bold.

**Creational**|**Structural**|**Behavioural**
:-----:|:-----:|:-----:
***Abstract Factory***|Adapter|Chain of Responsibility
Builder|Bridge|Command
***Factory***|Composite|Interpreter
Object|Decorator|Iterator
Pool|Facade|Mediator
Prototype|Flyweight|Memento
Singleton|Proxy|Observer
 | |State
 | |Strategy
 | |Template
 | |Visitor



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQ2MzM0MDU0LC0xNDM5NDAyMzYwLC05Mz
YyMDg1NDIsLTMzODc0MTM0MiwtMjA3NDc0Nzk5MywtOTc1ODc4
Mjc4LC01MTM2MDk2NTAsLTY1ODI2NTI5OCwxOTA4NDY1ODEzLC
0yMDI4MTgyOTYyLC0yMTMwNjU5OTU1XX0=
-->