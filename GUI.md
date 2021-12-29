---
title: Graphical User Interfaces
categories: Haskell Python
...

## My experience

I ([/who/astynax]()) have spent a lot of time building various user interfaces:

- [/TUI]()s for the MS-DOS programs written in [QBasic](https://en.wikipedia.org/wiki/QBasic) and [Turbo Pascal](https://en.wikipedia.org/wiki/Turbo_Pascal)
- Graphical interfaces for Windows programs written in [Borland Delphi](https://en.wikipedia.org/wiki/Delphi_(software))
- Tcl/Tk-based GUIs and "Web GUIs" for Linux programs

Here I have written my experience in doing such stuff.

## Tck/Tk

I didn't use the [Tcl](https://en.wikipedia.org/wiki/Tcl) itself but I played a lot with its GUI toolkit, the [Tk](https://en.wikipedia.org/wiki/Tk_(software)). Usually it were the [Tkinter](https://docs.python.org/3/library/tkinter.html) for [/Python]() or [uni-htk](https://hackage.haskell.org/package/uni-htk) for [/Haskell](). Tk is pretty simple to use, lightweight, and "just works" on many platforms.

Here is a nice but opinionated article about Tkinter: ["How to setup correctly an application with Python and Tkinter"](https://medium.com/@mattia512maldini/how-to-setup-correctly-an-application-with-python-and-tkinter-107c6bc5a45)

Also, if you are a Pythonista take a look at [PySimpleGUI](https://github.com/PySimpleGUI/PySimpleGUI). It is a wrapper that helps to create Tk, Qt, and even the Web GUIs using a set of universal primitives. Code looks so script'ish for me. But it is quite Ok when you want to make a prototype ASAP.

## Web GUIs

Nowadays I prefer to use [/Elm](). Though I always have in my pocket the [Threepenny-GUI](https://wiki.haskell.org/Threepenny-gui) (a [/Haskell]() library) if I will need to do some heavy lifting :)

Usually, WebGUI implies [/CSS]() and under the link I keep a couple of good variants of it to use in my projects.

## Menus, dialogs

When I don't need a full-featured GUI and some simple menu-like interface is enough I use the [/Rofi]() with some Python scripting.

Sometimes I just need to show a simple confirmation window or a text entry. In such cases [/Zenity]() can be just good.

# Resources

## 7GUIs

Recently I found a nice set of tasks that are testing how your favorite GUI toolkit capable to do the real work. Here it is: ["7GUIs: A GUI Programming Benchmark"](https://eugenkiss.github.io/7guis/). My advice: just scroll through the list of tasks and look to the last ones! :)

## Interesting stuff to play with

- [zserge/lorca](https://github.com/zserge/lorca), "Build cross-platform modern desktop apps in Go + HTML5" ([/Golang]())
- [BeeWare](https://beeware.org/), "Write your apps in [/Python]() and release them on <...many platforms> using rich, native user interfaces."
- [Nuklear](https://github.com/Immediate-Mode-UI/Nuklear), "A single-header ANSI C immediate mode cross-platform GUI library" with [bindings](https://github.com/snuk182/nuklear-rust) for [/Rust]()
- [libui](https://github.com/andlabs/libui), "Simple and portable (but not inflexible) GUI library in C that uses the native GUI technologies of each platform it supports."
  - [bindings](https://github.com/msink/kotlin-libui) for [/Kotlin]()/Native.
  - [bindings](https://github.com/andlabs/ui) for [/Golang]()