# An idea

**PixCell** is the common name for a couple of software pieces I made. Each piece implements a simple [Pixel Art](https://en.wikipedia.org/wiki/Pixel_art) editor. The overall simplicity of the core concept makes this app a good exercise or a "weekend project".

Common features:

- 16x16 pixels
- 16 colors
- simple image transformations like "flip" and "rotate"
- different palettes

# PixCell/Clj

[This version](https://pixcell-cls.recursive.one) is implemented in [/Clojure]() and keeps all the state in the URL. It is a [proof of concept](https://en.wikipedia.org/wiki/Proof_of_concept): I just wanted to build a "thin" WebApp as a server-generated page and have no state on the server itself and also no implicit state in the cookies or other kinds of local storage. That's why the URL keeps all the app's state.

Features:

- No info is storing anywhere (except for browser history), no cookies, no local storage, no user profiles on the server-side.
- If you need to save your work you can just create a bookmark.
- Browser history works as Undo/Redo.

# PixCell/Elm

[This version](https://astynax.me/pixcell-elm/) works exclusively in your browser. You can save a standalone HTML page and use it offline!

File saving feature isn't implemented yet but I work on it :)