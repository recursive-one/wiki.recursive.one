---
toc: no
...

[pandoc](https://pandoc.org/) is a converter between many text markup formats. It is written in [/Haskell]() but many uses even don't know that - they just use a statically linked binary or a system package. I think it is a good example of well-made software.

Pandoc can parse your [/Markdown]() file and produce a chunk of HTML, a standalone HTML page, or even a PDF document. It can highlight code examples, "render" LaTeX formulas, do many other text related kinds of work. As the official page says, "pandoc is your swiss-army knife". Even [/gitit]() renders this Wiki using pandoc!

[/Emacs]() users can process their Org mode files with [ox-pandoc ](https://github.com/kawabata/ox-pandoc). Also, one can run pandoc as a [/Docker]() container: there is a [plenty of images](https://hub.docker.com/u/pandoc).

## Filters

One neat feature of pandoc is filter support. Pandoc filters are small programs that read an [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree) of the input document, transform it, and produce the resulting AST. Usually, filters work with JSON, but one can have the access to more convenient representations if he will write the filter in

- [/Haskell]() with [pandoc as a library](https://hackage.haskell.org/package/pandoc)
- [/Python]() with [panflute](https://github.com/sergiocorreia/panflute/) package