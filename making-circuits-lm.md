---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 2

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: Electrical Circuits
        url: '../electrical-circuits-lm'
    next:
        content: Arduino
        url: '../arduino-lm'
---

# Making Circuits

The following materials are derived from the *Making Circuits lecture*. The video lecture is included at the bottom of the [document](#video-lecture).
{: .callout .callout--warning}

In this lecture we will look at how to use TinkerCAD to make simple Electrical Circuits and the basics of your first program in Arduino.

## Using TinkerCAD

We have established some basics of electricity and circuits, so now we're going to put it into practice. Initially
we're going to use a piece of software called [Tinkercad](http://www.tinkercad.com/). 

Tinkercad is a way to simulate electrical circuits, but also to simulate circuits and their use with a range of components as well as Arduino and other microcontrollers. 

![Simple Circuit](images/tc-interface2.png)
*fig 1. - TinkerCAD Interface*

### TinkerCAD Interface

What tinkercad is very good at is simulating. The environment of Arduino so that we can build things with low cost in terms of putting it together and then we can test it through a simulation (2 in fig. 1) of the Arduino environment. You can drag components on to the stage from the right hand inspector (3 in fig. 1). We can also write code in order to demonstrate it (1 in fig. 1). However, this is just a test environment it's important to actually use your own Arduino and the Arduino IDE in conjunction with the USB connection to your Arduino. This is just a way to
test the process before you implement it for real.

![Simple Circuit](images/tc-simple.png)
*fig 2. - Simple Circuit*\
**[View Circuit on TinkerCad](https://www.tinkercad.com/things/aefmW5mPE86-simple-electric-circuit/editel?sharecode=bjxDkcj1jYkU3qDBDux5XN-GflpCaIIjGHqfXsWVICQ)**

Here is a simple circuit. We need a source of power. So in this case we're going to use a simple coin battery, and we're going to have a light an LED, and basically all we need to do is wire the two together. To wire something in TInkerCAD just pull away from the pin or terminal of the battery or component and a line will appear. These line are equivalent to the jumper leads you use in a real circuit on a breadboard.

LED's have a longer pin and a shorter pin. The  longer pin is positive (+) and shorter is negative (-). So we wire the LED accordingly. 

Once we have the Led in our circuit we have a put a 'load' on the circuit by introducing the LED which is using power. If you start the simulation you can see that the load is too much for the LED, a questions mark appears warning us thar the LED will burn out if we don't resist the flow of electricity.

### Resistance Calculation

We need to add a resistor. In order to workout which resistor to use, we need to workout the resistance value and that is done by a resistance calculation which is:
  
$$R = \frac{V_S - V_	L}{I_L}$$

- **VS** is the source voltage, measured in volts (V),
- **VL** is the voltage drop across the LED, in Volts (V),
- **IL** is the current through the LED, in Amps (A)
- **R** is the resistance, measured in Ohms (Ω).

This is a variation of **Ohms law**, but applied specifically to LED's. We can use an online calculator to make things easier:

**[https://www.hobby-hour.com/electronics/ledcalc.php](https://www.hobby-hour.com/electronics/ledcalc.php)**

We need to workout:

 - **Supply voltage** . We know that we are using a  Volt coin battery so our supply
voltage is 3 volts.
-  **LED current** The standard load on an LED is about 20 milli amps
The great thing with this this
- **Voltage drop** - This is the voltage being used in the circuit by the LED. Typically, the forward voltage of an LED is between 1.8 and 3.3 volts. It varies by the color of the LED. A red LED typically drops around **1.7 to 2.0 volts**, but since both voltage drop and light frequency increase with band gap, a blue LED may drop around 3 to 3.3 volts.

Once the numbers above are added to the calculator **3v, 20mA** and let's say it's a red LED so its **2v**. The output is this:

![Resistance Calculation](images/resist-calc.png)
*fig 3. - Resistance Calculation*

You won't necessarily have the exact resistor in your Arduino Kit, but you just want to round up to the closest
resistor in your pack when you actually physically wire this together. 

![Simple Circuit with resistor](images/rc-simple-resistor.png)
*fig 4. - Simple Circuit with Resistor*\
**[View Circuit on TinkerCad](https://www.tinkercad.com/things/aefmW5mPE86-simple-electric-circuit/editel?sharecode=bjxDkcj1jYkU3qDBDux5XN-GflpCaIIjGHqfXsWVICQ)**

If we start the simulation, we've now got the light coming on, but there's no exclamation mark as we no longer over powering the LED. It's something to be wary of becuause LED's can easily burn out.

### Control Systems - A Switch

We're going to put a switch in there to allow a user to control the flow from the battery to the LED. To turn it on and off.

In this example we are going to change the configuration slightly by including a breadboard. A breadboard is essentially a set of rails in a board that conduct the power through channels either **horizontally** or **vertically** depending on the rail. The rails have plugholes so that components and jumper leads can be plugged in. See the image below to see how this occurs on the board:

![Breadboard](images/tc-breadboard.png)
*fig 5. - Rails on a Breadboard*

Breadboards allow us to create complex layouts of components without having to solder. It's an electronics sandbox environment.

![Simple Circuit with resistor](images/tc-circuit-switch.png)
*fig 6. - Simple Circuit with Switch*\
**[View Circuit on TinkerCad](https://www.tinkercad.com/things/j2mHkxwsdeL-basic-circuit/editel?sharecode=lUW-e_VPCYdwvUkmJTQy4I5D_la_LC-eEi7h7Q3y9gE)**

In the above example we use the horizontal tracks on either side of the breadboard to plug the battery in. The horizontal tracks are marked with **red (+)** and **black (-)**. It is not essential to use them for the positive or negative terminals but using the red and black convention helps to avoid confusion. The reason for using the horizontal tracks means we can plug multiple components into this track across the length of the breadboard and draw power from the power source.

A cable from the battery is plugged into the red and black track on either side of the board anf then cables are connected to the LED and the resistor. However we have one more component to add the mix.

A switch is a means to interrupt the flow of electricity in a basic **single throw** switch it either on or off.  But the switch in the above example is a **double-throw** switch as it has 3 terminals (see below). Terminal 1, Common and Terminal 2

![Switch](images/switch.jpg)
*fig 7. - Double Throw Switch\

When the switch is in one position, the common terminal is connected to the A terminal, so current flows from the common terminal to the A terminal but no current flows to the B terminal. When the switch is moved to its other position, the terminal connections are reversed: current flows from the common terminal to the B terminal, but no current flows though the A terminal. Essentially this means we can use the pins to choose whether the switch starts in the **on position** or the **off position**.

In the diagram the swtich is wired to the right hand pin and the 

e

So I'm going to connect.



dc

This to there, and then I'm
going to connect that there.



eae

And.



-cccbeda

Make that black just so that we
understand. Now if we start the



-af-

simulation it is off.



ac

And then it's on. So this is
kind of a standard kind of.



-ffc

School Electric electronics
experiment. We've



aafa

essentially just wide a
battery to a light. You've



aa

probably seen this many
times. We've shown in the



ebfb

previous example, but this
shows how we can use



aefdf

tinkercad to create a.



-fabfd

Simulation of an electrical
circuit. Now let's just



bbbfd

advance this circuit a little
bit more by adding the



bdcbad

breadboard so the breadboard
has.



d

Has a number of different
pins on it, and it's a



ddbcd

kind of prototyping tool
'cause it allows us to



fdfa

plug different elements
together along a these



afafe

tracks and these tracks
allow us to.



cddcfe

Control the flow of electricity
in our circuit and it means



fb

that we can formalize the
process rather than doing it



fbdc

like we've done as in this
example that we just did. It



cbfedac

was a bit kind of it's a bit
chunky, it's a bit kind of



-ceebb

patched together. If you did
this for real, would literally



bbdaae

just be soldiering or kind of
tying bits of cable bits of



fdcfc

wire together in order to see
that this works, whereas the



dd

breadboard allows us to do
something kind of clean and



bee

functional way.



bbcdbc

So the important thing to know
about the breadboard is that it



aafdb

has a series of rails or tracks
and they flow. We have these



ddaaa

outer tracks which we call the



daac

power rails. OK, so this is plus



efaed

and minus. It doesn't matter the
breadboard. Essentially, these



-ddefea

are just. These are just bits of
metal wired together inside the



cefcdde

breadboard in order to create a
rail so it doesn't. It says plus



eeb

and minus, but it doesn't. This
is just as a guide, it doesn't



eae

really matter, so you have these
two rails which are horizontally



ad

connected, so anything connected
from here to here will be



afab

flowing along this rail switch
to the next thing, whereas these



bb

ones that they have horizontal



cccc

rails. Anne, these horizontal
rails can be.



-def

Are used to and this is
tend to be where we put



c-

our various components. So
let me just show you if I



dfda

take so I'm not going to.



bed

Take this off there for
a second.



bafd

Thing and put the Ellie D about
here and then what we're going



cb

to do is we're going to wire
this up a little bit more



-eccf

neatly, a little bit more
effectively. I'm going to.



ea

Take get rid of these.



cebac

For a moment, let's do it.



-ebfbb

In a different way.



cfdeb

So if we put the battery on
the side of the breadboard



febaadb

and then what I'm going to
do is, I'm going to attach.



-cbc

The plus to plus rail here and
the minus to the minus rail



-fffd

here. So what this means is that
we can run different components



-cfcd

from these rails, so it means we
can have multiple things going



cbbe

on on our bread board, and so
we've essentially. We've now



cbee

powered these rails, and then we
simply just have to kind of



bacc

connect them up. So what I'm
going to do is put my resistor



-ffeafbbb

here and then I'm just finally
going to put the.



ddbc

Switch here so when you when
you're actually doing this for



-cc

real in Arduino, you can. You
will see how much kind of this



badbdc

makes a lot of sense. This
project, 'cause it's A kind of



eab

plug and play with the jump wise
you can just plug them directly



e

into these little holes and it
makes life a lot easier. So now



-eeebedc

I'm going to do is take a cable.



c

From there to there and then a
cable from there.



ceee

.



-badc

Here and then. Finally, a
cable from there to there.



dbfb

Now if I just change the
colors of these just so that



baadd

it makes a bit more sense.



faedc

So now you can see that.



bace

We have the same circuit but we
have we have kind of although it



b

may look a more complex, it's
actually more functional and in



-fe

some ways it's more effective.
So we've got the power now



abe

running into this rail and it
runs down until it meets the



-ccabe

point where it can then transmit
here. Now these rails run



ffea

vertically, so the power will
then transfer to the resistor



e

over the resistor to the Ellie D





across. To the other pin of the
LEAD and then out through this



-eeffa

cable to the central prong of
the switch and then finally out



fb

here and then along this rail
and back into the battery to



-efcb

complete the circuit. So it's
just a much neater way of doing.



fcc

Thanks. So now what we're going
to do is introduce the Arduino.



dbb

We've just I've just opened a
brand new project up here.



bfbab

You'll notice how it likes to
call them by these.



accd

Strange names, so if we just
call this basic blink.



cb

What we're going to do is
introduce our Arduino.



edefa

OK, so I've just dragged an
example about doing so. This



cadfa

is going to simulate it.
It's got the kind of the USB



-abbbfc

plugged into the Arduino.



-bebda

So I have pre cleared this
but you normally get a bit



aebcab

of test code but I just
wanted to take you through



eabfe

the basic kind of code
layout. O Arduino has two



eefe

key functions or methods
within it, so it has both.



dbbfddaf

It has set up.



-fc

So for those for those of you
who are familiar with unity,



-fdff

there are some of these things
are fairly are similar, so this



aeba

is a little bit. The setup is a
little bit like the start and



-ccd

then the loop is a bit like
update or fixed update, so the



caac

setup is, well, we set up the
key things that we want to



fbc

happen. And then the loop is
what actually happens repeatedly



abbcb

through the program, so.



d

The first thing we're going to
write is this, which is PIN mode



dcebc

. I miss built like no soap in
Mode  is to do with the



ccbacb

output. It means that we're
going to. We're setting the pin



-ac

mode to output on PIN . OK,
now PIN  is both the pin that



bbff

we can see here, but it is also.



fedbd

The lights here so the both of
them are applicable. So if we



fe

say PIN mode  it will be
triggering this built in LED



bead

now. Now we want to actually.



eee

Write a digital signal.



cdeee

So as you run from previously
digital right is a on off



af

function, so we're sending it to



beedeccc

. And.



edbbe

We are setting it too high, so
this means that we want to set



bdc

the eleidy too.



fdb

Be on so it's high and
low, low is off or zero



bdcfdf

at high is on or one.



-efcc

Then delay.



-aefd

 So what we're getting
here is a delay, so there



-bebfcc

will be a delay of.



ee

So let's make this 
milliseconds. So this is



acf

measured in milliseconds, so it
waits for a second.



adabeec

After it's come on and then
we're going to. So what I'm



-aef

going to do is just to save
time. I'm going to copy and



fafbfa

paste this, and we're putting
another digital right, but



-db

this time we're going to set
it too low and there will be a



cdd

gap of  second between those
two things. So if I now start



c

the simulation.



-daefb

You can see that in our
example here, the LED light



-eacc

in the simulation is flashing
on and off for a second. We



-eebedabf

can shorten this time.



fbeadb

Let me just stop the simulation
so we could shorten this.



feaaccf

.



-b-

. And we can start the
simulation. So now it's a



ff

lot faster.



-ecacbd

OK, so let me just hide the
code. So we've created a very



-eeff

simple looping. Flashing Eli
D But we may want to start



cabcbe

expanding on that. So what
I'm going to do is introduce



fb

a breadboard.



bea

And we're going to put our trust
the Ellie D. Back in and we are



fdeea

going to do the simplest thing
that we can do, which is to.



bee

Why are ?



bd

Here.



fe

At 



-deda

here. And we take the grounds
because the ground. So we're



fdbe

taking power from our Arduino,
so we need the ground, which is



bedeb

our sort of this. Is there
negative? So we need to put that



eadf

into the negative pin of our
lead there, and we need to add



ffdbcce

our resistor. So I'm going to
just rotate that resistor and



ce

put it here. I'll put that in



fb

the wrong place. Let me just
zoom in a little bit there so.



-dffbb

And then we can see now.





And let me just once again
change the colors so that it



fb

makes sense. So the digital pin
is being so this the information



dedf

that the digital pin is being
turned on. And remember it's pin



-adfe

 and the ground will be black.



abdbffbc

And. This was,
I believe, .



-ceadd

So now.



abcd

Oh, I know why I stupidly put
this in the wrong place, that it



c

should be on the track there.





Except it's saying that it
doesn't like this.



bedbeb

Oh, hold on.



ecfed

So this time when we put the
resistor in, we need to use a



abfa

slightly different thing
because the Arduino is driving



afbad

 volts of power as opposed to
 volts of power. So we need



beebdde

to set the. We need to do our
calculation again.



ed

So if we take this example here
and we're going to say  volts



faefc

and it's got a  milligrams, is
the same 'cause that's the LED



fef

current. The voltage drop is
about  volts, so we calculate



a

again, so we've got .



-afc

Times.



eaa

There we go, so now we can see



fedbdbb

both. This Eli D onboard Eli D
is blinking but also the Eli D





that we've set.



-bccd

Here. So there is
our basic circuit.



aca

Make sure that you wire up
your Arduino as you can see in



ecea

this picture of the circuit
that I've made, but basically



af

it's the same as wiring the
Arduino is should be the same



fbb

as wiring it in tinkercad. You
just need to make sure you use



acbc

the jump leads, the resistors
and the Ellie dies in the



addd

order and plug them to the
right pins in the Arduino.



d

So finally writing code,
uploading it to Arduino.



ce

First of all you will need
to make sure that you've



cfaed

downloaded Arduino above,
which you will need to go to



cdc

Arduino dot CC, go to
software downloads and



eacedd

download the latest version
of Arduino for whichever



ce

platform you're using.



-dd

And once you've done that, when
you open Arduino, you will get a



a

little sort of programming
window. It's an IDE, so it's A



b

kind of. It is an editor and.



cfb

You will get the same sort of
code as we saw in.



afe

In Tinker Cat because Tinker CAD
is emulating what we expect to



bbfcdb

see in the Arduino IDE here, so
we have the setup and the loop,



abfb

and we've got setting the PIN
modes and. So this is basically



-cea

a copy of exactly what we did
previously in Tinker CAD, and



faad

once you've written that, that
code in there are also a number



f

of other examples that you can
use inside Arduino to do a



dcfb

number of different things, and
you can download more libraries.



aeafad

Which we will look into at
a later date.





But what we need, what we're
going to do is, once you've



ed

written your code, you just the
one thing you need to check is



-bab

make sure that your USB cable is
plugged both into your Arduino



bfcdb

and into your computer via USB



ddea

port. Anne. And you will need to
check. Once you've done that,



-aabc

you'll know because the light
will come on the Arduino, but



fedf

you also need to check that your
port is connected. So I've got



da

my connecticon three. It could
be different depending on your



ececf

computer, but you need to make
sure that you have a port, so



eeab

you need to go to tools and
ports and you need to make sure



aff

that your board is Arduino Uno
or Genuino Uno. Or if you have a



-dad

different board at the moment
you all should have an Uno.



fce

If you click get board info it
will give you the outline of the



cebcae

board. The reason mine says
unknown is 'cause I've got a



-bfdb

kind of generic clone cheap
Chinese generic clone plugged



badea

in, but normally would say
genuino Uno. But it means that



-dfee

we've connected to a board at
any rate. So once you've done



dfbaf

that all you need to do is click
the upload button and it will



-ac

upload. And then it will have
uploaded when it's done



-adcdd

uploading and as you can see,



db

we. We now have.



ed

A working sketch. So this is
your first intro to using.



eeebbf

Arduino.


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI3MzU5NjQ3NSwtMTc3MzY3OTI4NSwtNT
MwMzY2NzE5LDE3NTI3NzAzNDEsMTczMzQ4ODc1MSwtMTkxNjY5
MTY2OCwtMTQzNjQ0NzgyMiwtMTE0MTE1Njg3MywxMDc0NTU1MD
csLTg2NjY5MzgwMCwtODM0NTc2MTgwLDgwNTc2NDYyMCwtMTQ4
OTI5NDA3NSwzOTM3MTY5MjksLTc5MTU3ODEzNSwtNjcwMzA4OD
gwLDEyMjY0ODA1MzQsMjEwMDM5MTUwMSwyMDEwNTAyNjEwXX0=

-->