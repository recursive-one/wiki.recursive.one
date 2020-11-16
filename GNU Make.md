---
toc: no
category: Linux
...

I ([/who/astynax]()) use [GNU make](https://www.gnu.org/software/make/) really often. Every time I need to remember some long command or two I prefer to add a `Makefile` with single [.PHONY target](https://www.gnu.org/software/make/manual/html_node/Phony-Targets.html#Phony-Targets) instead.

Yes, "shortcut management" is not the main function of Make but nowadays most Linux newcomers are using it just this way. Even [modern tutorials](https://makefile.site) are keeping focus only on "command" execution. Sad but true.

I myself is trying to use Make as build toot when it is convenient. Most of the languages I use have their own build tools so I need to *make* something only in very specific situations, but when I need it Make can save the day!

Also I have some alternatives to choose from when I feel what my Makefile grows too large. [/Shake (build system)]() is the one of such variants.

## Fun stuff

Here is a "static site generator" that uses [/pandoc]() to build simple static site from the bunch of [/Markdown]() files.

```makefile
.PHONY: markdown
markdown:
	find src/ -name *.md -print \
	| sed -e 's/\.md$$/\.html/' \
	| sed -e 's/src/_site/' \
	| xargs -n 1 make

_site/%.html: src/%.md
	test -d $(@D) || mkdir -p $(@D)
	pandoc -s -o "$@" "$<"

.PHONY: clean
clean: _site
	rm -r _site
```

*(Yes, I know, this sed-dark-magic looks scary! `:)`)*