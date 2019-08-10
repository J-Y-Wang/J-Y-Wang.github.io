---
title: 'Quick Notes for Java'
date: 2019-04-18
permalink: /posts/2019/04/blog-post-3/
tags:
  - Java
  - Computer Science
  - Code Farmer
---

##Part One: [w3schools Java tutorial](https://www.w3schools.com/java)

*This part is only for quick grammar notes, but does not explain concepts and definition very clearly.*

At the beginning of learning Java, in comparison with C++ and Fortran, here are some quick notes.

C++ is part C and part Object Oriented, but Java is more Object Oriented from the very beginning, let's see.

Java use `class` and default main sentence `public static void main(String[] args)` rather than the `#include` and `void main` in C++.

<del>The definition of variable is slightly different, must using `int number=100` where in C++ and Fortran, there is no requirement for initial value.</del> This works only for local variables.

Java array looks a little bit more flexible compare to the scientific array in Fortran.

A `method` in Java is like a `suroutine` in Fortran or a `function` in C++.

Well, big head come with the Java Class.

`final` as a modifier like `constant` in Fortran.

##Part Two: "Head First Java", by Kathy Sierra & Bert Bates

Starting from "Head First Java"

Really straight forward start!

###Chapter 1: Breaking the Surface

Strict sturcture: class -> method -> statement

Compiling(like `javac`): xxx.java -> compiler -> xxx.class

Statement ends with `;` same to C++

boolean works different, `while(1){` will not work in Java

`system.out.println` means printing in a new line

generate random numbers: `int ran1=(int) (Math.random()*oneLength)`, and force to be int using `(int)`

###Chapter 2: A Trip to Objectville

An `Object` contains `instance variable` and `method`.

A class is a *blueprint* for an object.

real class versus tester class(also to start application).

>Now I feel a little bit about why Java and C++ are called OO language, while Fortran is not. Fortran is more of a procedure language, handling with scientific programs which are based on solid equations and rarely vary. However, OO are facing with real world application with blooming sepcifications or functions. It is unrealistic to imagine all data comes in traditional sturcture so that changing source codes for each instance will be crazy.
Maybe I will have better understanding, let's see.

public + static, equals to `global` in Fortran  
public + static + final, equals to `constant` in Fortran

###Chapter 3: Know Your Variables

Primitive types: `boolean`, `char`, `byte`, `short`, `int`, `long`, `float`, `double`

By indicating `type b=c` makes b and c refering to the same object, they are copies of each other with same contents. This might be tricky during program until one of them are assigned `null`.

Array is always object.

###Chapter 4: How Object Behave

The point to setters and getters is that you can change your mind later, without breaking anyone else's code.

Default initial values for instance variables:

|Type      |Value   |
|:--------:|:------:|
|integer   |0       |
|float     |0.0     |
|boolean   |false   |
|reference |null    |

However, local variables does not have default initial values.

###Chapter 5: Extra-Strength Methods

Prep code (pseudocode), test code (no run at this stage), real code  
try to adopt this procedure through a few examples.

|Pseudo	|Targey	|
|:-------:|:-------:|
|Declear	|Variable	|
|Make		|Instance	|
|Compute	|Number	|
|Invoke	|Method	|
|Get		|Input/Method	|
|Set		|Method	|

Converting a string to an int `Integer.parseInt(yourString)`

###Chapter 6: Using the Java Library

Optimize the game using ArrayList (API class)


##**To be continued**


###Chapter 7: Better Living in Objectville

###Chapter 8: Serious Polymorphism

###Chapter 9: Life and Death of an Object

###Chapter 10: Numbers Matter

###Chapter 11: Risky Behavior

###Chapter 12: A Very Graphic Story

###Chapter 13: Work on Your Swing

###Chapter 14: Saving Objects

###Chapter 15: Make a Connection

###Chapter 16: Data Structures

###Chapter 17: Release Your Code

###Chapter 18: Distributed Computing
