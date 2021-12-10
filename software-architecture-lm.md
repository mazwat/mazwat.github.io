---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: COMP140 - Lecture Materials 3

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: OOP
        url: '../oop-lm'
    next:
        content: UML
        url: '../uml-lm'
---

# Software Architecture

## So what is Software Architecture

A way of establishing **patterns** for the development of software.  These architectural patterns are a description of the **relationship** types and **elements** as well as the **constraints** or **limitations** in the system being built. Patterns are usually **reusable solutions** to common problems.

Ralph Johnson a famous programmer and professor at the University of Illinois, who co-authored one the essential books on programming called *Design Patterns*. Design Patterns is something we are going to look at in a later lecture. He questions this idea of architecture, arguing that there was no objective way to define what was fundamental, or high level and consequently there was no formal notion of established structure implied by the word architecture and that a better way to describe this approach is the:

***‘shared understanding that the expert developers have of the system design’***
***The decisions you wish you could get right early in a project'***

Johnson also cryptically said this:
  
***“Architecture is about the important stuff. Whatever that is”***

### Networks of Dependency

As we write code and our projects scale the interconnecting parts can become confusing. We sometimes generate dead ends or unnecessary code that causes our applications to slow down or to become needlessly complex, this waste is known in programmer circles as - **cruft**! 

So having some basic principles to help to design the link between objects, classes and functions is incredibly useful. We want to limit the proliferation of cruft.

## SOLID

**SOLID** is basically 5 principles, which will help to create a good software architecture. You can see that all design patterns are based on these principles. SOLID is basically an acronym of the following:

-   **S** is single responsibility principle (SRP)
-   **O** stands for open closed principle (OCP)
-   **L** Liskov substitution principle (LSP)
-   **I** interface segregation principle (ISP)
-   **D** Dependency injection principle (DIP)

In this lecture we are going to focus on the first 3 and finally we are also going to look at Order of Execution as it links to how the SOLID principles work.

1.  **Single Responsibility Principle -** every class in a computer program should have responsibility over a single part of that program's functionality, which it should encapsulate.
2.  **Open Closed Principle -** software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.
3.  **Liskov’s Substitution Principle** - if poodle is a subtype of dog, then objects of type dog in a program may be replaced with objects of type poodle without altering any of the desirable properties of that program
4.  **Order of Execution /** **Game Loop -** The flow between processes in software and hardware.

You can see how features of OOP from the previous lecture form a major part of SOLID principles. Specifically objects encapsulation, classes and objects.

## Implementing SOLID

### Single Reponsibility Principle

**“…it is almost always incorrect to begin the decomposition of a system into modules on the basis of a flowchart. We propose instead that one begins with a list of difficult design decisions or design decisions which are likely to change. Each module is then designed to hide such a decision from the others.”**

David R Parnas -_ [_On the Criteria To Be Used in Decomposing Systems into Modules_](https://www.cs.umd.edu/class/spring2003/cmsc838p/Design/criteria.pdf)_. 1972

We can think of software much like a company and as most software is developed to serve business functions this is a perfect analogy. In the piece of code below the class ``Employee`` is serving methods for pay, archiving and reporting. In a company if the pay is not calculated properly the CEO of the company is responsible for it’s impact on the business, if the information is not saved then the CTO or Chief Technical Officer is responsible for failing to save records correctly. If the hours are not reported correctly then CFO the chief financial officer id responsible, as money is mis-spent.
```c#
public  class  Employee {
	public  Money  calculatePay();
	public  void  save();
	public  String  reportHours();
}
```
We can apply this same principle to a game example:
```c#
public  class  Game {
	public  Health  calculateHealth();
	public  void  updateUI();
	public  String  reportDamage();
}
```
If we use **Unity**, this example shows a class that logs and prints to the console. It is perfect because it has one simple task, it is not trying to do anything beyond the scope of its name.
```c#
using  UnityEngine;
public  static  class  Logger
{
	public  static  void  PrintToConsole(object  content)
	{
	Debug.Log(content);
	}
}
```
#### Change Colour Script for an Icon
Lets explore this further in an example which is adapted from this medium article:
[https://medium.com/unity-hub/unity-solid-s-single-responsibility-6707d9569e73](https://medium.com/unity-hub/unity-solid-s-single-responsibility-6707d9569e73)

PIC HERE

Avove you can see there's a picture of an icon, which is a pixel art sort coin, and we're going to create a script which is going to change the color of this icon. So the basic example here is a public class called ``ChangeColorPropagateColor``,
and already this feels a bit weird. It's like it's trying to do too many things at once. We define the renderer and then we assign the renderer to the object and then we use the ``Update`` to track the ``Input.GetKeyDown`` to see if somebody presses the key in order to change the color, and then we use a random generator there using a random range to generate the colour. of the icon.

```c#
public  class  ChangeColorPropagateColor : MonoBehaviour
{
	public Color color;
	private  SpriteRenderer  _spriteRenderer;
	private  SpriteRenderer  _spriteRenderer1;
	private  void  Start()
	{
		_spriteRenderer1 = gameObject.GetComponent<SpriteRenderer>();
		_spriteRenderer = gameObject.GetComponent<SpriteRenderer>();

	}
	void Update()
	{
		if (Input.GetKeyDown(KeyCode.F))
		{
			_spriteRenderer.color = new  Color(Random.Range(0,1.0f), Random.Range(0, 1.0f),Random.Range(0, 1.0f),1);
			color = _spriteRenderer1.color;
			Debug.Log(color);
		}
	}
}
```
But there is a **better way** to do this.

We break this up into different classes and seperate *.cs* files, the first class is the ``ColorHandler`` and this is going to generate a random color. So we're essentially just separating this out. 

```c#
public  static  class  ColorHandler
{
	public  static  Color  GenRandColor()
	{
	return new Color(Random.Range(0, 1.0f), Random.Range(0, 1.0f), Random.Range(0, 1.0f), 1);
	}
}
```
Then we've got the ``CheckInput``. This is going to use ``KeyCode InvokeKey`` and this is going to be defined by an object which is connected to the actual icon itself, and so then it will detect the keypress based on a chosen property of whichever key is being pressed.
```c#
public  class  CheckInput : MonoBehaviour
{
	public KeyCode InvokingKey;
	public UnityEvent keyPressed;
	void Update()	
	{
	if (Input.GetKeyDown(InvokingKey))
		{
		keyPressed.Invoke();
		}
	}
}
```
And then finally, there's ``ColorChanger`` and this is basically calling the random colour from the previous example, and then it's going to apply that color to Whichever objects its attached to.
So if we look here, we've got

```c#
using  UnityEngine;

public  class  ColorChanger : MonoBehaviour
{
	public Color color;
	public  void  ChangeColor() {
		color = ColorHandler.GenRandColor();
		ApplyColor(color);
}

  

private  void  ApplyColor(Color  clr)

{

gameObject.GetComponent<SpriteRenderer>().color = clr;

}

}
```



the example. So if this was the.





If this is the icon image in the
as a game object in the game,





then we attach the two scripts,
the check input which will check





the which what is being pressed
and then the color changes to



ffadad

change it and you can define
what color you want to define it



bddca

too, and so then it's attached





to. D. The object in the game,
and the great thing about this



a

is this is totally reusable, so
we can change at any point you



efcac

can change what key is being
pressed. You can define it's





here. Or you can use or you can
define, change the color and you



f

can also duplicate this. You can
create more game objects. You



bcabcb

can reuse this and then you can
change different values for





different objects. In this case
then everything becomes modular



fadabdd

and it becomes very reusable.


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxODc4NzE4LDE1NTc0NTgzODUsLTE1Nz
U5NjU5NDgsNjE0OTk5Nzc3LDEwNDgwMDY0ODcsMjE5MTkwODI3
LC0xNDMyMzM1NDI4XX0=
-->