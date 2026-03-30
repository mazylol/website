---
title: "OOP Is Not Great"
description: "My opinion is that OOP is detrimental to programmers"
tags:
  - java
  - go
  - csharp
  - c
series:
  - languages
date: "2024-08-20"
publishDate: "2024-08-20"
---

After 5 years of programming I have come to the conclusion that usually OOP is not great. This may sound shocking considering that 2 out of 5 posts on this blog are me raving about C# and Java but I have been reformed.

## Background
For around a year I was infatuated with C# and Java. Initially I got introduced to Java through making discord bots with JDA. It was great. Up until that point I was used to making bots with Python or C. Java was and still is pretty nice for bot development and I really enjoyed my time with it. Then later on I discovered C# and enjoyed it even more. The syntax was great, it was fast, had a whole bunch of IDE support, and had a whole bunch of stuff going for it. I especially liked it when interfacing with MongoDB with their library. My only real gripe with it was the .NET ecosystem. Being an enjoyer of linux the Windows-centric parts of C# really bothered me and I eventually just sulked back to Java.

## Reckoning
One day I decided to try out Go. I kind of fell in love. The simplicity and power of go was amazing to me. It still gave me the data modeling powers that I liked from Java but in a simpler and much more barebones way. I had more of an idea what was going on with my code and had a far more efficient time programming.

Then later on I developed a love for Rust and C++ and now the rest is history. I have not touched a single line of Java or C# in quite a long time.

## But what is wrong with OOP?
### Code Readability
Sure, anybody with a grasp on any language will be able to understand what is going on, but some languages are just plain easier to reason about.


You cannot convince me that this...

```java
class Animal {
    String name;
    String sound;
    int noOfLegs;

    public Animal (){}

    public Animal (String name, String sound, int legs){
        this.name = name;
        this.sound = sound;
        this.noOfLegs = legs;
    }

    public void display() {
        System.out.println("My name is " + name);
        System.out.println("My sound is " + sound);
        System.out.println("My no. of legs is " + noOfLegs);
    }
}

class Dog extends Animal {
    String color;
    String breed;

    public Dog(String name, String sound ,int legs, String color, String breed){
        super(name,sound,legs);
        this.color = color;
        this.breed = breed;
    }

    public void display() {
        super.display();
        System.out.println("My color is " + color);
        System.out.println("My breed is " + breed);
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog1 = new Dog("Billy","Bark",4,"Brown","Labrador");

        billy.display();
    }
}
```
...is better than
```go
package main

import "fmt"

type Animal struct {
	name     string
	sound    string
	noOfLegs int
}

type Dog struct {
	Animal
	breed string
	color string
}

func NewDog(name, sound string, noOfLegs int, color, breed string) Dog {
	return Dog {
		Animal: Animal {
			name:     name,
			sound:    sound,
			noOfLegs: noOfLegs,
		},
		breed: breed,
		color: color,
	}
}

func (d Dog) Print() {
	fmt.Printf("My name is %s\n", d.name)
	fmt.Printf("My sound is %s\n", d.sound)
	fmt.Printf("My no. of legs is %d\n", d.noOfLegs)
	fmt.Printf("My color is %s\n", d.color)
	fmt.Printf("My breed is %s\n", d.breed)
}

func main() {
	billy := NewDog("Billy", "Bark", 4, "Brown", "Labrador")

	billy.Display()
}
```
...this

I enjoy brevity. And this is not it.

## What is it good for?
Minecraft mods. Even though Java is your only option, maybe kotlin, it works well for minecraft modding. It is quite nice.
