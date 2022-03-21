---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Worksheet 6

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: Design Patterns
        url: '../design-patterns-ws'
---

# States & Transistions

This week your primary focus for the workshop should be on your project and your specific needs and requirements.

The theme for the week is intended as supporting material for the development of your final product. One of the key elements of the lecture was implementing **finite state machines**.

## Finite State Machines

One of the key areas where realtime applications fall down whether it's a computer game or an automous robot is handling the concurrent states and transitions. It's vital to identify different states in the system:

 - *Button ON*
 - *Button OFF*
 - *Character IDLE*
 - *Motor FORWARD*
 - *Motor REVERSE*
 - *Led BLINKING*
 - *Audio PLAYING*
 - *Enemy IN RANGE*

There are numerous states in a system and often these are monitored in relatively naive ways. Using an `if` statement or  a `switch case` nested in an `update` or a `loop`. We may still deploy these to detect thresholds but nonetheless we can use more advanced programming techniques to manage and transition effectively avoiding **ambiguity**, **memory leaks** and **continuous calibration**.

## Suggested Tasks

 1. Identify what the **states in your system**?
 *Pay specific attention to the hardware/embedded software aspect. Have a method to measure when LED's are on or off, for example*
  2. Develop a **state diagram** to describe them and the transitions associated with them
3. Consider refactoring your code around the **state design pattern**. The State pattern suggests that you create new classes for all possible states of an object and extract all state-specific behaviors into these classes.

## Supporting Materials

Refactoring Guru - State Design Pattern
[https://refactoring.guru/design-patterns/state](https://refactoring.guru/design-patterns/state)

Arduino State Pattern Example Repo
[https://www.tinkercad.com/things/iK5nt1hK1a1-state-machine-v2/editel?sharecode=1rTt9kOGr6jWJCP3FerWqFwGnoi-TieRCMLcAtDSPO0](https://www.tinkercad.com/things/iK5nt1hK1a1-state-machine-v2/editel?sharecode=1rTt9kOGr6jWJCP3FerWqFwGnoi-TieRCMLcAtDSPO0)





<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc0MjI4NjQ2LC0xMjQzNzk4NDQ3LC0xND
UyOTA3MjE2LDE0NTM4ODU0ODgsMTA2NjAwNzgxOF19
-->