---
title: Functional Programming
toc: no
...

# Functional Programming

I ([/who/astynax]()) like FP: [/Haskell](), [/Elm](), [/Clojure](), [/Racket](). That's why our Wiki is running on [/gitit]()!

```haskell
-- | An infinite sequence of Fibonacci numbers
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)
```