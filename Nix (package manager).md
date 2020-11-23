---
toc: no
...

<img src="https://avatars0.githubusercontent.com/u/487568?s=64&v=4" alt="The Nix logo" style="float: left; margin-right: 0.5em;">

[Nix](https://nixos.org/manual/nix/stable/) is "purely functional package manager". It manages sets of packages as immutable data structures so each particular environment has no dependencies from the outside world. This property makes it possible to have many versions of any piece of software simultaneously. You can even try to modify any particular environment and then roll it back. Any set of packages one can describe using "the Nix language" by writing a declarative program. Execution of this program with the Nix package manager will reproduce the described environment, and that is very convenient for development as for the deployment.
 
There is a [/Linux]() distribution [NixOS](https://nixos.org) which uses Nix as a system package manager. And one can configure the whole system with a single declarative program.

# Resources

- [Nix pills](https://nixos.org/guides/nix-pills/) is a nice step-by-step tutorial for the Nix newcomers
- ["Nix and Haskell in production"](https://github.com/Gabriel439/haskell-nix) teaches how to use Nix with [/Haskell]()

And of course, one should take a look into [the official documentation](https://nixos.org/learn.html). There are described many aspects of using Nix with different toolchains, ([/Python]() for example is mentioned [here](https://nixos.org/manual/nixpkgs/stable/#python)). 

# Tips

## Locales

By default there are no locales will be installed with glibc and some software won't work after installation. Here is a workaround:

1. Install `glibcLocales`:

    ```bash
    $ nix-env -iA nixpkgs.glibcLocales
    ```

2. Configure the environment:

    ```bash
    if [ -f "$HOME/.nix-profile/lib/locale/locale-archive" ]; then
        export LOCALE_ARCHIVE="$HOME/.nix-profile/lib/locale/locale-archive"
    fi
    ```
