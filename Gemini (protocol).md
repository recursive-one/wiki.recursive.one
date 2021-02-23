# The protocol

[Gemini](https://gemini.circumlunar.space/) is an alternative internet protocol. It looks a lot like a modern [Gopher](https://en.wikipedia.org/wiki/Gopher_(protocol)) but

- enforces [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security)
- has its own `text/gemini` media type (also the line-oriented as Gopher text)
- supports other [MIME-types](https://en.wikipedia.org/wiki/MIME) (images for example)

The full specification is available [here](https://gemini.circumlunar.space/docs/specification.html) (mirror in Gemini: `gemini://gemini.circumlunar.space/docs/specification.gmi` ([or via HTTP-proxy](https://portal.mozz.us/gemini/gemini.circumlunar.space/docs/specification.gmi)).

# Resources

`gemini://gemini.circumlunar.space` is an entry point to the Geminspace. To browse it you will need to have a **Gemini client**. But you can open any `gemini://` address within a Web-browser using some proxy server like [this](https://portal.mozz.us/gemini/gemini.circumlunar.space) or [that](https://proxy.vulpes.one/gemini/gemini.circumlunar.space).

Here are some clients:

- [Castor](https://git.sr.ht/~julienxx/castor) written in [/Rust]()
- [Lagrange](https://gmi.skyjake.fi/lagrange), nice and slick but powerful GUI client written in C11 using SDL
- [kristall](https://kristall.random-projects.net/), a cross-platform "Small-Internet Browser", supports Gopher and Finger too. 
- [Deedum](https://github.com/snoe/deedum), a Gemini browser for [/Android]()
- [diohsc](https://portal.mozz.us/gemini/gemini.thegonz.net/diohsc/), a terminal client written in [/Haskell]()

Many pieces of Gemini-related software are listed [here](https://portal.mozz.us/gemini/gemini.circumlunar.space/software/). Also, one can always look at [awesome-gemini](https://github.com/kr1sp1n/awesome-gemini) repo.

**Gemini text** can be edited in [/Emacs]() (see [ox-gemini](https://github.com/emacsmirror/ox-gemini) and [gemini-mode](https://github.com/matt-y/gemini-mode). Also, Markdown can be converted to Gemini/text using [md2gemini](https://github.com/makeworld-the-better-one/md2gemini).

One can set up its own Gemini server and have a personal star in the Gemini constellation. Many of such servers can be found in [this list](https://portal.mozz.us/gemini/gemini.circumlunar.space/servers/) or through the [GUS](https://portal.mozz.us/gemini/gus.guru/) (Gemini Universal Search). 

Notable servers and server-side frameworks:

- [Pollux](https://git.sr.ht/~julienxx/pollux) ([/Rust]())
- [Agate](https://github.com/mbrubeck/agate) (also [/Rust]())
- [Jetforce](https://github.com/michael-lazar/jetforce) ([/Python]())
  
  This one can serve some static files but can be used to build applications like [astrobotany](https://github.com/michael-lazar/astrobotany)

- [gig](https://github.com/pitr/gig), a framework for ([/Golang]()), looks pretty neat
- [/haskell/gemini-server](), a simple framework for [/Haskell]()

# Community

Many Gemini users have their own blogs - the "gemlogs". Usually, gemlog looks like [this](https://portal.mozz.us/gemini/gemini.marmaladefoo.com/blog/) or [that](https://portal.mozz.us/gemini/republic.circumlunar.space/users/joneworlds/) - minimalistic but nice. Someday I also build one for myself!

Also, some people from the [/Tilde]()verse create and host Gemini resources.

There is even a some kind of "blogging platforms" like [flounder](https://flounder.online/) where you can register a profile and just write some posts. That posts will be accessible as from Gemini as from portal's HTTP face.

# Why

It is just fun! And there are people's thoughts:

- [What is this Gemini thing anyway, and why am I excited about it?](https://portal.mozz.us/gemini/drewdevault.com/2020/11/01/What-is-Gemini-anyway.gmi)
- [Why not just use a subset of HTTP and HTML?](https://portal.mozz.us/gemini/gemini.circumlunar.space/~solderpunk/gemlog/why-not-just-use-a-subset-of-http-and-html.gmi)
- [Gemini, the stronger twin](https://portal.mozz.us/gemini/gemini.sensorstation.co/computing/gemini.gmi)

# Interesting content

- ["A vision for Gemini applications"](https://portal.mozz.us/gemini/gemini.circumlunar.space/~solderpunk/gemlog/a-vision-for-gemini-applications.gmi)
- ["Subscribing to Gemini pages"](https://portal.mozz.us/gemini/gemini.circumlunar.space/docs/companion/subscription.gmi), some thoughts about separate feeds VS the page content itself as a source of changes to subscribe to.
- ["Gemini and POST"](https://portal.mozz.us/gemini/warmedal.se/~bjorn/posts/gemini-and-post.gmi) + [".., Part 2"](https://portal.mozz.us/gemini/warmedal.se/~bjorn/posts/gemini-and-post-part2.gmi)