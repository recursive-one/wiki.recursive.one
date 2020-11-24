---
title: Astynax's setup (OS, apps, etc)
...

## OS

For many years the [/Linux]() is my main OS. On physical machines, I prefer the [Ubuntu Linux](https://ubuntu.com/) because "it just works". And I'm pretty happy with it. Yes, sometimes I am adding some PPA's or Snap packages, but I'm ready to pay this price.

## Desktop Environment

Just the [XFCE](https://xfce.org/) with the [/i3]() as a Window Manager. Most of the interactions with the OS I am doing with on-screen menus those I made myself with [/Rofi]() and some [/Python]()-scripting (with my own [pyrofi](https://github.com/astynax/pyrofi) library). This setup is equally good for small laptop screens as for multi-display configurations.

## Developer's Tools

I use [/asdf]() to manage the languages I write in. It is just a time-saver: I don't need to remember how to use each of the version managers, how to update the stuff. 

I use [/Docker]() from time to time, but I prefer to not mix it with any orchestration tools, even with docker-compose: [/GNU Make]() is just enough to me for now. 

Also, I started a migration to the [/Nix (package manager)]() and now I use it to install [/Rofi](), `rq`/`ripgrep`/`bat`/.. (see [/Rust powered tools]()). It is pretty neat to be able to describe an entire package configuration with a single file!

## Programming Languages

[/Haskell](), [/Rust](), [/Elm](), [/Clojure](), [/Racket](), [/Python](). Most of them I have installed with [/asdf]() or its own version managers.

## The one editor

I love the GNU [/Emacs](). I'm not using it as OS (yet?), but Emacs is my IDE, note-taking app, GTD app (I'm not so into GTD, actually). An entire editor's ecosystem I did configure myself without [Spacemacs](https://spacemacs.org/), [DooM Emacs](https://github.com/hlissner/doom-emacs), or any other "build".

Actually, I am using [/Vim]() for quick and casual editing when I am working in the terminal. But I'm trying to switch to Emacs for such activities too... 
