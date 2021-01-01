---
title: Lucid
...
[Lucid](https://hackage.haskell.org/package/lucid) is a

> Clear to write, read and edit DSL for HTML

I found Lucid pretty concise and easy to use (alongside [/haskell/servant]() for example). You should write all the markup in [/Haskell]() but the whole process is pretty straightforward. There is no need for cycles or variable substitution because Lucid is an **eDSL** and all the code is just a bunch of function calls:

```haskell
page_ :: Html a -> Html a
page_ inner_ = do
  doctype_
  head_ $ do
    title_ "Hello World"
    link_
      [ rel_ "icon"
      , href_ "data:image/png;base64,"
      ]
  html_ $ do
    h3_ "Hello World"
    inner_
```

# Cookbook

## Maybe attributes

```haskell
field_ :: Show a => Text -> Maybe a -> Html () 
field_ name mv =
  input_ [name_ name] `with`  -- "with" works nice with comprehensions
    [value_ (Text.pack $ show v) | Just v <- [mv]]
```