---
title: "C# is awesome"
description: "I have discovered the wonders of C# and I like it more than Java"
tags:
  - csharp
  - java
series:
  - languages
date: "2023-02-12"
publishDate: "2023-02-12"
---

Over the past few weeks I have discovered the greatness of C#. Initially I thought that is was just a Microsofty Java clone, and while that is somewhat true, there is a lot of stuff in C# that makes me a lot happier than Java.

## Tooling
The tooling for C# is superb. It makes Java look like a nightmare.

### Rider
Rider is a dream to code in. In my opinion it is much better than Visual Studio (especially since it is cross-platform). It is smooth and the memory profiling abilities are a bit better than what is available in IDEA. Riders helpful language features help me to feel more confident in writing code.

Plus, as of late I have been working with the OpenWeatherMap API. Being able to generate classes from a JSON file automatically is very helpful. Not to mention that making API calls is a bit easier than Java.

### Project Generation
Dealing with Gradle in Java is painful. There are so many ways to go about strucuring a build.gradle(.kts?) file that it just feels overwhelming. Here, everything feels much more standarized and it is a lot easier to reason about a project in general.

## Language Features
There is a lot to love here. It still has some boilerplace like Java but it is generally easier to reason about. I like the conciseness of the code and it feels like I have a harder time making it break in comparison to Java.

### Nuget / Dependencies
I like how everything is centralized. Plus, having the package manager built right into Rider is really nice. Dependencies are a main concern for the language, not an afterthought like Java.

## Gripes
Take this with a grain of salt, I am still learning and that takes time. It is still kind of hard for me to understand .sln and .csproj files. Like currently in my WeatherCord project for example. It is kind of jankily hacked together, but I wanted to have my dependencies shared across projects so I could just manage them in one place. I have been trying to do that but it is confusing. I know it is possible, I just don't now *how* it is possible. Also the syntax for the files is like visual basic. VB makes me cry blood.
