---
toc: no
categories: Vim
...

I ([/who/histrio]()) have plenty of made-up reasons and excuses not to write something here. One of them is the fear of losing all that I wrote. A simple way to get some insurance about that is a simple auto-save. 

## Vim

For [/Vim] it will take no efforts. Just some config editing.

Auto save after timeout
```vimrc
autocmd CursorHold,CursorHoldI *.md update
```

Autosave on each change
```vimrc
autocmd TextChanged,TextChangedI *.md update
```

Autosave on focus lost
```vimrc
autocmd FocusLost,VimLeavePre *.md update
```