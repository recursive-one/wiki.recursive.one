---
toc: no
...

Rofi is a modern [dmenu](https://linux.die.net/man/1/dmenu) successor. Usually, it looks like an on-screen menu and helps to

- switch windows quickly
- launch programs
- select stuff

![Rofi in a window switching mode](https://davatorium.github.io/rofi/images/rofi/window-list.png)

# Usage

```bash
$ rofi -modi "window,run,ssh" -show run
```

- `-modi` enables some builtin "tabs", "window" stays for window switcher, "run" gives you a app launcher (any executable from `$PATH`), "ssh" selects the host to connect to
- `-show` sets an active tab

In "run" mode you can run the selected item in a *new shell window* buy pressing `<Shift>-<Return>` instead sole `<Return>`.

There are many options for the look&feel and behavior customization. So just read `man rofi` :)

# Custom menus

One can just pipe to Rofi some text strings and then select any of them using [fuzzy matching](https://www.techopedia.com/definition/24183/fuzzy-matching). Rofi keeps selection history and makes future choices even quicker.

That's how I use Rofi to switch between video outputs:

```bash
# files in ~/.screenlayout/ are profiles saved from arandr(1)
ls -1 .screenlayout/*.sh | rofi -dmenu -p 'Screen Layout:' | xargs -r sh
```

And here is my "remote control" for the [/mpd]() (using `mpc`):

```bash
echo 'toggle\nnext\nprev\nplay\nstop' | rofi -dmenu -p 'MPD:' | xargs mpc
```

# Menu-bases GUI

I ([/who/astynax]()) have built a simple Python library named [pyrofi](https://github.com/astynax/pyrofi) to build user interfaces from nested menus.

There are libraries that are way more powerful than mine. The [python-rofi-menu](https://github.com/miphreal/python-rofi-menu) for example. But I found it too complicated for my pretty simple cases: I just don't want to define a couple of classes to have a simple menu. So my pyrofi uses a single function call and a single data structure and all the program looks like that:

```python
run_menu({
    'Calculator': ['xcalc'],
    'Games': {
        'Rogue': ['rogue'],
        'Angband': ['angband']
    },
    'Calendar': ['ncal', '2020'],
})
```

# Wofi

[Wofi] is a clone of Rofi for the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol).