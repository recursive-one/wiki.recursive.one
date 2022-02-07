---
toc: no
categories: emacs,emacs-lisp
...

# `org-mks`

Just found the `org-mks` function used in [/Org Mode]() capturing. Looks simple to use and because I always have Org Mode installed I can use `org-mks` in my personal tasks.

Example:?revision=764c29b87ca14242c1ed7cf2d1d88d92ccf38148

```commonlisp
(org-mks
 ; TABLE documented as ALIST but only proper lists work
 '(("m" "Make") ; named prefix
   ("mb" "Breakfast" breakfast) ; final entry
   ("mc" "Coffee" coffee)
   ("p" "Play")
   ("pg" "Game" game))
 "Activities"
)
;; => ("pg" "Game" game) ; returns the whole entry
```