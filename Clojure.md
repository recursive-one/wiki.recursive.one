---
toc: no
...

[Clojure](https://clojure.org/) is language from the [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language)) family. The language itself is very opinionated: a lot of design decisions were made by its author [Rich Hickey](https://en.wikipedia.org/wiki/Rich_Hickey). That's why most of clojurians don't have to "built a language for the domain" as it often happens with users of other lisps.

Clojure has a rich (ha-ha, Rich) standard library and gives to its user an ability to write *high-concurrent code* with ease. This simplicity of the concurrency model is possible because of the [/FP]()-first nature of language.

Me [/who/astynax]() personally like to write some Clojure from time to time. It isn't statically typed but the design process itself is pretty fun because it is interactive: "the REPL-driven development" they say. You can even program a WebApp without any stops of the server, pure fun!

## Notable libraries

- [ring](https://github.com/ring-clojure/ring) - an abstraction of HTTP server, the foundation for any WebApp
- [compojure](https://github.com/weavejester/compojure) - a routing DSL for Ring
- [hiccup](https://github.com/weavejester/hiccup) - a DSL for HTML templating
- [Quil](http://quil.info/) - a library for creating interactive drawings and animations (based on Processing)

## Interesting projects

- [Dactyl Keyboard](https://github.com/adereth/dactyl-keyboard) - a parametrized split keyboard (Clojure program defines the 3D model)
- [Overtone](https://overtone.github.io/) - an audio environment for music live-coding (I saw pretty impressive stuff made with it!)
