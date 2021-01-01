---
categories: Haskell
title: Servant (framework)
...
The [servant](https://hackage.haskell.org/package/servant) library makes it possible to define HTTP APIs *on the type level*. Then having such API-types one can define clients and servers and even generate automatically mocks and API specs ([OpenAPI](https://en.wikipedia.org/wiki/OpenAPI_Specification)/[Swagger](https://en.wikipedia.org/wiki/Swagger_(software))).

# Ecosystem

- [servant](https://hackage.haskell.org/package/servant) one can use to define the API itself
- [servant-server](https://hackage.haskell.org/package/servant-server) helps to build WAI applications for the defined APIs
- [servant-multipart](https://hackage.haskell.org/package/servant-multipart) handles form data and file uploading
- [/haskell/wai](), the Web Application Interface - a way to define Warp-handlers
- [warp](https://hackage.haskell.org/package/warp), an embeddable Web-server
- [servant-lucid](https://hackage.haskell.org/package/servant-lucid) makes Lucid templates ([/haskell/lucid]()) "servant ready"

# Cookbook

### Redirect

```haskell
type FormPost = ... :> Verb 'POST 303 '[PlainText] (Redirect Text)
type Redirect = Headers '[Header "Location" Link]

-- ...
post :: ... -> Handler (Redirect Text)
post ... = do
  -- ...
  pure $ addHeader (safeLink ...) "ok"
```