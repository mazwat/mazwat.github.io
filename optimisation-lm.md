---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: 10. Optimisation & Performance
description: COMP140 - Lecture Materials 10

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: States & Transistions
        url: '../cybernetics-lm'
---

# 10. Optimisation & Performance

The following materials are derived from the *Optimisation & Performance lecture*. The video lecture is included at the bottom of the [***page***](#video-lecture).
{: .callout .callout--warning}

-   Explain the role of optimisation in the development of software
-   Identify the role of hardware in performance.
-   Assess various techniques to optimise your code
-   Apply these methods using specific tools.

## Introduction

One of the important aspect of programming is **optimising** for **performance**. We need to understand the **hardware** our products will be deployed onto, We need to understand the **programming languages** we use. We also need to understand the **frameworks, platforms** or **game engines** we develop for. And finally we need to understand the **tools** we can use to tune **performance**.

## Memory

The most fundamental factor in understanding how we can fine tune our projects is to identify the role played by memory.

**Memory** in most modern programming languages is allocated in two spaces

-   **Dynamic memory** (allocated with new) is allocated on the **Heap** and will grow in size
-   **Stack memory** (everything that doesn’t use new) is allocated on the **Stack** and is fixed size

Let's further clarify the differences between the two types:

|STACK| HEAP |
|--|--|
|The memory is allocated at the **compile time**.| The memory is allocated at the **runtime**.|
|In static memory allocation, while executing a program, **the memory cannot be changed**.| In dynamic memory allocation, while executing a program, the **memory can be changed**.|
|Static memory allocation is preferred in an **array**.  | Dynamic memory allocation is preferred in the **linked list**. |


## Video Lecture

<iframe width="100%" height="370" src="https://web.microsoftstream.com/embed/video/f40015bb-d506-4ffc-9a7a-8e90069ffdae?autoplay=false&showinfo=true" allowfullscreen style="border:none;"></iframe>

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg0NTYzNjc0NSwxNTExMzYxMjgzLDEwOD
EwODU5MjFdfQ==
-->