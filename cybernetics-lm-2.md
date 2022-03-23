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
*Fig. 1 - Greek Fighting Ship and tablet from circa 800 BC*

Cybernetics comes from the Greek word - **kybernetes** which means ‘_steersman_’ and relates to the principle of controlling or directing of a system. The ancient Greeks dominance of the classical world was in part due to their mastery of machines. Specifically fast fighting ships, packed with Spartan warriors. Consequently the **kybernetes** who steered them throughout the Mediterranean sea had a very important role to play.

![Cybernetics book](images/cyber-book.png)
*Fig. 2 - Cybernetics book*

The seminal text on the subject is *Cybernetics or Control and Communication in the Animal and the Machine* By Norbert Weiner who is considered the father of cybernetics.

Wiener described the field like this: 

*"Control and communication in the animal and the machine"*

Cybernetics is also about learning processes from animals and plants and using robotic simulations to gain a better understanding of complex natural systems.

![Lemur Jumping](http://38.media.tumblr.com/85a4d3868504f9df624084ed91d6c8ca/tumblr_nbf6a2C26U1s391qwo1_500.gif)
\*fig. 3 - Attribution Source: [www.9fail.com](http://www.9fail.com/post/96689672071/lemur-gif)*

We are used to associating robots with the imitation of humanoid behaviour but sometimes a simpler form of perambulation like, that we see in lemurs overcomes some of the complexity of attempting to move through an environment. If a robot can constantly jump it resolves the need to have complex feet or wheels, springs and differentials to adapt to changing terrain. When it hits any surface it jumps, if it is suitably well balanced it can stay mobile. 

<iframe width="100%" height="315" src="https://www.youtube.com/embed/xvIk39rkkiU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This example ‘Salto’ by USC Berkeley’s robotics lab shows how study of an animal jumping process can help to develop better robotic locomotion and navigation. We will return to this idea of mimicry later, but first let’s address some fundamentals.

### Early Cybernetics

![enter image description here](https://www.arshake.com/wp-content/uploads/2014/02/wiener-cart-corner-1-500x4611.jpg)
*fig. 4 - Norbert Wiener - Image Attribution: [Arshake](https://www.arshake.com/en/norbert-wiener/)*

In its early years in the 1920s and 30s cybernetics was concerned with the problem of tracking targets (optically and then with radar), predicting their future positions, calculating ballistics, and directing guns to fire to destroy the targets. Norbert Wiener, a brilliant but eccentric MIT mathematician, already had a successful career in which he made numerous contributions to mathematics particularly to fields like harmonic (Fourier) analysis and stochastic processes. However Wiener’s work proved to have little application to wartime problems (it generated ponderous, complex solutions) but it did lead him to produce an important paper that paved the way for the modern theories of optimal estimation and signal processing. He created a general theory of smoothing and predicting any problem expressed as a discrete series of data. This generalization, from a specific human/machine problem to any aspect of the world that can be expressed as time-series data, presented an early glimpse of the strategies that would define cybernetics.

![Photo of the Earth](images/earth.png)
*fig. 5 - Photo by [NASA](https://unsplash.com/@nasa?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/earth?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)*

Weiner’s work on measuring natural systems with time series data lead the scientist James Lovelock to propose The Gaia hypothesis which posits that the Earth is a self-regulating complex system involving the biosphere, the atmosphere, the hydrospheres and the pedosphere, tightly coupled as an evolving system. The hypothesis contends that this system as a whole, called Gaia, seeks a physical and chemical environment optimal for contemporary life. Cybernetics can be used to measure all life as we know it.

### The Cybernetics Loop

![Cybernetics Loop](images/cybernetic-loop.svg)
*fig. 6 - Cybernetic Loop*

**Sensing**, **Controlling** and **Actuating**. Any computational system that is effected by the real world must have a way to sense it in some way, maybe it’s a button, a camera, a microphone, or a light sensor. The data from the sensor is then measured and processed by the controller this is usually a computer but it can be simpler (as we well address later) and depending on the how the data is interpreted an actuator is started. This could be a motor turning a wheel, a pump or even moving a virtual object in a game or storing data point in a database. This process is a continuous feedback loop, The actuation may well effect the state of the sensor data, and so the process returns to the start to begin all over again.  Cybernetics is also highly relevant to thinking about control scheme’s and player feedback in games. In games design one of the fundamental principles is the game feedback loop which is derived from Cybernetic principles.

![enter image description here](images/causal-loop.svg)
*fig. 7 - Causal Systems*

Cybernetics explains how circular causal systems work or what we call single loops. So as well as defining the inputs and outputs we also need to factor in the goal of the **actor** and how factors in the **environment** can cause **disturbances** to the achievement of that **goal**.

![enter image description here](images/steer.gif)
*fig. 8 - Steering a ship into port*

If we return to our steersman in Ancient Greece.  We can see that the **goal** is to reach a safe port, and the input of rowing and wind in the sails should push the boat along its course. But the tide or wind of a real system like the sea can disturb the smooth procession of the vessel. The steersman has to measure the **disturbance** and apply a **correction** to overcome the error created by the **environment**.



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MTc2NjkzMzYsMTUyMjMzMDgyNywxNz
MyNTMxNjY4LC0zNTgwNDEwOTYsLTgwMzkzNTU0NiwtNDUxNzgz
MzMzLC0yMDY0NDI5NzIsLTEwMDcwMjc4MzAsLTEzNTMzOTYxOD
QsMzk0Njg3MzI2XX0=
-->