---
toc: no
...

# Rust powered tools

<img style="background-color: white; float: right;" alt="Rust logo" src="https://www.rust-lang.org/static/images/rust-logo-blk.svg">

There are many projects that are proposing nice alternatives to various command-line tools like *grep(1)* or *ls(1)*. Some of them are written in [/Rust](). Here we have a list of such tools those we use ourselves.

## How to

Rust has its own build tool called "cargo". When you are asking Cargo to install some *software* (not a library) it usually puts the executable binaries into "`${HOME}/.cargo/bin`". So make sure what you have this directory in your `$PATH`.

To install any of the listed below tools you will need to run "`cargo install <name>`". But some projects also provide `.deb` packages or just the zipped binaries — take a look at the repos.

## The tools

- [ripgrep](https://github.com/BurntSushi/ripgrep) — very fast and [/Git]()-aware modern alternative to *grep(1)*
- [bat](https://github.com/sharkdp/bat) — drop-in replacement for *cat(1)* with syntax highlighting, line numbering, diff preview

## TODO

- tealdeer
- exa
- ffsend
- hyperfine
- fd
- just
- alacritty
- dust
- drill
- autojump-rs
- bb
- git-delta
- dust
- meli

### Some aliases

```
alias ll="exa --long"
alias ls="exa"
```
