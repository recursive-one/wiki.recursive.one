[Shake](https://shakebuild.com/) is a "built system" as they say. With Shake, you are just building your own build system using some sort of framework for [/Haskell](). Like "Build-System-as-a-Library", you know! Shake easily handles all the heavy-lifting: watching for FS changes, caching, running the sub-processes. Also, Shake-powered builds are cross-platform, unlike the ones that use [/GNU Make]().

GHC, the Glorious Haskell Compiler uses Shake and [many others](https://shakebuild.com/#who-uses-shake) do the same.

I ([/who/astynax]()) have used Shake here and there. For example, [astynax.me](https://astynax.me) was built using Shake as a part of my own little static-site generator.