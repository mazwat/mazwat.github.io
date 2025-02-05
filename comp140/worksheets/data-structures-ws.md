---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: Worksheet 5
description: COMP140 - Worksheet 5

# Author box
author:
    title: Matt Watkins
    description: Lecturer in Computing at Falmouth University

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: UML
        url: '../uml-ws'
    next:
        content: Design Patterns
        url: '../design-patterns-ws'
---

# 6. Data Structures

## EXERCISE 1
### Collections
1. Fork the following **[repo](https://github.falmouth.ac.uk/Games-Academy/COMP140-DataStructures-Exercise)**
2. Open the **main** scene in Unity
3. Add at least 20 additional items to the collection
4. Display these to the screen

![Start point for Exercise 2](images/unity-sort.png)
*Screenshot of Collections Exercise - Start Point*

## EXERCISE 2
### Sorting
1. Write a default sort, so that the items are sorted by **name**
2. Sort the collection when the s key is pressed
3. Write another sort, to sort by **score**, trigger this with a key press
4. Write another sort, to sort by **age**, trigger this with a different key press

## EXERCISE 3
### Searching
5.  Investigate how to **search** for items in collections    
6.  Add code to search for **specific items** in the collections   
7.  Add **visual representation** to show that the search has completed, this could be a colour change or just displaying the found item elsewhere on the screen.

## STRETCH GOAL
### ICompare & IComparable

8. Using this **[data set](https://falmouthac-my.sharepoint.com/:x:/g/personal/matt_watkins_falmouth_ac_uk/EewqOswxQWhFrI3gRrhNR8cBoTOgn16HfE4bYFTWkTCl0g?e=FMdSYG)** which is in CSV format.
9. Develop a method to **parse** the data in the file using a **struct** into either **Unity** or a **VS Console App**.
10. If your using a Unity here's a clue for parsing the data. It reads all the contents of a file into a single string, splits that string into an array of records, take the first record and splits it on commas, and converts the first value in the split array to a string:
```c#
     var fileData : String  = System.IO.File.ReadAllText(path)
     var records : String[] = fileData.Split("\n"[0]);
     var recordData : String[] = (records[0].Trim()).Split(","[0]);
     var name : String;
     string.TryParse(recordData[0], name);
```
This may also help: [https://www.youtube.com/watch?v=xwnL4meq-j8](https://www.youtube.com/watch?v=xwnL4meq-j8)
11. Create a highscore table that sorts the data to only show the first **20 records** with the **highest scores**.
12.  Create a button or text input instruction to **remove** all players that are **not members** from the highscore table.
13. **Extra stretch** - Add a sort that shows the **20 most recent** high scores in the table.

You may find these articles useful. Find out more: **[https://dev.to/digionix/icomparable-vs-icomparer-274f](https://dev.to/digionix/icomparable-vs-icomparer-274f)**
**[https://unity3d.com/learn/tutorials/modules/intermediate/scripting/lists-and-dictionaries](https://unity3d.com/learn/tutorials/modules/intermediate/scripting/lists-and-dictionaries)**
{: .callout .callout--info}

## Tasks for the rest of the week
Consider your individual project and implement a data structure class in your code that processes
a feature of your game/experience. 

For example, you could use them to process:
- enemies
- score
- bullets
- resource management
- pick-ups

Please use at least one of these: **Lists, LinkedList, Stack, Queue** or **Dictionary**
Please bring your code to discuss with your programming tutor in your seminar group.



## VIDEO LECTURE

It is assumed that you have watched the video lecture before this workshop. If not you should find time to watch them during the week.
{: .callout .callout--warning}

### Lecture - Data Structures Part 1
<iframe width="100%" height="360" src="https://web.microsoftstream.com/embed/video/8f8786c7-82bb-4d21-a5d8-17c7088c0fcc?autoplay=false&showinfo=true" allowfullscreen style="border:none;"></iframe>

### Lecture - Data Structures Part 2
<iframe width="100%" height="360" src="https://web.microsoftstream.com/embed/video/620d8fc4-9ce0-41d9-83f0-35ee903040dc?autoplay=false&showinfo=true" allowfullscreen style="border:none;"></iframe>

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NDQ5NzQ5NTksLTExNzUwNjk5MDIsLT
kxNjUzOTM1OCwxOTEzNTExMTU1LC0xMDIzNDc4NjA1LC0xNTY2
OTcxNTQ5LC0yMDU5MDYxMzAzLDE2MDU3MjY5NTcsLTY3MTU0Nz
UxNCwtNDg3NzkyMjAwLDExNjA1MzU3MzYsLTMxMjM4NTQ4MCwt
MjI3NTgwMDksLTIyNzU4MDA5LC0xMDIzOTI2MDMwLC0xNDg0ND
UyNDQ2LDM2ODEwMzA1LDk1NTg5NTc0OCwtMTAxMzA2MzA3OV19

-->