---
categories: TODO
...

<img src="https://raw.githubusercontent.com/babashka/babashka/master/logo/babashka.svg" style="float: right; margin-left: 0.5em; width: 100px;">

[Babashka](https://github.com/babashka/babashka) is a native, fast starting [/Clojure]() interpreter for scripting. It runs a subset of the Clojure for JVM in your shell and does it fast!

```bash
$ ls | bb -i '(filter #(-> % io/file .isDirectory) *input*)'
("doc" "resources" "sci" "script" "src" "target" "test")
bb took 4ms.
```

# How to

For now I have the babashka installed using the [/asdf]() version manager. I can use the [/Nix (package manager)]() but I don't want to get a whole [GraalVM](https://www.graalvm.org/) as a dependency :)

# Resources

- [Babashka Book](https://book.babashka.org/)
