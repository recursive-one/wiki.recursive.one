# Language itself

<img src="https://racket-lang.org/img/racket-logo.svg" style="float: left; margin-right: 0.5em; width: 64px; height: 64px" alt="The Racket logo">

[Racket](https://racket-lang.org/) is a dialect of [Scheme](https://en.wikipedia.org/wiki/Scheme_(programming_language)), which is a member of [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language)) family. The language is dynamically typed, multiparadigm, [/FP]() capable. Racket has an interactive REPL, a cross-platform compiler, even its own IDE, [Dr.Racket](https://docs.racket-lang.org/drracket/index.html).

For now, the Racket team is [migrating](https://notamonadtutorial.com/rebuilding-the-racket-compiler-with-chez-scheme-210e23a69484) the language's core to the [Chez Scheme](https://www.scheme.com/) so Racket will be pretty fast someday!

# Language-Oriented Programming

The core idea behind the language is "Language-Oriented Programming": you are designing and implementing the domain-specific languages just for every domain you work with! Here is a great talk about LOP: ["Lambda World 2019 - Language-Oriented Programming with Racket"](https://www.youtube.com/watch?v=z8Pz4bJV3Tk)".

Also, there is a book ["Beautiful Racket"](https://beautifulracket.com/) just about the LOP.

# Batteries included

The Racket as a platform has a nice set of "batteries". For example, a really great set of libraries to work with graphics/animations/games. Here is a talk about this aspect: ["big-bang: the world, universe, and network in the programming language"](https://www.youtube.com/watch?v=ayoofXuKqMY). I have played with this stuff myself: made some pieces of *generative art*. You can take a look at them [here](https://astynax.neocities.org/daily-art/).

Another thing in Racket world I played with is [/Pollen](): my [recursive.one](https://recursive.one) site was made using it.

# Resources

- ["Deploying Racket Web Apps"](https://defn.io/2020/06/28/racket-deployment/), a quick intro to `raco distribute` and to resource file handling
- ["The Missing Guide to Racket's Web Server"](https://defn.io/2020/02/12/racket-web-server-guide/) + ["Continuations in Racket's Web Server"](https://defn.io/2020/05/11/racket-web-server-internals/)

# Ecosystem

- [RackSnaps](https://racksnaps.defn.io/) (an [announcement](https://defn.io/2020/05/03/ann-racksnaps/)), the simple way to lock all the packages (yep, the raco does not do that)