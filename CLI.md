# Command-Line Interfaces

[CLI](https://en.wikipedia.org/wiki/Command-line_interface) is a thing that many of us love a lot. But CLI is as good as we make them be, obviously. Here are some links to the best practices:

- [Minimal safe Bash script template](https://betterdev.blog/minimal-safe-bash-script-template/), a nice and sane "framework" for small scripts
- [12 Factor CLI Apps](https://medium.com/@jdxcode/12-factor-cli-apps-dd3c227a0e46) from authors of [The Twelve-Factor App](https://12factor.net/) ([Heroku](https://heroku.com)). Yep, some of the factors are so-so. Bot the intent itself is good. TLDR:
  1. Great help
  2. Flags instead of args
  3. Version info
  4. "stdout for output, stderr for messages"
  5. Error handling
  6. Colors plus `--no-color`
  7. "Prompt if you can" (interactivity)
  8. "Use tables"
  9. "Be speedy"
  10. "Encourage contributions" ("Plugins, COC, Open Source". Meh)
  11. "Be clear about subcommands"
  12. "Follow XDG-spec" **(!)**

Also, it will be nice to add an [/asciinema]() to your tool's documentation.

# Use the libraries, Luke

Implementation of the proper CLI is a though work. Hopefully, there are some shortcuts in this way. One just needs to remember about them.

- optparse-applicative ([/haskell/optparse-applicative]()) for [/Haskell]()
- Click ([/python/click]()) for [/Python]()