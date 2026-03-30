---
title: "How Rust Became My New Goto"
description: "I am making a blog"
tags:
  - rust
series:
  - languages
date: "2023-07-19"
publishDate: "2023-07-19"
---

Nowadays Rust is by far my preferred language for any new project. Whenever I have some sort of problem I instinctively run `cargo new [project]`. Here is why I enjoy it so much.

# Syntax
Syntactically Rust combines a lot of what I like all language paradigms. It has a perfect mix of OOP and Functional programming.

Here is a very simple way of defining a struct and then using impl to make instantiating a new book easier:
```rust
struct Book {
    title: String,
    author: String,
}

impl Book {
    fn new(title: &str, author: &str) -> Book {
        Book {
            title: String::from(title),
            author: String::from(author),
        }
    }
}

fn main() {
    let book = Book::new("1984", "George Orwell");

    println!("{} by {}", book.title, book.author);
}
```

What's not to love?

# The [Crate](https://crates.io) Ecosystem
The crates ecosystem is wide and pretty powerful. It eliminates the pain of dependencies that is present within C and C++ (looking at you CMake). Even nicer is that you can declare what features you want within the dependencies. This makes it easy to exclude stuff that you won't end up using, getting rid of bloat. This is all easily definable within Cargo.toml

Here's the file for my TwelveData wrapper:
```toml
[package]
name = "twelvedata"
version = "0.6.3"
description = "A Rust client for the Twelve Data API"
repository = "https://github.com/mazylol/twelvedata-rs"
readme = "../../README.md"
keywords = ["twelvedata", "api", "client", "rust"]
categories = ["api-bindings", "finance"]
documentation = "https://docs.rs/twelvedata"
authors = ["Landon Porter <mazy@cock.li>"]
license = "MIT"
edition = "2021"

[dependencies]
reqwest = { version = "0.11.18", features = ["json"] }
serde = { version = "1.0.163", features = ["derive"] }
tokio = { version = "1.28.2" }
```

As a bonus here's some crates that I use and like a whole lot:

- clap
- serde
- tokio
- yew
- leptos
- serenity / poise
- twitchchat
- tui / crossterm

# The Community
The Rust community is one of the best I've ever been a part of. Everyone is super helpful and friendly. I've never had a question go unanswered. The Rust Discord is a great place to get help and learn more about the language. The Rust subreddit is also a great place to learn more about the language and see what other people are doing with it.

# The Compiler
Even though the community is great your real best friend is the ... compiler? Unlike GCC the compiler actually helps you write code. When you have an error a lot of the time it will provide a solution. Then even when it does not have a direct solution it will point you in the right direction.

Here's a simple example:
```rust
fn square(x: &mut i32) {
    *x *= *x;
}

fn main() {
    let mut x = 5;

    square(x);

    println!("x = {}", x);
}
```

This code does not compile, but fear not! The compiler tells you how to fix it:
```
error[E0308]: mismatched types
 --> src/main.rs:8:12
  |
  |     square(x);
  |     ------ ^
  |     |      |
  |     |      expected `&mut i32`, found integer
  |     |      help: consider mutably borrowing here: `&mut x`
  |     arguments to this function are incorrect
  |
```

All we need to do is change `square(x);` to `square(&mut x);` and voila `x = 25`
