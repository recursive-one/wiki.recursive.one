---
categories: Haskell
...
When you need to parse something you can juggle bytes and characters with your hands or write some BNF grammars. Or, if you love [/FP]() you can use the *parser combinators* to grow up any complex parser from a *combination* of small bits. Especially, this kind of parsing is fun if you are using languages like [/Haskell]() :)

# [/Haskell]()

- [parsec](https://hackage.haskell.org/package/parsec), the most famous but a bit old and clumsy library
- [megaparsec](https://hackage.haskell.org/package/megaparsec), the new "cool kid", fast and fancy
- [attoparsec](https://hackage.haskell.org/package/attoparsec) when you need to process some big chunks of raw bytes

# [/Python]()

- [funcparserlib](https://pypi.org/project/funcparserlib/), just "the Parsec for Python" :)

# Other resources

- ["Parser Combinators: a Walkthrough"](https://hasura.io/blog/parser-combinators-walkthrough/), a good introduction article about Parsec-like parsers.
