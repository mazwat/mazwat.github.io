---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 1

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    next:
        content: OOP
        url: '../oop-lm'
---

# Arduino

The following materials are derived from the *Arduino lecture*. The video lecture is included at the bottom of the [document](#video-lecture).
{: .callout .callout--warning}

In this lecture we will look at Arduino in subsequent lectures we will explore the other elements of the workflow.

## Introduction to the Arduino UNO  
 The arduino is a single board microcontroller designed to be used a controller for robotics and electronics projects.
 It is comprised of a 

### The Board

The Arduino is essentially a microcontroller with a range of peripherals attached to a **PCB** (printed circuit board) that allow for differnet externals to interface with the microcontroller these include things like: power, usb serial port for uploading firmware programs from a computer, a clock and most importantly it uses **pin** inputs so sensors and actuators can communicate with the controller.

![Arduino Layout](images/arduino-layout.png)
*fig1. - Arduino Board Layout*

### The Micro Controller

A micro controller is different from a microprocessor that consists of only a Central Processing Unit, whereas a Micro Controller has a range of other components and peripherals.

![Micro Controller Layout](images/micro-layout.png)
*fig2. - Microcontroller Features*

- **CPU** - The main function of the CPU Core is to ensure the correct program execution. The CPU must therefore be able to access memories, perform calculations, control peripherals, and handle interrupts.
- **Flash Memory** - Program Space. This is where the program you will write known as a ‘sketch’ is stored. There is 32kb of Flash Memory
- **SRAM** - (Static Random Access memory This is where the sketch creates and manipulates variables when it runs. The SRAM is only 2kb
- **EEPROM** - is memory space that programmers can use to store long term information. You are probably familiar with the term ROM from previous studies. EEPROM is only 1024 bytes
- **I/O Ports** - These are bi directional ports to manage communication between the CPU and peripherals.
- **Clock** - The clock can run at 16 MHz or 16 million cycles a second.
- **ADC** = 10 bit ADC means it has the ability to manage 1,024(2 to the power of 10) discrete analog levels. We will look at analogue later in this presentation.
- **USART** - Universal synchronous and asynchronous receiver transmitter - Used for communication between the microcontroller and computers on other devices
- **SPI** - Serial Peripheral Interface allows high speed synchronous data transfer between the device and peripheral units, or between several AVR devices, the CPU on the ATmega is AVR

### Form Factor

The controller is the essential bit you could make your own board up by adding the other peripherals manually, as in the example below, but the Arduino board is a cheap effective and less time consuming alternative to building your own.

![Home made board](images/home-made-board.png)
*fig3. - Home Made Arduino Board*

## What is the purpose of an Arduino Board?

It's a rapid prototyping board. It gives you the ability to quickly plug pins from the Arduino to devices and components on a bread board to rapidly prototype creative electronic projects.

![Arduino and Breadboard](images/board-bread.png)
*fig4. - Arduino, breadboard, LED and resistor*

Arduino is often thought of as the preserve of hobbyists and creative makers, but it has other more serious applications.

| ArduSat  | OceanBot |
|--|--|
|![ArduSat](images/ardusat.png)|![OceanBot](images/oceanbot.jpg)|
| The **ArduSat** satellites are powered by the Arduino Uno. It  follows cube satellite (CubeSat) standards to build  compact 10 cm cubes that can easily be sent to orbit. The company has "the goal to democratize access to space". | This robot prototype swims underwater and is propelled by fins, it was developed at the Control Systems and Robotics  Laboratory of the **Technological Educational Institute of  Crete**, in Heraklion (Greece) and it’s controlled by an  Arduino Mega. |

## Principles of Robotics
To further understand how to apply Arduino in your own practice it is useful to think of the 3 key principles of robotics and engineering this is also referred to as **Process Control**:

- **Sensing** - measuring an input, like a button press or change in light levels.
- **Controlling**- adjusting an *actuator* in response to the measurement from the *sensor*
- **Actuating**- manipulation in order to cause an action

A common example of this is the humble **toilet**. The sensor is the ballcock or float in the cistern that measures the level of the water. If the water is too low it will open the valve to allow more water into the cistern. The valve is the actuator as it manipulates a mechanism to cause an action - to allow or to prevent the flow of water. The controller is a small screw that allows the user to adjust the height that the float reaches before opening the valve.

<iframe width="100%" height="400" src="https://www.youtube.com/embed/v_kMOMYq0MU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

*fig 5. - Petit Mal by Simon Penny*

The above video showcases a robot designed by Simon Penny in 1996. The goal of 'Petit Mal' is to produce a robotic artwork which is truly autonomous.  This example is particularly relevant to the above principles. The robot is **sensing** using an array of ultrasound sensors to detect the presence of a human and responding by getting close and then backing away. Its **actuators** - the motors are being driven in different directions by the **controller** which in turn is adapting to the input from the sensors. This is a constant feedback loop.

Simon Penny its creator describes the robot as being: 

> *"..nimble and charming; sensing and exploring architectural space and pursuing and reacting to people; giving the impression of intelligence but displaying a behavior which is neither anthropomorphic nor zoomorphic, but which is unique to its physical and electronic nature."*

This is something to think about with your projects. how can you create a project that defies the usual expectations of interaction. How can we challenge our assumptions about human or animal interfaces with machines. How robots can appear to convey emotions like curiosity or aggression. Robots are different beings with a very different situated intelligence.

In another lecture I will introduce **cybernetics** and we will look at the concept of *situated intelligence* in more detail.

## Control Systems

So to create a system relevant to this module we need to define what sensors, controllers and actuators. In your project you can use any of these as building blocks for your system. I have listed some examples but there are many more that you could use. These come in the form of components that are easily bought very cheaply, some can also be found in common consumer devices.

![Sensors Controllers and Actuators](images/sensors-actuators.png)
*fig6. - Different types of sensor and actuator*

Here are a couple of examples of custom control systems for games. 

![Inputs and Outputs- Example 1](ball-controller.png)

IN the first example a large exercise ball is being used as a control system for a game about world domination. This has the interesting effect of literally giving you the feeling of having the whole world in your hands. The use of rotary encoders to map relative rotation of the ball in both a vertical and horizontal direction to a virtual globe in the game is very effective. 

![Inputs and Outputs - Example 2](samba.png)

In the second example here are some of my friends playing *Samba de Amigo* designed for the **Wii controller** in 1999. The Wii controller makes use of an infrared bar that detects the position of the controller in vertical and horizontal space and accelerometers in the hand controller which detect the nature and speed of the movement in 3d space. The Wii controllers had this maracca wrap around to enhance the imm
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTYxNjc4MzM5MywxMDE3NzE4NjcxLDExNj
k3NzA1MTcsMTcyNDEwNjkyMSwtMTYzNzc2OTc4OCwtMTMzNDgw
MjM5NywxNTQwODcxNzcyLC0yMjA2OTUyMDQsLTE4Nzc0OTQwND
AsNzAxMTQzOTg3LC04OTQwMzUwNDcsMzQ5NzY4MzAxLC0xMzAw
NDk5MzgzLDM4NjAyMjYyMiwxMDY3ODg4MzE4LDMwNTk0MzMzMy
wtMTc1MTkxMjA5NywyMTA0MTIzNjA4LDE4MDI0NTUzNTksNDc5
MjM5ODI4XX0=
-->