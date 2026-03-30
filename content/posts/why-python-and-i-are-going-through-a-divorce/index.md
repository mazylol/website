---
title: "Why Python and I are going though a divorce"
description: "Python has become increasingly frustrating and it is time to make a change."
tags:
  - python
  - c
  - rust
series:
  - languages
date: "2022-10-05"
publishDate: "2022-10-05"
---

I, like many other programmers, wrote my first Hello world in Python. For a good while I was having a blast. Python is what brought me into this world and I have to give it some commendation for that. However, over time, I have drifted away from Python. Here's why.

## Simplicity
Syntactically, Python is very simple. This is a great thing for new programmers...or is it? While being easy to understand is important Python's strangeness makes understanding other languages a bit more difficult. It is almost like Python gives you training wheels, but never let's you take a leap of faith and gain the full power of riding two wheeled. For example Python's Dynamic Typing got me accustomed to making variables with little to no thought. Then when I tried languages like Rust and C I was very confused by the idea of static typing.

## Speed
Python is an interpreted language. What does this mean? An interpreter reads code line by line. It translates your human understandable code to stuff that a computer can actually do something with. Notice how I said line by line. The Python interpreter executes code one line at a time. Consider this example. Here I have Python code that will solve the tower of hanoi. It does it, cool. Now let's compare it to the exact same problem, but solved using C. The C version was over two times faster! Let's look at this another way. Say we are trying to do c = a + b. In C, under the hood it would be loading the integer from location a, then again for location b. It would do the addition and store the value into location C. Meanwhile in Python it would have to load the object from location a, then from location b. Find the add method in object a, perform type checks and do the proper type casting for object b. Throw an exception if b does not have an appropriate representation. Extract the integer value from object a, then again for object b. Do the addition, allocate new memory, wrap the value in a new object. So basically Python issues a few hundred CPU commands for C's 4.

## Errors
Due to the dynamic typing of Python, many errors only show up at runtime. This is inefficient and annoying. Even more annoying is the content of the errors themself. Python errors are very hard to decipher. They are complex and do not do a good job of telling you what is wrong. This is the reason that I like Rust so much. Rust errors are very, very easy to understand, plus a lot of the time the compiler will almost tell you what you need to do to fix it.

## Package Management
Installing a Python package with PIP can be a real nightmare. For example, you try to install a package and you get `permission denied`, you try to install it with sudo and it messes with the environment variables on your system. Plus I always find that PIP has errors that are a hassle to reconcile when all I want to do is whip up the odd script.

## Readability
This is probably the biggest thing that makes Python a nightmare for me. The code is basically spaghetti. Who thought that tabs instead of curly braces is a good idea? Having functionality be determined by code formatting is preposterous. It makes seeing where functions end and where if statements begin.

## Summary
In the end Python will always have a place rooted in my heart for being the language that got my foot in the door to programming. But now that I have matured and discovered better tools I will not be using it for anything other than quick scripting.
