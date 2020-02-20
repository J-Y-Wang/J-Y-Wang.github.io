---
title: 'Quick Notes for Java'
date: 2019-04-18
permalink: /posts/2019/04/blog-post-3/
tags:
  - Java
  - Computer Science
  - Code Farmer
categories:
  - English
---

## Part One: 

**[w3schools Java tutorial](https://www.w3schools.com/java)**

*This part is only for quick grammar notes, but does not explain concepts and definition very clearly.*

At the beginning of learning Java, in comparison with C++ and Fortran, here are some quick notes.

C++ is part C and part Object Oriented, but Java is more Object Oriented from the very beginning, let's see.

Java use `class` and default main sentence `public static void main(String[] args)` rather than the `#include` and `void main` in C++.

<del>The definition of variable is slightly different, must using `int number=100` where in C++ and Fortran, there is no requirement for initial value.</del> This works only for local variables.

Java array looks a little bit more flexible compare to the scientific array in Fortran.

A `method` in Java is like a `suroutine` in Fortran or a `function` in C++.

Well, big head come with the Java Class.

`final` as a modifier like `constant` in Fortran.

## Part Two: 

**"Head First Java", by Kathy Sierra & Bert Bates**

Starting from "Head First Java"

Really straight forward start!

### Chapter 1: Breaking the Surface

Strict sturcture: class -> method -> statement

Compiling(like `javac`): xxx.java -> compiler -> xxx.class

Statement ends with `;` same to C++

boolean works different, `while(1){` will not work in Java

`system.out.println` means printing in a new line

generate random numbers: `int ran1=(int) (Math.random()*oneLength)`, and force to be int using `(int)`

### Chapter 2: A Trip to Objectville

An `Object` contains `instance variable` and `method`.

A class is a *blueprint* for an object.

real class versus tester class(also to start application).

>Now I feel a little bit about why Java and C++ are called OO language, while Fortran is not. Fortran is more of a procedure language, handling with scientific programs which are based on solid equations and rarely vary. However, OO are facing with real world application with blooming sepcifications or functions. It is unrealistic to imagine all data comes in traditional sturcture so that changing source codes for each instance will be crazy.
Maybe I will have better understanding, let's see.

public + static, equals to `global` in Fortran  
public + static + final, equals to `constant` in Fortran

### Chapter 3: Know Your Variables

Primitive types: `boolean`, `char`, `byte`, `short`, `int`, `long`, `float`, `double`

By indicating `type b=c` makes b and c refering to the same object, they are copies of each other with same contents. This might be tricky during program until one of them are assigned `null`.

Array is always object.

### Chapter 4: How Object Behave

The point to setters and getters is that you can change your mind later, without breaking anyone else's code.

Default initial values for instance variables:

|Type      |Value   |
|:--------:|:------:|
|integer   |0       |
|float     |0.0     |
|boolean   |false   |
|reference |null    |

However, local variables does not have default initial values.

### Chapter 5: Extra-Strength Methods

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

### Chapter 6: Using the Java Library

Optimize the game using ArrayList (API class)

`ArrayList` never needs to know how big it should be. It looks very similar to the pointer concept in C++.

Find API in "Java in a nutshell-A desktop quick refernce" or HTML.API docs.

### Chapter 7: Better Living in Objectville

Inheritance and polymorphism

`superclass` versus `subclass`, what if the subclass is only partial inheritate from the superclass? It's override!

Use inheritance to avoid duplicating codes in subclasses.

The lowest method on the inheritance tree is called first.

Use IS-A test for any inheritance relationships.

But what if the `superclass` is modified, it might affect a bunch of subclass but not all the subclass want to be modified I guess? Only applicable in cases where IS-A test is passed?

Use `final` modifier to prevent from being overridden.

### Chapter 8: Serious Polymorphism

`abstract class`, useful only when extended, with no method body but declaration.

`interface` (including abstract methods only) allows classes in different inheritance trees to implement a common thing. Multiple inheritance is not allowed due to "Deadly Diamond of Death".

A `class` only extent one `class` but implement multiple `interface`.

`super` allows to use superclass method, despite the subclass overridden.

Class `Object` is a more universal but vague concept.

Well, `interface` looks like a "Table of Content", it tells you what methods are in the subclasses, but don't explain it. You have to open the book and define by yourself. The benefit is that it will always remind you of what you should write about and where.

### Chapter 9: Life and Death of an Object

`instance variable` lives within the object they belong to, on the *Heap*.

`method` lives in *stack* with current `method` on the top of it.

Use `constructor` to initialize important state and keep identical name to class with no return type.

`overload` when there is more than one `constructor`, but they must have different argument list.

`super()` calls the superclass constructor, which must finish before its subclass constructor.

Superclass constructors with arguments are used to send information from subclass to superclass, expecially for `private` instance variables.

***`this` used for overloaded constructor from another?***

`null` means deprogramming the 'remote control' to somethings.

### Chapter 10: Numbers Matter

`static` lets a method run without any instance of the class, therefore no object (on the heap) in this case, e.g. Math.xxx(). It should be called using the class name rather than an object refrence variable.

But a static method can access a static variable.

Static variables are shared and initialized (or default value) before any object of that class can be created.

Constant variable names should all be in caps!

What `final` mean to different things:

|Things	|You can't	|
|:-------:|:-------:	|
|Variable	|Change value	|
|Method	|Override		|
|Class		|Extend		|

`import static` will make the code confusing to read, so I guess it's better to avoid it and most editors have the auto-completion function.

Number and date formatting...

## Feb 21

### Chapter 11: Risky Behavior
40p

### Chapter 12: A Very Graphic Story
40p

## Feb 22

### Chapter 13: Work on Your Swing
30p


### Chapter 14: Saving Objects
40p

## Feb 23

### Chapter 15: Make a Connection
60p

## Feb 24

### Chapter 16: Data Structures
50p

## Feb 25

### Chapter 17: Release Your Code
20p

### Chapter 18: Distributed Computing
40p
