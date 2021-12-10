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

-   **S**ingle responsibility principle (SRP) - every class in a computer program should have responsibility over a single part of that program's functionality, which it should encapsulate.
-   **O** stands for open closed principle (OCP)
-   **L** Liskov substitution principle (LSP)
-   **I** interface segregation principle (ISP)
-   **D** Dependency injection principle (DIP)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NTcwMzg5MTAsNjE0OTk5Nzc3LDEwND
gwMDY0ODcsMjE5MTkwODI3LC0xNDMyMzM1NDI4XX0=
-->