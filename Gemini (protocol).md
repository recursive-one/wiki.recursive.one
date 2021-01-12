# The protocol

[Gemini](https://gemini.circumlunar.space/) is an alternative internet protocol. It looks a lot like a modern [Gopher](https://en.wikipedia.org/wiki/Gopher_(protocol)) but

- enforces [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security)
- has its own `text/gemini` media type (also the line-oriented as Gopher text)
- supports other [MIME-types](https://en.wikipedia.org/wiki/MIME) (images for example)

The full specification is available [here](https://gemini.circumlunar.space/docs/specification.html) and [here](https://portal.mozz.us/gemini/gemini.circumlunar.space/docs/specification.gmi) is a mirrored version of it, also available through Gemini itself.

# Resources

`gemini://gemini.circumlunar.space` is an entry point to the Geminiverse. To browse it you will need to have a **Gemini client**. But you can open any `gemini://` address within a Web-browser using some proxy server like [this](https://portal.mozz.us/gemini/gemini.circumlunar.space) or [that](https://proxy.vulpes.one/gemini/gemini.circumlunar.space).

Here are some clients:

- [Castor](https://git.sr.ht/~julienxx/castor) written in [/Rust]()
- [Xenia](https://gitlab.com/tslocum/xenia), a Gemini browser for [/Android]()
- [diohsc](https://portal.mozz.us/gemini/gemini.thegonz.net/diohsc/), a terminal client written in [/Haskell]()

Many pieces of Gemini-related software are listed [here](https://portal.mozz.us/gemini/gemini.circumlunar.space/software/). Also, one can always look at [awesome-gemini](https://github.com/kr1sp1n/awesome-gemini) repo.

**Gemini text** can be edited in [/Emacs]() (see [ox-gemini](https://github.com/emacsmirror/ox-gemini) and [gemini-mode](https://github.com/matt-y/gemini-mode). Also, Markdown can be converted to Gemini/text using [md2gemini](https://github.com/makeworld-the-better-one/md2gemini).

One can set up its own Gemini server and have a personnel star in the Gemini constellation. Many of such servers can be found in [this list](https://portal.mozz.us/gemini/gemini.circumlunar.space/servers/) or through the [GUS](https://portal.mozz.us/gemini/gus.guru/) (Gemini Universal Search). 

Notable servers:

- [Pollux](https://git.sr.ht/~julienxx/pollux) ([/Rust]())
- [Jetforce](https://github.com/michael-lazar/jetforce) ([/Python]())
  
    This one can be used not only as server for static files. One can build a whole application like [astrobotany](https://github.com/michael-lazar/astrobotany)

# Community

Many Gemini users have their own blogs - the "gemlogs". Usually, gemlog looks like [this](https://portal.mozz.us/gemini/gemini.marmaladefoo.com/blog/) or [that](https://portal.mozz.us/gemini/republic.circumlunar.space/users/joneworlds/) - minimalistic but nice. Someday I also build one for myself!

Also, some people from the [/Tilde]()verse create and host Gemini resources.

# Why

It is just fun! And there are people's thoughts:

- [What is this Gemini thing anyway, and why am I excited about it?](https://portal.mozz.us/gemini/drewdevault.com/2020/11/01/What-is-Gemini-anyway.gmi)
- [Why not just use a subset of HTTP and HTML?](https://portal.mozz.us/gemini/gemini.circumlunar.space/~solderpunk/gemlog/why-not-just-use-a-subset-of-http-and-html.gmi)
- [Gemini, the stronger twin](https://portal.mozz.us/gemini/gemini.sensorstation.co/computing/gemini.gmi)