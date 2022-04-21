# Subject

<img style="background-color: white; float: right;" alt="Rust logo" src="https://www.rust-lang.org/static/images/rust-logo-blk.svg">

Many projects are proposing nice alternatives to various command-line tools like *grep(1)* or *ls(1)*. Some of them are written in [/Rust](). Here we have a list of such tools that we use ourselves.

# How to

Rust has its own build tool and package manager called ["cargo"](https://doc.rust-lang.org/stable/cargo/). When you are asking Cargo to install some *software* (not a library) it usually puts the executable binaries into "`${HOME}/.cargo/bin`". So make sure you have this directory in your `$PATH`.

To install any of the listed below tools you will need to run "`cargo install <name>`". But some projects also provide `.deb` packages or just the zipped binaries — take a look at the repos.

Also, some of the mentioned tools could be installed using [/asdf]() or [/Nix (package manager)]().

# The tools

- [ripgrep](https://github.com/BurntSushi/ripgrep) — very fast and [/Git]()-aware modern alternative to *grep(1)*
- [bat](https://github.com/sharkdp/bat) — drop-in replacement for *cat(1)* with syntax highlighting, line numbering, diff preview
- [exa](https://github.com/ogham/exa) — modern replacement for the venerable file-listing command-line program *ls(1)*
- [fd-find](https://github.com/sharkdp/fd) — simple, fast and user-friendly alternative to *find(1)*
- [just](https://github.com/casey/just) — very simple alternative to [/GNU Make]()
- [du-dust](https://github.com/bootandy/dust) — more intuitive version of *du(1)* in rust
- [procs](https://github.com/dalance/procs) — modern replacement for *ps(1)*
- [skim](https://github.com/lotabout/skim) — an [fzf](https://github.com/junegunn/fzf)-like [fuzzy matching](https://www.techopedia.com/definition/24183/fuzzy-matching) search and selection tool
- [difftastic](https://difftastic.wilfred.me.uk/) — a syntax-aware replacement for `git diff`, can be easily integrated with [/git]()

# Not-so-replacements

These projects don't pose themselves as replacements for "good old Unix tools". But they also are built using Rust and we found it interesting :)

- [tealdeer](https://github.com/dbrgn/tealdeer) — very fast implementation of [tldr](https://github.com/tldr-pages/tldr) 
- [ffsend](https://github.com/timvisee/ffsend) — fully featured Firefox Send client
- [hyperfine](https://github.com/sharkdp/hyperfine) — command-line benchmarking tool
- [alacritty](https://github.com/alacritty/alacritty) — terminal emulator
- [drill](https://github.com/fcsonline/drill) — HTTP load testing application
- [autojump](https://github.com/xen0n/autojump-rs) — port of the wildly popular helper application [autojump](https://github.com/wting/autojump)
- [bb](https://github.com/epilys/bb) — simple process viewer
- [git-delta](https://github.com/dandavison/delta) — viewer for git and diff output
- [dura](https://github.com/tkellogg/dura) — "a background process that watches your Git repositories and commits your uncommitted changes without impacting HEAD, the current branch, or the Git index"
- [meli](https://github.com/meli/meli) — terminal email client
- [rage](https://github.com/str4d/rage) — encryption tool
- [ht](https://github.com/ducaale/ht) — "Yet another HTTPie clone". [HTTPie](https://httpie.io/) is a [/Python]() powered ["Swiss Army knife"](https://en.wikipedia.org/wiki/Swiss_Army_knife) for HTTP requests.
- [gitui](https://github.com/extrawurst/gitui) — a neat [/TUI]() for the [/Git]()
- [miniserve](https://github.com/svenstaro/miniserve) — a "[/CLI]() tool to serve files and dirs over HTTP"

## Editors

Yep, editor building is a pretty popular theme for the hobby projects. There are some:

- [Xi-Editor](), dead but good. Was the first one of the kind and still gives the inspiration for new projects.
- [Lapce](https://github.com/lapce/lapce), a pretty new one. Proposes a [/WASI]() based plugin system!

# Aliases

Some (most?) of the mentioned tools are designed as "drop-in" replacements for the corresponding programs. That's why you can add some aliases to your shell and keep the muscle memory:
   
```bash
alias cat="bat"
alias ll="exa --long"
alias ls="exa"
```