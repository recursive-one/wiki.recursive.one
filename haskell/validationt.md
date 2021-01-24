---
toc: no
...

[validationt](https://hackage.haskell.org/package/validationt), "a simple data validation library."

# TLDR

```haskell
import Control.Monad.Validation
import Control.Monad (when)

data User = User
  { name :: String
  , pass :: String
  , age  :: Maybe Int
  } deriving Show

main :: IO ()
main = do
  u <- runValidationT $ User <$> vName "Bob" <*> vPass "abc" <*> vAge (Just 20)
  print u
  where
    vName n = vZoom (mmSingleton "name") $ do
      when (null n) $ vError ["is empty"]
      when (length n < 5) $ vWarning ["is too short"]
      pure n
    vPass p = vZoom (mmSingleton "pass") $ do
      when (null p) $ vError ["is empty"]
      when (length p < 5) $ vWarning ["is too short"]
      pure p
    vAge Nothing  = pure Nothing
    vAge (Just a) = vZoom (mmSingleton "age") $ do
      when (a < 1) $ vError ["too low"]
      when (a > 120) $ vWarning ["too high"]
      when (a < 18) $ vWarning ["is low"]
      pure $ Just a
```