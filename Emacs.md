---
title: GNU Emacs
...

<img src="https://www.gnu.org/software/emacs/images/emacs.png" style="float: right; margin-left: 0.5em; width: 64px;" alt="Orgmode logo">

I ([/who/astynax]()) use [GNU Emacs](https://www.gnu.org/software/emacs/) for anything, it is "the true one editor" for me: programming, note-taking, GTD, Web-bookmarks - Emacs helps me doing it. The main reason to use Emacs is its extensibility and the ability to bend an editor to the shape I like and find comfortable. Someone tweaks her bike or a car buys and replaces some old parts with new ones. I am doing the same with my editor and I like this process! :)

# My configuration

You can find it [here](https://github.com/astynax/dotfiles/blob/master/.emacs) with other [/dotfiles]().

# use-package

The capstone of my config is the [use-package](https://github.com/jwiegley/use-package): this package configures all other packages and even downloads them if some of it isn't present in the system.

# Org mode

<img src="https://orgmode.org/resources/img/org-mode-unicorn.svg" style="float: right; margin-left: 0.5em; width: 64px;" alt="Orgmode logo">

The [Org mode](https://orgmode.org/) - the main (and even *the only* for someone) reason to use Emacs. It is an IDE for notes, TODOs, agendas, contacts, writing, research. If I need to produce a good portion of text I am writing it in Org and then export it into the target format (Markdown, HTML, etc).

[Org babel](https://orgmode.org/worg/org-contrib/babel/intro.html) I use to do some [/Literate programming]() or just to play with some HTTP APIs. For the later task I use [restlient.el](https://github.com/pashky/restclient.el)+[ob-restclient.el](https://github.com/alf/ob-restclient.el).

# Working with projects

[projectile](https://docs.projectile.mx) - adds a project level to your buffers

# Magit

<img src="https://magit.vc/assets/magit-400x400px.png" style="float: right; margin-left: 0.5em; width: 64px;" alt="Magit logo">

[Magit](https://magit.vc/) is the ultimate way to do [/Git]() and to learn it in the process. Just a must-have.

Some great resources about Magit:

- [Magit deep dive](https://emacsconf.org/2019/talks/14/) (EmacsConf 2019)
- [Introduction to MAGIT](https://www.youtube.com/embed/2-0OwGTt0dI) by [Protesilaous Stavrou](https://protesilaos.com/)