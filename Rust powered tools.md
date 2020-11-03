# Rust powered tools

There are many projects those are proposing a nice alternatives to various command line tools like `grep` or `ls`. Many of them are written in [/Rust](). Here we have a list of such tools those we use ourself.

## How to

Rust has own build tool called "cargo". When you are asking Cargo to install some *software* (not a library) it usually puts the executable binaries into `${HOME}/.cargo/bin`. So make sure what you have this directory in your `$PATH`.

To install any of listed below tools you will need to run `cargo install <name>`. But some projects also provide `.deb` packages or just the zipped binaries — take a look onto the repos.

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
