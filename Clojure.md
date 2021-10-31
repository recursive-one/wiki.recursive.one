---
toc: no
...

<img src="https://clojure.org/images/clojure-logo-120b.png" style="float: left; margin-right: 0.5em; width: 64px; height: 64px" alt="The Clojure logo">

[Clojure](https://clojure.org/) is language from the [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language)) family. The language itself is very opinionated: a lot of design decisions were made by its author [Rich Hickey](https://en.wikipedia.org/wiki/Rich_Hickey). That's why most of the clojurians don't have to "built a language for the domain" as it often happens with users of other lisps.

Clojure has a rich (ha-ha, Rich) standard library and gives its user an ability to write *high-concurrent code* with ease. This simplicity of the concurrency model is possible because of the [/FP]()-first nature of language.

Me [/who/astynax]() personally like to write some Clojure from time to time. It isn't statically typed but the design process itself is pretty fun because it is interactive: "the [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)-driven development" they say. You can even program a WebApp without any stops of the server, pure fun!

One can even write a shell-script in Clojure with [babashka](https://github.com/borkdude/babashka) or just use `bb` as a chunk of big pipe:

```bash
$ ls | bb -i '(take 2 *input*)'
("CHANGES.md" "LICENSE")
```

# Tools to start quickly

- [Leiningen](https://leiningen.org/), a popular all-in-one tool for project scaffolding, test running, dependency management
- [nREPL](https://nrepl.org/), a "network REPL" (just keep in mind: Leiningen uses it implicitly)
- [sublime-clojure](https://github.com/tonsky/sublime-clojure), the "Clojure support for [Sublime Text](http://www.sublimetext.com/) 4"

# Notable libraries

- [ring](https://github.com/ring-clojure/ring), an abstraction of the HTTP server, the foundation for any WebApp
- [compojure](https://github.com/weavejester/compojure), a routing DSL for Ring
- [hiccup](https://github.com/weavejester/hiccup), a DSL for HTML templating
- [Quil](http://quil.info/), a library for creating interactive drawings and animations (based on Processing)
- [dali](https://github.com/stathissideris/dali), a hiccup-like DSL for creating the SVG graphics (also, dali can render SVG as PNG)
- [aleph](https://aleph.io/) ([GitHub](https://github.com/clj-commons/aleph)), a library for client and server network programming with "stream" abstraction

# Interesting projects

- [Dactyl Keyboard](https://github.com/adereth/dactyl-keyboard), a parametrized split keyboard (Clojure program defines the 3D model)
- [Overtone](https://overtone.github.io/), an audio environment for music live-coding (I saw pretty impressive stuff made with it!)
- [/asciinema](), a screen capture tool for your terminal
- [/babashka](), a native, fast starting Clojure interpreter for scripting

# My projects

- [/PixCell]() (a Clojure implementation of it) - a simple Pixel Art editor