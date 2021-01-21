---
toc: no
categories: Haskell
...

<img src="https://www.haskell.org/img/haskell-logo.svg" alt="The Haskell logo" style="height: 32px;">

[Haskell](https://www.haskell.org/) is a pure-[/FP]() language I ([/who/astynax]()) really like and use in my projects. I write Haskell in the [/Emacs]() or just use the REPL.

# How to get and use

I use [ghcup](https://www.haskell.org/ghcup/) to get the [GHC compiler](https://www.haskell.org/ghc/) itself, the [Haskell Language Server](https://github.com/haskell/haskell-language-server), the [Cabal](https://cabal.readthedocs.io) tool.

> Sometimes HLS wants you to do some preparation if you are planning to use it with your projects. Usually, all you need is `hie.yaml` containing this "`cradle: {cabal: {}}`". For more info go to docs for [hie-bios](https://github.com/mpickering/hie-bios#cabal).

In the past, I preferred the [Stack](https://docs.haskellstack.org) tool but nowadays I'm glad to use the Cabal. Someday, I may adopt the [/Nix (package manager)]() as a more predictable alternative/companion for Cabal.

# Notable packages

- [/Turtle (library)](), a shell scripting toolkit
- [Threepenny-GUI](https://wiki.haskell.org/Threepenny-gui), a Web [/GUI]() framework with the [FRP](https://en.wikipedia.org/wiki/Functional_reactive_programming) taste
- [Shake](https://shakebuild.com/), a declarative build system
- [propellor](https://propellor.branchable.com/), a configuration management system (does the same work that [/Ansible]() does)
- [Hakyll](https://jaspervdj.be/hakyll/), a static site generation framework
- [HsLua](https://hackage.haskell.org/package/hslua), binding to [/Lua]() language. [Here](https://hslua.github.io/santas-little-lua-scripts.html) is a good intro and [here](https://github.com/hslua/hslua-examples) are nice examples of usage.
- [QuickCheck](https://hackage.haskell.org/package/QuickCheck), the [famous](https://en.wikipedia.org/wiki/QuickCheck) property-based testing framework ([good intro](https://jesper.sikanda.be/posts/quickcheck-intro.html) to)
- [brick](https://hackage.haskell.org/package/brick), a declarative framework for building [TUI](https://en.wikipedia.org/wiki/Text-based_user_interface)
- [/haskell/wai](), the Web Application Interface that helps you to build the Web-apps
- [/haskell/servant](), a framework for HTTP APIs

# Online resources

- [Hoogle](https://hoogle.haskell.org/) (or just `!hoogle` *bang* in the [/DuckDuckGo]()), the "search by types"
- [https://packdeps.haskellers.com/reverse]() shows reverse dependencies for the Hackage's packages
- [https://hackage-search.serokell.io/](), a `grep(1)` like search over Hackage

# Haskell powered software

- [Xmonad](https://xmonad.org/), a [tiling window manager](https://en.wikipedia.org/wiki/Tiling_window_manager) 
- [/pandoc](), an ultimate text conversion tool
- [Shellcheck](https://www.shellcheck.net/), a tool that finds bugs in your shell scripts
- [hadolint](https://github.com/hadolint/hadolint), a `Dockerfile` (for [/Docker]()) linter

# Projects of mine

*(notable ones `:)`)*

- [Hemmet](https://github.com/astynax/hemmet), a text templating tool inspired by [Emmet](https://emmet.io/)/[ZenCoding](https://www.456bereastreet.com/archive/200909/write_html_and_css_quicker_with_with_zen_coding/)

# Notes

- ["Haskell with UTF-8"](https://serokell.io/blog/haskell-with-utf8), a proper way to handle IO with Unicode
