---
toc: no
...

<img src="https://avatars3.githubusercontent.com/u/20698192?s=64&v=4" style="float: left; margin-right: 0.5em;">

[Elm](https://elm-lang.org/) is a small pure FP language I ([/who/astynax]()) use to build the Web stuff. It compiles to JavaScript so I don't need to write JS myself - such a relief!

Also, Elm is *self-contained*: it has its packaging system and compiler, no WebPack is needed. You are just writing a single file, call `elm make`, and getting the good old standalone HTML page!

The language itself has a builtin framework, The Elm Architecture, that is very easy to learn and use. "Batteries included", you know! There are many libraries to use in Web UIs. I even made [one](https://github.com/astynax/tea-combine/) by myself - is is wierd but pretty usable though.

# Ellie

One can try the language or play with libraries inside [Ellie](https://ellie-app.com) - a sort of Paste Bin + Online IDE.

# Elm powered stuff

Here some stuff I have built

- [Hekoish Watch](https://github.com/astynax/elm-hekoish-watch/) - a fullscreen watch (the cryptic one, actually). Live [demo](https://astynax.me/elm-hekoish-watch/),

# Notable libraries

- [mdgriffith/elm-ui](https://package.elm-lang.org/packages/mdgriffith/elm-ui/latest/) - a rich WebGUI "toolkit"
- [timjs/elm-collage](https://package.elm-lang.org/packages/timjs/elm-collage/latest/) - composable graphics library (I used it in my Hekoish Watch)
- [elm/file](https://package.elm-lang.org/packages/elm/file/latest/) makes possible to download or upload a file using the web browser, works with text and binary files
- [justgook/elm-image](https://package.elm-lang.org/packages/justgook/elm-image/latest/) is able to manipulate the raster images (`.png`!) and convert them to/from `BASE64` or just bytes