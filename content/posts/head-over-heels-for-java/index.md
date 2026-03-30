---
title: "Head Over Heels For Java"
description: "I have discovered the wonders of Java"
tags:
  - java
series:
  - languages
date: "2022-12-09"
publishDate: "2022-12-09"
---

In the past month I have discovered the wonders of Java. After months of teetering on the edge I finally decided to dive
right in. That is a choice that I will forever hold in high esteem.

## Why I like Java

### Write Once Run Anywhere

I know it's been said a thousand times but it really is amazing. From the perspective of a dev that has mainly been
developing in languages such as C, Rust, and Go it is nice to avoid the pain of compiling for every platform.

### Language Design

I like the syntax. Works well and makes sense to me. It just really resonates with me.

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

While initially it seems obscure. Once you get past the initial nightmare it is actually quite nice.

### OOP

Now I will admit. I had no clue what OOP was or why I would enjoy it. I kind of got a slight grasp when I learned C# but
it kind of escaped my mind. Now in Java I was forced to figure out what it meant. Now that I am using it and understand
the concepts I have an appreciation for it.

### Tooling

#### Editor

With the help of IntelliJ IDEA the code practically writes itself. While this is not necessarily a feature of the
language itself, it sure is nice.

#### Build Tools & Dependencies

Centralized dependency management is a hell of a drug. With Maven Central and Gradle, configuring a project and getting
dependencies is a breeze. After using CMake, this is a breath of fresh air.

## Pain Points

### Build Speed

Gradle can be a bit slow to compile. Especially on a machine with a lower core count. It is especially noticeable when
you develop on GitHub Codespaces often.

### General Finickiness

When not developing in IDEA I feel like gradle builds don't end up working like half of the time. Plus just dealing with
the project is a lot more of a task.

### I like Vim and Emacs

I really enjoy terminal based editors. While I technically could develop with Java in them. It would be more trouble
that it is worth.

## So why don't I just use Kotlin?
I actually use Kotlin here and there. I just prefer the Java approach to things. Furthermore, Kotlin is not entirely mature in my opinion and it tends to have breaking changes way too often for my liking. Plus, while it is interoperable with Java, older libraries to not always end up integrating the best. Writing Gradle configurations in Kotlin is a mile ahead of Groovy though, so it can have that.

## Closing
I love Java. I imagine that was clear from my writing. I look forward to learning all that I can about it and using it to build some fun stuff in the coming months.
