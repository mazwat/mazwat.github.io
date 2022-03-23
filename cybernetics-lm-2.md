---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: 9. States & Transitions
description: COMP140 - Lecture Materials 9

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
        url: '../design-patterns-lm'
    next:
        content: Optimisation & Performance
        url: '../optimisation-lm'
---

# 9. States & Transitions
## An Introduction to Cybernetics

![Header Image](images/states-header.jpg)

In this lecture I plan to outline some key theories but also their application in the field of Cybernetics. Cybernetics is commonly applied to robotics but its applications are relevant to all areas of computing and design and especially realtime systems like computer games where we are dealing with the transformations between the states of a system.

This can be useful in thinking about both the physical and virtual components of your system but also the human interface with the experience you intend to develop.

### Learning Outcomes

-   Outline the meaning and application of **cybernetics**
-   Explain and apply **transformations** between states using **kinematics**
-   Define the role of **transistors** as simple neurone in electronic control systems
-   Identify uses of **signal processing** in embedded systems
-   Apply cybernetics to electronics projects in the form of **finite state machines**

## What is Cybernetics?

_“Cybernetics is the study of human/machine interaction guided by the principle that numerous different types of systems can be studied according to principles of feedback, control, and communications. The field has a quantitative component, inherited from feedback control and information theory, but is primarily a qualitative, analytical tool – one might even say a philosophy of technology.”_ - David A Mindell - MIT

![Greek Ship](images/greek-ship.jpg)
*The steersman of a Greek Fighting Ship*

Cybernetics comes from the Greek word - **kybernetes** which means ‘_steersman_’ and relates to the principle of controlling or directing of a system. The ancient Greeks dominance of the classical world was in part due to their mastery of machines. Specifically fast fighting ships, packed with Spartan warriors. Consequently the **kybernetes** who steered them throughout the Mediterranean sea had a very important role to play.



The seminal text on the subject is *Cybernetics or Control and Communication in the Animal and the Machine* By Norbert Weiner who is considered the father of cybernetics.

Wiener described the field like this: 

*"Control and communication in the animal and the machine"*

Cybernetics is also about learning processes from animals and plants and using robotic simulations to gain a better understanding of complex natural systems.

§![Lemur Jumping](http://38.media.tumblr.com/85a4d3868504f9df624084ed91d6c8ca/tumblr_nbf6a2C26U1s391qwo1_500.gif)
*Attribution Source: [www.9fail.com](http://www.9fail.com/post/96689672071/lemur-gif)*

We are used to associating robots with the imitation of humanoid behaviour but sometimes a simpler form of perambulation like, that we see in lemurs overcomes some of the complexity of attempting to move through an environment. If a robot can constantly jump it resolves the need to have complex feet or wheels, springs and differentials to adapt to changing terrain. When it hits any surface it jumps, if it is suitably well balanced it can stay mobile. 

<iframe width="100%" height="315" src="https://www.youtube.com/embed/xvIk39rkkiU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This example ‘Salto’ by USC Berkeley’s robotics lab shows how study of an animal jumping process can help to develop better robotic locomotion and navigation. We will return to this idea of mimicry later, but first let’s address some fundamentals


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MjMzNjY1NzMsLTEzNTMzOTYxODQsMz
k0Njg3MzI2XX0=
-->