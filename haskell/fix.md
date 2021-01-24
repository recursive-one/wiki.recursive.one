---
toc: no
...

# `fix` as a loop

One can use `fix` this way:

```haskell
main = do
  putStrLn "A cycle!"
  fix $ \loop -> do
    l <- getLine
    unless (null line) $ do
      putStrLn l
      loop
```

And even with the loop variable!

```haskell
main =
  flip fix 3 $ \loop i -> do
    print i
    unless (i == 0) $
      loop (i - 1)
```

Source: ["Write a simple loop with fix"](https://dev.to/lotz84/write-a-simple-loop-with-fix-np)

