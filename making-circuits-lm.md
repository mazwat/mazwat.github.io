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

Tinkercad is a way to simulate electrical circuits, but also to simulate circuits and components with Arduino and other microcontrollers. 

![Simple Circuit](images/tc-simple.png)
*fig 1. - Other Microcontrollers*

https://www.tinkercad.com/things/aefmW5mPE86-cool-hillar/editel?sharecode=bjxDkcj1jYkU3qDBDux5XN-GflpCaIIjGHqfXsWVICQ

https://www.tinkercad.com/things/j2mHkxwsdeL-basic-circuit/editel?sharecode=lUW-e_VPCYdwvUkmJTQy4I5D_la_LC-eEi7h7Q3y9gE




ecced

And you can see that what we
have here is a the interface of



aad

Tinker CAD and we're going to go
to the circuit section and we're



ddccc

going to create a new circuit.



dfa

What tinkercad is very good at



aafd

is simulating. The
environment of Arduino so





that we can build some base
we can put together basic



ff

components and we can test it
through a simulation of the



dcde

Arduino environment. We can
also write code in order to



ec

demonstrate it. However, is
very important that you



fc

actually use your own Arduino
and you use the Arduino.





IDE in conjunction with the
Relecq USB connection to your



f

Arduino. This is just a way to
test the process before you



d

implement it for real.



effc

So what we're going to do is
we're going to make a very



e

simple circuit, so if we think
about the basic circuit, we need



a

a source of power. So in this
case we're going to use a simple



fc

coin battery that we've taken
here.  Volt coin bit battery,



accab

and we're going to have a light
and LED, and basically all we



fbbee

need to do is why are the two?



ebbbf

Together now this is the plus,
so this is the positive going to



fdbeeccb

the Ellie D and we know that. So
you can see here in the Ellie D



-bcbe

The in the positive on an alley
on Eli D. The problem positive



efbccb

problem on Eli D is the longest
one or as demonstrated here.



dbdaa

With this slightly kind of with
a bit of a kink in it. This is



cc

the positive terminal for the
Ellie D so.



-dbcc

Because this is positive, just
to make things clear, we're



cdfa

going to make this red. And then
what we're going to do is draw



effdd

take another wire so these are
the equivalent of jumper leads



dfd

or wires if you like between the
different elements. OK, so there



d

we are. We've wired up our
battery, so this is like a



edc

simple circuit that we saw
earlier on where we've got our



-fca

source of power. And then we've
got the load that we want to



dbaad

drive, which is this lead.



abebbfdef

So if I start the simulation,
you can see that it immediately



fbc

comes on and we've got lights
coming out of RLED. However, you



dbf

can see that there is a question
mark and that is becausw. We are



-ece

putting too much power through
the Ellie D and it needs to be



cacab

controlled. It needs to be. It
needs to be managed and it's



accaf

being managed through the
resistor. So we need to add a



d-

resistor to our circuit.



ce

Now in order to workout.



ffc

Our resistor we need to workout
the resistance value and that is



dffadc

done by resistance calculation
is R = V, S minus VLE D /



debdba

I LED. This is where V is the
source voltage measured in volts



-cadad

where VLD is. The voltage drop
across the LD measured in volts



acc

and ILD is the current through
the energy measured in amps.



cfa

And finally, our is the
resistance measured in ohms,



fe

so this is a variation of
ohms law, but applied



adfef

specifically to Ellie D's.



bda

So we can use a Calculator.



dbbab

This example here is a
Calculator which will calculate



-feb

the resistance that we need. The
type of resistor that we need to



-dfbf

use. So what we need to do is
first of all we need to workout



-ffb

what our supply voltages so we
know that we are using a  Volt



cbfcbf

coin battery so our supply
voltage is  volts. Now the



eaed

standard load on an Eli D for an
LED current is about  million.



fcbff

Milli amps is quite standard.
The great thing with this this



bdb

Calculator is it actually tells
you the different colors and you



fe

get different value.



eefbad

And this is what's known as
the voltage drop.



adf

Or the direct voltage. So this
is what will be. This is the



cb

valves that's being drawn by the
the validian so that this is



bbdc

being taken away in the equation
that you saw earlier on, we've



-aeeecf

got one LED and then we can
calculate and you can put it to



-ade

with the percentage of accuracy.
So the type of resistor that we



-eded

want is either the higher is a
 or , so that means we need



cfae

to. So let's go with the higher
one and let's say it's .



-afccd

At the symbol here.  homes.



befdb

Resistor, so if we now go back
to here and we select a resistor



aaafce

from the top.



-adc

And we're going to put the
resistor between.



d

Let's turn that resist around.



afdba

The resistor between.



dbe

And we'll make this red as well,
just so that we are showing the



-cdc

positive side of our circuit.



becce

And. We established that it was
going to be .



cad

I believe that was  ohms, so
we don't want Killer owns. We



db

just want ohms. We say .



ef

Now you may have in your
Arduino kit. You won't



adcafa

necessarily have the exact
resistor, but you just want to



adea

round up to the closest
resistor in your pack when you



dbd

actually physically wire in
this together.



ab

So then if we start the
simulation, we've now got the



bf

light coming on, but there's no.
There's no sort of exclamation



fff

mark which is, so there's no
warning. We're not. We're not



dfcf

over powering the LED 'cause you
can burn leads out if you have



ab

don't have the correct resistor
in the circuit is a nice simple



eaabb

circuit. It's working. We've got
the power flowing through the



dee

from the battery through the
resistor  already.



-cedfaff

Which is providing the load
and then the circuit is is



b

finished by sending to the
negative terminal from the



fcfcfd

negative pin of the Ellie D.
Just to finish this off,



aceba

we're going to put a switch
in there, so we're going to.



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
eyJoaXN0b3J5IjpbLTkyNDYwMTUyOSwyMTAwMzkxNTAxLDIwMT
A1MDI2MTBdfQ==
-->