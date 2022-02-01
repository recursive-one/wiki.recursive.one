---
title: Self-describing Haskell scripts
...

# Cabal
  
```haskell
#!/usr/bin/env cabal
{- cabal:
build-depends: base, type-level-sets
-}
main = pure ()
```

([doc](https://cabal.readthedocs.io/en/3.6/cabal-commands.html#cabal-v2-run))

# Stack

```haskell
#!/usr/bin/env stack
{- stack
  script
  --resolver lts-14.20
  --package turtle
  --package "stm async"
  --package http-client,http-conduit
-}
main = pure ()
```

([doc](https://docs.haskellstack.org/en/stable/GUIDE/#script-interpreter))

# Nix

```haskell
#!/usr/bin/env nix-shell
#!nix-shell -i runghc -p "haskellPackages.ghcWithPackages(p: with p; [type-level-sets])"
#!nix-shell -I nixpkgs=channel:nixos-18.03
main = pure ()
```

([doc](https://nixos.org/manual/nix/stable/command-ref/nix-shell.html#use-as-a--interpreter), [using of shebangs](http://chriswarbo.net/projects/nixos/nix_shell_shebangs.html))