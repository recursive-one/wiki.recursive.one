---
title: Functional Programming
toc: no
...

# Functional Programming

~~~ { .haskell }
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)
~~~