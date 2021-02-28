# gemini-server, gemini-router

[gemini-server](https://hackage.haskell.org/package/gemini-server) is a simple framework that helps to build the [/Gemini (protocol)]() applications like [this one](https://git.sr.ht/~fgaz/gemini-textboard). Any application looks like a functions from the request to the response.

Any more complex routing can be built using the [gemini-router](https://hackage.haskell.org/package/gemini-router) package.

# Gemtext

If one need to work just with Gemini text the one can get the [language-gemini](https://hackage.haskell.org/package/language-gemini) package: this one doesn't depend on any network stuff.