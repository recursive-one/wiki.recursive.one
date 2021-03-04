---
toc: no
...

<img src="https://avatars0.githubusercontent.com/u/487568?s=64&v=4" alt="The Nix logo" style="float: left; margin-right: 0.5em;">

[Nix](https://nixos.org/manual/nix/stable/) is "purely functional package manager". It manages sets of packages as immutable data structures so each particular environment has no dependencies from the outside world. This property makes it possible to have many versions of any piece of software simultaneously. You can even try to modify any particular environment and then roll it back. Any set of packages one can describe using "the Nix language" by writing a declarative program. Execution of this program with the Nix package manager will reproduce the described environment, and that is very convenient for development as for the deployment.
 
There is a [/Linux]() distribution [NixOS](https://nixos.org) which uses Nix as a system package manager. And one can configure the whole system with a single declarative program.

# Resources

- [Nix pills](https://nixos.org/guides/nix-pills/) is a nice step-by-step tutorial for the Nix newcomers
- [nix.dev](https://nix.dev/), "An opinionated guide for developers getting things done using the Nix ecosystem."
- [Scrive Nix Workshop](https://scrive.github.io/nix-workshop/), "the workshop materials used for training Haskell developers at Scrive."
- ["Nix and Haskell in production"](https://github.com/Gabriel439/haskell-nix) teaches how to use Nix with [/Haskell]()
- [NUR](https://github.com/nix-community/NUR), the Nix User Repository, user contributed nix packages. Here is a [template](https://github.com/nix-community/nur-packages-template) for such packages

And of course, one should take a look into [the official documentation](https://nixos.org/learn.html). There are described many aspects of using Nix with different toolchains, ([/Python]() for example is mentioned [here](https://nixos.org/manual/nixpkgs/stable/#python)). The ["Developing Python with Poetry & Poetry2nix"](https://www.tweag.io/blog/2020-08-12-poetry2nix/) is also a good entry point to Nix for the Python users.

# Additional tools

- [nix-tree](https://github.com/utdemir/nix-tree), "Interactively browse the dependency graph of your Nix derivations."
- [nix-script](https://github.com/BrianHicks/nix-script), that "lets you write quick scripts in compiled languages, tranparently compile and cache them, and pull in whatever dependencies you need from the Nix ecosystem." (see an [article](https://bytes.zone/posts/nix-script/))

# Nix Flakes

[Nix Flakes](https://nixos.wiki/wiki/Flakes) are an upcoming feature of the Nix package manager.

Series of posts in the Tweag.io blog:
- ["Nix Flakes, Part 1: An introduction and tutorial"](https://www.tweag.io/blog/2020-05-25-flakes/)
- ["Nix Flakes, Part 2: Evaluation caching"](https://www.tweag.io/blog/2020-06-25-eval-cache/)
- ["Nix Flakes, Part 3: Managing NixOS systems"](https://www.tweag.io/blog/2020-07-31-nixos-flakes/)

# Tips

## Subprocesses

If you are using some app that run other apps as subprocesses (like [/Rofi]()) then beware: all the subprocesses will run inside the same nix env.

For example, rofi depends on the Gtk and runs any apps inside the env with this particular version of Gtk. For me it breaks any Gtk-based apps those I run from the rofi!

## How much

This command shows how many space will "eat" a particular package:

```shell
nix-env --dry-run -iA nixpkgs.gimp
```

## Profile update

```shell
nix-env -iA nixpkgs.myPackages && nix-collect-garbage
```

With `-r` it will remove all the packages that aren't mentioned in your `myPackages`.

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

## "Why"

[nix-tree](https://github.com/utdemir/nix-tree) can tell why this or that package was installed.