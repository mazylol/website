---
title: "C, A Return To Monkey "
description: "C is amazing and I have come back to it after all this time"
tags:
  - c
  - c++
series:
  - languages
date: "2024-12-25"
publishDate: "2023-12-25"
---

After a few years of avoiding C like the plague I have discovered a love for it. While I would be better served using a language like Go in most cases, C is just a lot more fun to me personally. Live, laugh, unsafe.

# Background

When I started programming a few years ago I began the journey with Python. After realizing that I hated it I decided to switch to C. Initially, I was having a great time making discord bots with the [Orca](https://github.com/cee-studio/orca), now [Concord](https://github.com/Cogamasters/concord), library. I was absolutely flying but eventually, I got skill issued. I just could not wrap my head around pointers and memory management. I ended up moving onto Java, Go, Rust, and Rust.

# A Change

Somewhat recently I started to play around with C++. I really enjoyed using the [D++](https://dpp.dev) discord library and made a few bots with it. I actually really enjoyed C++ for a while and honestly would not mind using it, the only thing that really annoyed me was the bloat. Templates are clunky and there are pieces of code that are just completely unintelligible. For example:

```cpp
// this is from a video by code_report
int calculate(int bottom, int top) {
    return top <= bottom ? 0 :
        ranges::accumulate(
            std::views::iota(bottom, top + 1) |
            std::views::filter([](auto e) { return e % 2 == 0; }), 0);
}
```

...what this hell is even that

# Off The Deep End

After becoming disillusioned with C++ I decided to check out C again. While it was a bit of a rocky start, I have come to love the language. While I am not as productive or safe as I would be in a modern language I feel that it is a neccessary tradeoff for my happiness. I am having fun in C. If I am not having fun, what is the point anyways? I have had fun writing data structures that I had previously taken for granted for other languages and have found this to be a very educational experience. My code is not perfect, at all. Debuggers and Valgrind are my best friends. But I am having a good time and plan to continue my C journey. void pointers are good enough, I don't need generics anyways. So far one of my favorite projects has been [multithreaded bogosort](https://github.com/mazylol/ultimate-bogo-c), because it is hilarious to me.
