---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 6

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: Software Architecture
        url: '../software-architecture-lm'
    next:
        content: Data Structures
        url: '../data-structures-lm'
---

# Unified Markup Language

![Hero Banner Image](images/uml-hero-banner.png)

The following materials are derived from the *UML lecture*. The video lecture is included at the bottom of the [document](#video-lecture).
{: .callout .callout--warning}

## What is UML?
UML is a **visual notation system** which can be used to design software. It was first devised in **1996** by Booch, Jacobson and Rumbaugh. The goal was to **unify/standardise** all the various modelling languages and diagrams used in Software Development. In **2005**, ISO published UML as an **international standard**. **UML 2.0** is the most current version, with **14 different diagram types** defined as being part of UML.

![Inventors of UML](images/booch.png)
*fig.1 - Booch, Jacobson and Rimbaugh, the devisors of UML*

### Why use UML?

-   UML offers us a **standardised way of designing** software
-   It allows us to **think through our systems** before committing them to code
-   It offers a **shared language** between programmer and other disciplines including **clients**

## Diagram Families

![UML types](images/uml-types.png)
*fig.2 - UML types*

UML can be divided into **2 types**:

1. **Behaviour Diagrams**
– Describes what happens in a system, this includes interactions between users and the system
– Or the current system and other external systems

2. **Structure Diagrams**
– Describes what is contained in the system
– Typically used to model the system

## Behavioural Diagrams

### 1. Use Case Diagram

Use Case diagrams typically details the user’s interaction with the system. In essence it details the **Use Case** of the **System** and the **Actors** which interact with the system

– NB. These Actors could be other systems!
{: .callout .callout--info}

- Created using terms that a layperson could understand
- Can be used to capture and communicate User Requirements
- This is often the first diagram created for a system
- An attempt to represent the key features of a system and it's goals.

![Use Case Diagram](images/use-case-1.svg)
*fig.3 - Use Case Diagram - Banking App*

The above diagram describes as system for a mobile banking app.  

 1. The **bounding box** describes everything contained within the system and outside it are the actors which are the customer or user and the bank itself (which could equally refer to an employee or the system itself). 
2. In the **ellipses** we have the **features** of the system - Login, Check Balance etc. 
3. The **lines** connecting them represent interactions between the actors and the system and are called **associations**.  
4. Finally a line with an **arrow** signifies a **generalisation**  which denotes a parent/child relationship. Tne arrow always points towards the parent.

![Include and Extend-extend](images/include-.svg)
*fig.4 - Include and Extend*

## Tools for making UML

1. **Diagram** - [http://www.diagram.net](http://www.diagram.net)
2. **Lucid Chart** - [https://www.lucidchart.com](https://www.lucidchart.com)
3. **Gliffy** - [http://www.gliffy.com](http://www.gliffy.com)

There are many more you can use but these are some of the best.

Many of the above options are freemium. You may have a limited number of diagrams you can make or a time limit for use. Just be aware of the pay wall when using these tools.
{: .callout .callout--warning}
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM4OTY1Nzg4NCw2NjExNTEyNzAsMzE1MD
M0NTkwLC0yNjU5Nzc5NTEsLTkzNTI4NDk5NSwyNTA5MDY0OCwt
MTk1Nzk0OTUyMCwxNjM5MDMyNzcxLC04MzA2OTI0NjAsLTEzOD
c5MzU5NDVdfQ==
-->