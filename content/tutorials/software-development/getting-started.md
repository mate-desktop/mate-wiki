---
title: Getting Started
weight: -20
---

This page tells you how to get started with software development for the MATE Desktop Environment.

<!--more-->

{{< toc >}}

## Prerequisites

To be able to really help developing the MATE Desktop, you should know the basics of programming. But do not worry if you are not a Linus Torvalds yet. Your motivation, patience and willingness to learn usually are sufficient to get started with software development in a few month, even if you have never programmed before.

Most of the MATE Desktop is written in C. Although C is a [procedural language](https://en.wikipedia.org/wiki/Procedural_programming), some [object-orientated](https://en.wikipedia.org/wiki/Object-oriented_programming) features (like constructors and polymorphism) can be accessed through the GTK+ library. The MATE System Monitor is written in C++. Some plugins and the Menu Editor Mozo is written in Python.

So if you know any of this language, you can [skip](#getting-used-to-gtk) the next paragraph. Otherwise, keep reading.

## Learn Programming

If you are new to programming the important thing to do is to practice. Even if you think that you understand everything from the tutorials, you should still do some exercises to check if you really understood what you were reading.

As most of the MATE Desktop is written in C it makes sense to start with that language, otherwise C++ and Python are fine too. There are a lot of great free resources out there:

- Printed Books
  - "The C Programming Language" by Brian Kernighan and Dennis Ritchie

- Online
  - https://en.m.wikibooks.org/wiki/C_Programming (C Programming)
  - https://en.m.wikibooks.org/wiki/C%2B%2B_Programming (C++ Programming)
  - https://en.m.wikibooks.org/wiki/Python_Programming (Python Programming)

So I recommend that you take a look at one of these books or online tutorials, learn how to write some simple programs and how to compile and execute them. After that, you can continue reading.

## Getting used to GTK

If you now are able to write a hello world program, a Celsius to Fahrenheit converter or even a fully featured command line calculator, you will still look at most MATE programs without understanding what is going on. That is because MATE uses the GTK toolkit which is responsible for the whole graphical part of the application and even for a little bit more.

<!--TODO-->

  - https://developer.gnome.org/gtk3/3.24/ (GTK Reference Manual)
  - https://prognotes.net/gtk-glade-c-programming/ (GTK Glade Programming)


