---
title: Functional Programming
toc: no
...

# Functional Programming

I ([/who/astynax]()) like FP: [/Haskell](), [/Elm](), [/Clojure](), [/Racket](), maybe some [/Elixir](). That's why our Wiki is running on [/gitit]()!

It can be a piece of math

```haskell
-- | An infinite sequence of Fibonacci numbers
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)
```

Or a [Web App](https://ellie-app.com/bsnBBvtWbJwa1 "live demo")

```elm
main = Browser.sandbox
    { init = 0
    , update = always
    , view = \v -> Html.div []
        [ Html.button [ onClick <| v + 1 ] [ text "+" ]
        , text <| String.fromInt v
        , Html.button [ onClick <| v - 1 ] [ text "-" ]
        ]
    }
```

But it always fun! **Fun**ctional Programing forever!