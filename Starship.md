---
title: Starship prompt
categories: Linux bash
...

<img src="https://starship.rs/logo.svg" style="height: 64px" alt="Starship logo">

[Starship](https://starship.rs/) is a "cross-shell prompt" that can show in your shell a [/Git]() branch and status, a version of [/Python]() used in the project, the battery status, and many other "states" of the system.

Starship is one of the [/Rust powered tools]() we use daily (it just integrated into the shell!). It works pretty fast just because it doesn't show any "heavily obtainable" info during the navigation process and collects the stuff in the background on idle. This kind of asynchronicity is just not easily available in bash-powered prompts.