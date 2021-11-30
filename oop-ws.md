---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Worksheet 1

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: Previous page
        url: '#'
    next:
        content: Next page
        url: '#'
---

# Object Oriented Programming

This workshop is divided into to 2 parts where we will explore the use of code in Visual Studio and Unity. Complete each task in your own time. We will review solutions at the halfway point.

## PART 1 - OOP in **Visual Studio**
### Exercise 1

![Add Console App](images/create-console.png)

Create a console app project in VISUAL STUDIO
1. Create a C# program that requests 5 names of ``Dog`` from the user and stores them in an array of objects of type ``Dog``. To do this, first create a dog class that has a name member variable of type ``string``.
2. Your input should be: ``Labrador, Poodle, Wolf, Fox, Pug.`` 
3. Your output should be: 

```
A pack of wild dogs emerged out of the wilderness. 
Amongst their number was:
A Labrador
A Poodle
A Wolf
A Fox
A Pug
```
You should use a loop to iterate through the array. Your Dog class needs a method to return the value of name. 
You should use ``console.ReadLine`` to input the value.
{: .callout .callout--info}

### Exercise 2

1. Expanding on the previous exercise. Create 2 new classes called Wild and Domestic. 
2. Once again use the loop to iterate output values.
3. Use inheritance to inherit the parent class filed name. Your should also have a new property called Behaviour which contains the behaviour of each class of dog. It should be both readable and writable.
4. Output should be something like this:

```
The Labrador wags its tail!
The Poodle Wags its tail!
and so on…
```
### Exercise 3

1. Create a class Smoothie and do the following:
2. Create a property called Ingredients.
3. Create a GetCost method which calculates the total cost of the ingredients used to make the smoothie.
5. Create a GetName method which gets the ingredients and puts them in alphabetical order into a nice descriptive sentence.
6. If there are multiple ingredients, add the word "Fusion" to the end but otherwise, add "Smoothie". 
7. Finally there should be a method called makeSmoothie that outputs the name, ingredients and costs of a smoothie based on inputted ingredients. 

Remember to change "-berries" to "-berry". See the examples below.
{: .callout .callout--info}

```
s1 = Smoothie(new string[] { "Banana" })
s1.Ingredients ➞ { "Banana" }
s1.GetCost() ➞ "£0.50"
s1.GetPrice() ➞ "£1.25"
s1.GetName() ➞ "Banana Smoothie"

s2 = Smoothie(new string[] { "Raspberries", "Strawberries", "Blueberries" })
s2.ingredients ➞ { "Raspberries", "Strawberries", "Blueberries" }
```