---
categories: Python
...

# Python language

<img src="https://www.python.org/static/img/python-logo.png" alt="Python logo" style="height: 64px">

Python is a "go-to language" that both of us ([/who/astynax]() and [/who/histrio]()) are using to do quick and dirty work. Because

- we know Python quite well
- it is "just here" (if you are using some sort of [/Linux]())
- it has "batteries included"

The language itself is far from ideal. But if one can tell "a language is just a tool" it will be about Python, a one of many tools in our toolbetls.

# Tooling

- [poetry](https://python-poetry.org/), a "Python packaging and dependency management made easy".
  - ["Developing Python with Poetry & Poetry2nix"](https://www.tweag.io/blog/2020-08-12-poetry2nix/) (see [/Nix (package manager)]())

# External "batteries" nice to have

- [plumbum](https://plumbum.readthedocs.io), a "shell combinators and more". Quick, dirty, fun, gets stuff done
- [click](https://click.palletsprojects.com), all you need to build a command-line tool
- [prompt_toolkit](https://python-prompt-toolkit.readthedocs.io) does all the heavy-lifting when you need to build a [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) (like [IPython](https://ipython.readthedocs.io)) or just a text adventure
