---
categories: Linux
...

# Who is who

<img src="https://www.debian.org/Pics/openlogo-50.png" style="float: right; margin-left: 0.5em">

- [dpkg](https://wiki.debian.org/dpkg), "a medium-level package manager for Debian"
- [apt](https://wiki.debian.org/Apt), "the main command-line package manager for Debian and its derivatives"
- [aptitude](https://wiki.debian.org/Aptitude), "an Ncurses and command-line based front-end to numerous Apt libraries" or just "[TUI](https://en.wikipedia.org/wiki/Text-based_user_interface) for Apt"

# Recipies

## Reverse dependencies

1. A simple one

    ```bash
    apt rdepends bash
    ```

2. More complicated and informative

    ```bash
    aptitude why bash
    ```

## Package the file came from

```bash
$ dpkg -S `which bash`
```

## Packages from alternative sources

```bash
$ grep Package /var/lib/apt/lists/*amd64_Packages \
    | grep -v ubuntu\.com \
    | grep -v canonical\.com
```