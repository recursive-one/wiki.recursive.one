---
toc: no
categories: Linux
...

[asdf](https://asdf-vm.com/) it is a version manager like [nvm](https://github.com/nvm-sh/nvm) (Node JS), [pyenv](https://github.com/pyenv/pyenv) ([/Python]()), [rvm](http://rvm.io/) (Ruby), [rustup](https://rustup.rs/) ([/Rust]()) and many others.

Usually, the *version manager* gives software developers the power to have as many versions of some toolchain as he wants. The developer even doesn't need to install any tools (even the VM itself) into the system globally. Yep, no more *sudo(1)* and external package repositories! Also, VM makes it possible to *pin* the toolchain version to this project.

Here *asdf* does the same: it helps to install and switch/pin the toolchains. But it works with many different toolchains at the same time! You just don't need pyenv/nvm/...vm anymore. Now you have a VM to rule them all!

Also, *asdf* manages many popular standalone tools like [bat](https://github.com/sharkdp/bat) or [kubectl](https://kubernetes.io/docs/reference/kubectl/kubectl/). Some of [/Rust powered tools]() we wrote about could be installed using asdf.

## Plugins

The core feature of asdf is the *plugin system*: asdf provides a simple framework and then [dozens of plugins](https://asdf-vm.com/#/plugins-all) enumerate, install, remove actual software pieces.

A typical scenario looks like this:

```bash
$ asdf plugin add clojure
$ asdf install clojure 1.10.1
$ asdf global clojure 1.10.1
$ clojure --version
Clojure 1.10.1
user=> ...
```

Any tool or even a set of tools could be pinned to the particular project and/or set as global defaults.