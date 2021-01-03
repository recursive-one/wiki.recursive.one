[optparse-applicative](https://hackage.haskell.org/package/optparse-applicative) provides a nice way to define CLIs using the [Applicative Functor](https://wiki.haskell.org/Applicative_functor)'s eDSL (`<$>` and `<*>`). One just declares a data type for all the options and uses a small set of combinators to "fill it up". In the end, one will have a parser with descriptive "help" and even with shell autocompletion.

Example:

```haskell
data Sample = Sample
  { hello :: String
  , quiet :: Bool
  }

sample :: Parser Sample
sample = Sample
  <$> strOption
    ( long "hello"
    <> metavar "TARGET"
    <> help "Target for the greeting" )
  <*> switch
    ( long "quiet"
    <> short 'q'
    <> help "Whether to be quiet" )

main :: IO ()
main = do
  ... <- execParser opts
  where
    opts = info (sample <**> helper)
      ( fullDesc
     <> progDesc "Print a greeting for TARGET"
     <> header "hello - a test for optparse-applicative" )

-- hello - a test for optparse-applicative
--
-- Usage: hello --hello TARGET [-q|--quiet] [--enthusiasm INT]
--   Print a greeting for TARGET
--
-- Available options:
--   --hello TARGET           Target for the greeting
--   -q,--quiet               Whether to be quiet
--   -h,--help                Show this help text
```

# Extra packages

- [optparse-version](https://hackage.haskell.org/package/optparse-version) provides a convinient "`-v`/`--version`" option:
  ```haskell
  info (sample <**> helper <**> version "0.1.0")
  ```
- [optparse-generic](https://hackage.haskell.org/package/optparse-generic) provides an auto-magic CLI for your `Generic` data type:
  ```haskell
  data Example = Example { foo :: Int, bar :: String } deriving (Generic)

  instance ParseRecord Example
  
  -- Test program
  --
  -- Usage: Example.hs --foo INT --bar STRING
  --
  -- Available options:
  --   -h,--help                Show this help text
  ```