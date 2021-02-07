# Cabal & cabal-install

[Cabal/cabal-install](https://cabal.readthedocs.io/) is a lib/tool for the building of [/Haskell] based projects.

# Recipies

## Common stanzas

```yaml
common deps
  build-depends: base ^>= 4.11
  ghc-options: -Wall

common test-deps
  build-depends: tasty ^>= 0.12.0.1

library
  import: deps
  exposed-modules: Foo

test-suite tests
  import: deps, test-deps
  type: exitcode-stdio-1.0
  main-is: Tests.hs
  build-depends: foo
```

([source](https://cabal.readthedocs.io/en/latest/cabal-package.html#common-stanzas))