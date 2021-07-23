---
title: WAI, Web Application Interface
...

[WAI](https://hackage.haskell.org/package/wai) is a common way to develop Web-applications in [/Haskell]. With WAI one defines handlers for the [warp](https://hackage.haskell.org/package/warp) server.

# Packages

- [wai-extra](https://hackage.haskell.org/package/wai-extra) provides a bunch of middlewares that handle
    - testing
    - Gzip'ping
    - request logging
    - simple routing
    - file streaming
    - ...
- [wai-middleware-static](https://hackage.haskell.org/package/wai-middleware-static) helps to serve static files
- [scotty](https://hackage.haskell.org/package/scotty) is a [Sinatra](http://sinatrarb.com/)-like routing library
- [wai-cli](https://hackage.haskell.org/package/wai-cli), a "command line runner for Wai apps". TLS, dev-logging, graceful shutdown.