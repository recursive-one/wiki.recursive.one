---
title: The "Fur tree" exercise
categories: fun
...

# The "Fur tree" exercise

There is a programming exercise I like: "The fur tree". The task is pretty simple. You just need to grow a tree with a defined height (number of levels). Your tree should look like this (that one has height "5"):

```text
    *
   ***
  *****
 *******
*********
```

Here is a small collection of thees grown by me :)

## Haskell

```haskell
import Data.Char (isSpace)
import Data.List (takeWhile)

main :: IO ()
main = putStr $ pine 10
  where
    pine =
      unlines
      . takeWhile (isSpace . head)
      . iterate (tail . (++ "**"))
      . (++ "*")
      . flip replicate ' '
```


## Python

```python
# one can rewrite this code as one-liner :)

def pine(n):
    return '\n'.join(
        (' ' * (n - x)) + ('*' * (x * 2 - 1))
        for x in range(1, n + 1)
    )

print(pine((10)))
```


## [dc(1)](https://www.gnu.org/software/bc/manual/dc-1.05/)

```sh
dc -e "[32P1-d0!=b]sb[42P1-d0!=s]ss[lilbxln+li-2*1-lsx]sr[li1-silrx10Pli1!=m]sm 10 1+snlnsilmx"
```