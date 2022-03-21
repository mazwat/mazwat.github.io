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

The theme for the week is intended as supporting material for the development of your final product. One of the key elements of the lecture was implementing finite state machines.

## Finite State Machines

One of the key areas where realtime applications fall down whether it's a computer game or an automous robot is handling the concurrent states and transitions. It's vital to identify different states in the system:

 - Button ON
 - Button OFF
 - Character IDLE
 - Motor FORWARD
 - Motor REVERSE
 - Led BLINKING
 - Audio PLAYING
 - Enemy IN RANGE

There are numerous states in a system and often these are monitored in relatively naive ways. Using an `if` statement or  a `switch case` nested in an `update` or a `loop`. We may still deploy these to detect thresholds but nonetheless we can use more advanced to 



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2OTQ4MDcyMjUsMTA2NjAwNzgxOF19
-->