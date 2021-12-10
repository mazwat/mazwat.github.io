---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 3

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: OOP
        url: '../oop-lm'
    next:
        content: UML
        url: '../uml-lm'
---

# Software Architecture

## So what is Software Architecture

A way of establishing **patterns** for the development of software.  These architectural patterns are a description of the **relationship** types and **elements** as well as the **constraints** or **limitations** in the system being built. Patterns are usually **reusable solutions** to common problems.

Ralph Johnson a famous programmer and professor at the University of Illinois, who co-authored one the essential books on programming called *Design Patterns*. Design Patterns is something we are going to look at in a later lecture. He questions this idea of architecture, arguing that there was no objective way to define what was fundamental, or high level and consequently there was no formal notion of established structure implied by the word architecture and that a better way to describe this approach is the:

***‘shared understanding that the expert developers have of the system design’***
***The decisions you wish you could get right early in a project'***

Johnson also cryptically said this:
  
***“Architecture is about the important stuff. Whatever that is”***

### Networks of Dependency

As we write code and our projects scale the interconnecting parts can become confusing. We sometimes generate dead ends or unnecessary code that causes our applications to slow down or to become needlessly complex, this waste is known in programmer circles as - **cruft**! 

So having some basic principles to help to design the link between objects, classes and functions is incredibly useful. We want to limit the proliferation of cruft.

## Principles of Software Architecture - SOLID

**SOLID** is basically 5 principles, which will help to create a good software architecture. You can see that all design patterns are based on these principles. SOLID is basically an acronym of the following:

-   **S** is single responsibility principle (SRP)
-   **O** stands for open closed principle (OCP)
-   **L** Liskov substitution principle (LSP)
-   **I** interface segregation principle (ISP)
-   **D** Dependency injection principle (DIP)

In this lecture we are going to focus on the first 3 and finally we are also going to look at Order of Execution as it links to how the SOLID principles work.

1.  **Single Responsibility Principle -** every class in a computer program should have responsibility over a single part of that program's functionality, which it should encapsulate.
2.  **Open Closed Principle -** software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.
3.  **Liskov’s Substitution Principle** - if poodle is a subtype of dog, then objects of type dog in a program may be replaced with objects of type poodle without altering any of the desirable properties of that program
4.  **Order of Execution /** **Game Loop -** The flow between processes in software and hardware.

You can see how features of OOP from the previous lecture form a major part of SOLID principles. Specifically objects encapsulation, classes and objects.

## Implementing SOLID

### Single Reponsibility Principle

*“…it is almost always incorrect to begin the decomposition of a system into modules on the basis of a flowchart. We propose instead that one begins with a list of difficult design decisions or design decisions which are likely to change. Each module is then designed to hide such a decision from the others.”*

_David R Parnas -_ [_On the Criteria To Be Used in Decomposing Systems into Modules_](https://www.cs.umd.edu/class/spring2003/cmsc838p/Design/criteria.pdf)_. 1972

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM3NDgzOTA1MSwtMTU3NTk2NTk0OCw2MT
Q5OTk3NzcsMTA0ODAwNjQ4NywyMTkxOTA4MjcsLTE0MzIzMzU0
MjhdfQ==
-->