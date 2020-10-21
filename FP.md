---
title: Functional Programming
toc: no
...

# Functional Programming

I ([who/astynax]()) like Haskell, Elm, Clojure, Racket. That's why you are reading this Wiki as [gitit]() pages!

```haskell
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)
```